---
description: Saiba como gerar tokens do Livefyre usando o idioma «C
seo-description: Saiba como gerar tokens do Livefyre usando o idioma «C
seo-title: Criar Tokens do Livefyre'C
solution: Experience Manager
title: Criar Tokens do Livefyre'C
uuid: c 5 e 05625-8550-4 b 51-9211-134600 e 20 ec 7
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Criar Tokens do Livefyre C\ # {#creating-livefyre-tokens-c}

Saiba mais sobre como gerar tokens do Livefyre usando a linguagem ``C#``.

Você pode aproveitar a documentação e o código de amostra herdados para usar `C#.NET` para criar métodos para criar tokens.

Para consultar as bibliotecas oficiais do Livefyre, use a Biblioteca [Java](https://github.com/Livefyre/livefyre-java-utils) como ponto de partida para `C#` desenvolvedores.

Você também pode considerar usar a [Biblioteca](https://github.com/Livefyre/livefyre-nodejs-utils) Node. js na linha de comando para gerar tokens de referência para si mesmo e para familiarizar-se com a estrutura do método.

* [Ir para o metadado da coleção](https://gist.github.com/gibron/56cb9c7060bf4816c4c5#the-collectionMeta-token)
* [Ir para o token de autenticação](https://gist.github.com/gibron/56cb9c7060bf4816c4c5#the-auth-token)

## Dependências {#section_c15_fnh_xz}

* Você precisará do [pacote](https://www.nuget.org/packages/JWT) JWT nuget no seu projeto para gerar os tokens.
* Amostras de código nesta página usam o [pacote Newtonsoft JSON](https://www.nuget.org/packages/newtonsoft.json/) .

## Collectionmeta token {#section_dzt_4mh_xz}

O collectionmeta token é transmitido ao Livefyre quando você incorpora Comentários em uma página e fornece o sistema com os metadados necessários para a nova coleção. Além disso, você criará um MD 5 `checksum` desses dados, que o Livefyre verifica para ver se os metadados foram alterados. (por exemplo, se o título ou url do seu artigo foi editado).

Esse token é assinado com seu `Site Key`, que foi fornecido por seu Gerente de Conta Techtival no Livefyre.

Consulte também:

* Documentos collectionmeta Token
* [Exemplo Gist](https://gist.github.com/pcolombo/dbbea020618c521a2bd5)

1. Crie um Dicionário contendo os metadados da coleção. Vamos adicionar apenas alguns dos campos necessários nesta etapa, pois queremos criar uma soma de verificação desse objeto antes de adicionar o articleid.

   ```
       // Site Key provided by Livefyre 
       string siteSecret = "ABCDE1234"; 
   
       var meta = new Dictionary<string, object>() { 
           {"title", "Kings win the Stanley Cup"}, 
           {"url", "https://www.website.com/kings-win-stanley-cup"}, 
           {"tags", "sports, hockey, stanley_cup"}, 
           {"type", "livecomments"} 
       };
   ```

   * **título** *necessário*: O título da coleção, normalmente o título do artigo. O comprimento máximo é de 255 caracteres. Não suporta entidades html. Codifice caracteres especiais usando UTF -8.
   * **url** *obrigatório*: O url canônico do artigo. Isso é usado pelos recursos de compartilhamento de comentário e sincronização social, e links para seu artigo a partir do painel de administração. Se estiver testando localmente, observe que o Livefyre não aceitará "localhost" como um domínio.
   * *****opcionais*: Uma lista de tags separada por vírgulas que você deseja adicionar à coleção no painel do Livefyre. As tags não podem conter espaços. Use sublinhados se desejar que um espaço apareça no painel de administração.
   * **type** *optional*:  A string indicating what type of collection to create. Os valores válidos são:

      * `reviews`
      * `sidenotes`
      * `ratings`
      * `counting`
      * `livecomments`
      * `liveblog`
      * `livechat`
      Se não for especificado, uma coleção livecomments é criada por padrão.


1. O JSON codifica esse dicionário e gere uma soma de verificação md 5 disso.

   ```
          var metaStr = JsonConvert.SerializeObject(meta); 
       byte[] hash; 
   
       using (var md5 = MD5.Create()) 
       { 
           hash = md5.ComputeHash(Encoding.UTF8.GetBytes(metaStr)); 
       } 
   
       StringBuilder sBuilder = new StringBuilder(); 
   
       // Loop through each byte of the hashed data  
       // and format each one as a hexadecimal string  
       for (int i = 0; i < hash.Length; i++) 
       { 
           sBuilder.Append(hash[i].ToString("x2")); 
       } 
   ```

1. Adicione **o articleid** ao dicionário. **A soma de verificação** não entra no collcollectionmeta, mas deve ser enviada como um parâmetro de seaprate no objeto de js convconfig.

   ```
       meta.Add("articleId", "article-abcde00001"); 
   ```

   * **Articleid** *necessário*: Um identificador exclusivo da sua coleção no site do Livefyre. Normalmente, o articleid único usado em seu CMS. (por exemplo, a ID de publicação do wordpress) Esse valor nunca deve ser alterado. O Livefyre identifica coleções exclusivas pela combinação de siteid e articleid.

1. Gere um token JWT assinado do dicionário usando a Chave do site fornecida para você pelo Livefyre. Observe que você deve especificar o algoritmo correto de hash, já que o pacote JWT não usa o HS 256 por padrão.

   ```
       string token = JWT.JsonWebToken.Encode(meta, siteSecret, JWT.JwtHashAlgorithm.HS256);
   ```

## O token de autenticação do usuário {#section_g1d_43h_xz}

O Token de autenticação do usuário é usado para assinar um usuário no Livefyre. Quando um usuário entra em seu site, o site gera um Token de autenticação do usuário passado para o widget do Livefyre na página. (Para obter mais informações sobre o processo de autenticação, consulte Perfis remotos.)

Esse token requer o nome da rede (network. fyre. co) e é assinado com sua Chave de rede, que é fornecida para você pelo Gerente de conta técnico no Livefyre.

Consulte também:

* Documentos de token de autenticação oficial
* [Exemplo Gist](https://gist.github.com/pcolombo/7d7403172c28734c87e2)

1. Crie um dicionário contendo as informações necessárias.

   ```
       string networkKey = "ABCDEF1234"; 
   
       var payload = new Dictionary<string, object>() {  
               { "domain", "mynetwork.fyre.co" }, 
               { "user_id", "user-00001" }, 
               { "expires", DateTime.Now.AddDays(7).Ticks }, 
               { "display_name", "johndoe" } 
           }; 
   ```

   * **domínio:** O nome da rede (fornecido pelo Livefyre.) Por exemplo, mynetwork. fyre. co
   * **user_ id:** A ID de usuário exclusiva para o usuário no sistema de perfil do site. Deve ser apenas caracteres alfanuméricos (A-Z, a-z, 0-9). Se a ID de usuário de sistemas contiver charaacters inválidos, considere enviar um hash md 5 da ID do usuário, ou uma versão codificada base 64 desse ID. (Deixe o gerente da conta saber se você fez isso.)
   * **expira:** A data (em época de época) que o token expira. Isso deve corresponder ao tempo de sessão de logons no site, para que o estado conectado do Livefyre fique sincronizado com o estado conectado do site.
   * **display_ name:** O nome de exibição do usuário no sistema de perfil, como deve ser exibido no fluxo de comentário.

1. Gere um token JWT assinado do dicionário usando a Chave de rede fornecida para você pelo Livefyre. Observe que você deve especificar o algoritmo correto de hash, já que o pacote JWT não usa o HS 256 por padrão.

   ```
          string token = JWT.JsonWebToken.Encode(payload, networkKey, JWT.JwtHashAlgorithm.HS256);
   ```
