---
description: Saiba como gerar tokens do Livefyre usando a linguagem "C#".
title: Criação de tokens do Livefyre "C#"
exl-id: 6360c325-0c3f-4ecb-90f7-951ef4e6f410
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '784'
ht-degree: 2%

---

# Criação de tokens do Livefyre C\# {#creating-livefyre-tokens-c}

Saiba mais sobre como gerar tokens do Livefyre usando a linguagem ``C#``.

Você pode aproveitar a documentação herdada e o código de amostra para usar `C#.NET` para gravar métodos para criar tokens.

Para fazer referência às bibliotecas oficiais do Livefyre, use a [Biblioteca Java](https://github.com/Livefyre/livefyre-java-utils) como ponto de partida para desenvolvedores `C#`.

Você também pode considerar o uso da [Biblioteca Node.js](https://github.com/Livefyre/livefyre-nodejs-utils) da linha de comando para gerar tokens de referência para você mesmo e familiarizar-se com a estrutura do método.

* [Ir para o Meta Token da Coleção](https://gist.github.com/gibron/56cb9c7060bf4816c4c5#the-collectionMeta-token)
* [Ir para o token de autenticação](https://gist.github.com/gibron/56cb9c7060bf4816c4c5#the-auth-token)

## Dependências {#section_c15_fnh_xz}

* Você precisará do [pacote de nuget JWT](https://www.nuget.org/packages/JWT) em seu projeto para gerar os tokens.
* Amostras de código nesta página usam o pacote [Newtonsoft JSON](https://www.nuget.org/packages/newtonsoft.json/).

## CollectionMeta Token {#section_dzt_4mh_xz}

O CollectionMeta Token é passado para o Livefyre quando você incorpora Comentários em uma página e fornece ao sistema os metadados necessários para sua nova coleção. Além disso, você criará um MD5 `checksum` desses dados, que o Livefyre verifica para ver se os metadados foram alterados. (por exemplo, se o título ou url do artigo foi editado).

Esse token é assinado com seu `Site Key`, que foi fornecido a você pelo Gerente de conta técnico em Livefyre.

Consulte também:

* Documentos Oficiais CollectionMeta Token
* [Exemplo de lista](https://gist.github.com/pcolombo/dbbea020618c521a2bd5)

1. Crie um dicionário contendo os metadados da coleção. Vamos adicionar apenas alguns dos campos necessários nesta etapa, pois queremos criar uma soma de verificação desse objeto ANTES de adicionar a articleId.

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

   * **** *Título necessário*: O título da coleção, normalmente o título do artigo. O comprimento máximo é de 255 caracteres. Não suporta entidades html. Codifique caracteres especiais usando UTF-8.
   * **** *urlrequired*: O url canônico do seu artigo. Isso é usado pelos recursos de compartilhamento de comentários e sincronização social, além de links para seu artigo no Painel de administração. Se estiver testando localmente, observe que o Livefyre não aceitará &quot;localhost&quot; como um domínio.
   * **** *tags opcionais*: Uma lista separada por vírgulas de tags que você deseja adicionar à coleção no painel do Livefyre. As tags não podem conter espaços. Use sublinhados se desejar que um espaço apareça no painel de Administração.
   * **** *typeoptional*: Uma string que indica o tipo de coleção a ser criada. Os valores válidos são:

      * `reviews`
      * `sidenotes`
      * `ratings`
      * `counting`
      * `livecomments`
      * `liveblog`
      * `livechat`

      Se não especificado, uma coleção LiveComments é criada por padrão.


1. JSON codifica esse dicionário e gera uma soma de verificação md5.

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

1. Adicione o **articleId** ao Dicionário. O **checksum** não entra no token collectionMeta, mas deve ser enviado como um parâmetro separado no objeto js de conversãoConfig .

   ```
       meta.Add("articleId", "article-abcde00001"); 
   ```

   * **** *articleIdrequired*: Um identificador exclusivo para sua coleção no site Livefyre. Normalmente, o articleId exclusivo usado em seu CMS. (por exemplo, sua ID de publicação do WordPress) Esse valor nunca deve ser alterado. Livefyre identifica coleções exclusivas pela combinação de siteId e articleId.

1. Gere um token JWT assinado do dicionário, usando a chave do site fornecida a você pelo Livefyre. Observe que você deve especificar o algoritmo de hash correto, pois o pacote JWT não usa HS256 por padrão.

   ```
       string token = JWT.JsonWebToken.Encode(meta, siteSecret, JWT.JwtHashAlgorithm.HS256);
   ```

## O Token de Autenticação do Usuário {#section_g1d_43h_xz}

O Token de autenticação do usuário é usado para assinar um usuário no Livefyre. Quando um usuário entra em seu site, o site gera um Token de autenticação de usuário que é passado para o widget Livefyre na página. (Para obter mais informações sobre o processo de autenticação, consulte Perfis remotos.)

Esse token requer seu nome de rede (network.fyre.co) e é assinado com sua chave de rede, fornecida a você pelo seu gerente de conta técnica na Livefyre.

Consulte também:

* Documentação oficial do token de autenticação
* [Exemplo de lista](https://gist.github.com/pcolombo/7d7403172c28734c87e2)

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

   * **domínio:** o nome da sua rede (fornecido pelo Livefyre.) por exemplo mynetwork.fyre.co
   * **user_id:** a ID de usuário exclusiva para o usuário no sistema de perfil do site. Deve ser somente caracteres alfanuméricos (A-Z, a-z, 0-9). Se as IDs do usuário do seu sistema contiverem caracteres inválidos, considere enviar ao Livefyre um hash md5 da id de usuário ou uma versão codificada em base64 dela. (Informe o gerente da conta se fizer isso.)
   * **expira:** a data (em época) em que o token expira. Isso deve corresponder ao tempo de sessão dos logons no site, para que o estado de logon do Livefyre permaneça sincronizado com o estado de logon do site.
   * **display_name:** o nome de exibição do usuário em seu sistema de perfil, como deve ser exibido no fluxo de comentários.

1. Gere um token JWT assinado do dicionário, usando a Chave de rede fornecida a você pelo Livefyre. Observe que você deve especificar o algoritmo de hash correto, pois o pacote JWT não usa HS256 por padrão.

   ```
          string token = JWT.JsonWebToken.Encode(payload, networkKey, JWT.JwtHashAlgorithm.HS256);
   ```
