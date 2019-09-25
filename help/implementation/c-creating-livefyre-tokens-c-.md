---
description: Saiba como gerar tokens Livefyre usando a linguagem C#.
seo-description: Saiba como gerar tokens Livefyre usando a linguagem C#.
seo-title: Criando Tokens Livefyre `C#'
solution: Experience Manager
title: Criando Tokens Livefyre `C#'
uuid: c5e05625-8550-4b51-9211-134600e20ec7
translation-type: tm+mt
source-git-commit: 74a63daa264014af9a8afb6639fa1561a7b83241

---


# Creating Livefyre Tokens C\# {#creating-livefyre-tokens-c}

Saiba mais sobre como gerar tokens do Livefyre usando a linguagem ``C#``.

Você pode aproveitar a documentação herdada e o código de amostra para usar `C#.NET` para gravar métodos para criar tokens.

Para fazer referência às bibliotecas oficiais do Livefyre, use a Biblioteca [do](https://github.com/Livefyre/livefyre-java-utils) Java como ponto de partida para `C#` desenvolvedores.

Você também pode considerar o uso da Biblioteca [do](https://github.com/Livefyre/livefyre-nodejs-utils) Node.js na linha de comando para gerar tokens de referência para você mesmo e familiarizar-se com a estrutura do método.

* [Ir para o Meta Token da coleção](https://gist.github.com/gibron/56cb9c7060bf4816c4c5#the-collectionMeta-token)
* [Ir para o token de autenticação](https://gist.github.com/gibron/56cb9c7060bf4816c4c5#the-auth-token)

## Dependências {#section_c15_fnh_xz}

* Você precisará do pacote [](https://www.nuget.org/packages/JWT) JWT nuget em seu projeto para gerar os tokens.
* As amostras de código nesta página usam o pacote JSON [Newtonsoft](https://www.nuget.org/packages/newtonsoft.json/) .

## CollectionMeta Token {#section_dzt_4mh_xz}

O CollectionMeta Token é passado para o Livefyre quando você incorpora Comentários em uma página e fornece ao nosso sistema os metadados necessários para a sua nova coleção. Além disso, você criará um MD5 `checksum` desses dados, que o Livefyre verifica se os metadados foram alterados. (por exemplo, se o título ou url do artigo foi editado).

Este token foi assinado com o seu `Site Key`, que lhe foi fornecido pelo seu Gerente de Conta Técnico em Livefyre.

Consulte também:

* CollectionMeta Token Docs oficiais
* [Gist de exemplo](https://gist.github.com/pcolombo/dbbea020618c521a2bd5)

1. Crie um Dicionário que contenha os metadados da coleção. Vamos adicionar apenas alguns dos campos necessários nesta etapa, pois queremos criar uma soma de verificação desse objeto ANTES de adicionarmos a articleId.

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

   * **título** *obrigatório*:  O título da coleção, geralmente o título do artigo. O comprimento máximo é de 255 caracteres. Não suporta entidades html. Codifique caracteres especiais usando UTF-8.
   * **url** *obrigatório*:  O url canônico do seu artigo. Isso é usado pelos recursos de compartilhamento de comentários e sincronização social, além de links para seu artigo no painel Admin. Se estiver testando localmente, observe que Livefyre não aceitará ‘localhost’ como um domínio.
   * **tags** *opcionais*:  Uma lista separada por vírgulas de tags que você deseja adicionar à coleção no painel Livefyre. As tags não podem conter espaços. Use sublinhados se desejar que um espaço apareça no painel Admin.
   * **tipo** *opcional*:  Uma string que indica que tipo de coleção deve ser criada. Os valores válidos são:

      * `reviews`
      * `sidenotes`
      * `ratings`
      * `counting`
      * `livecomments`
      * `liveblog`
      * `livechat`
      Se não for especificado, uma coleção LiveComments será criada por padrão.


1. O JSON codifica este dicionário e gera uma soma de verificação md5.

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

1. Adicione **articleId** ao dicionário. A **soma** de verificação não entra no collectionMeta token, mas deve ser enviada como um parâmetro separado no objeto js de consoleConfig.

   ```
       meta.Add("articleId", "article-abcde00001"); 
   ```

   * **articleId** *obrigatório*:  Um identificador exclusivo para sua coleção no site do Livefyre. Normalmente, o articleId exclusivo usado no CMS. (por exemplo, sua ID de publicação do WordPress) Esse valor nunca deve ser alterado. Livefyre identifica coleções exclusivas pela combinação de siteId e articleId.

1. Gere um token JWT assinado do dicionário, usando a chave do site fornecida a você pelo Livefyre. Observe que você deve especificar o algoritmo hash correto, pois o pacote JWT não usa HS256 por padrão.

   ```
       string token = JWT.JsonWebToken.Encode(meta, siteSecret, JWT.JwtHashAlgorithm.HS256);
   ```

## O token de autenticação do usuário {#section_g1d_43h_xz}

O token de autenticação do usuário é usado para assinar um usuário no Livefyre. Quando um usuário entra em seu site, o site gera um Token de autenticação de usuário que é passado para o widget Livefyre na página. (Para obter mais informações sobre o processo de autenticação, consulte Perfis remotos.)

Este token requer seu nome de rede (network.fyre.co) e é assinado com sua chave de rede, fornecida a você pelo seu gerente técnico de conta no Livefyre.

Consulte também:

* Documentos oficiais do token de autenticação
* [Gist de exemplo](https://gist.github.com/pcolombo/7d7403172c28734c87e2)

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

   * **** domínio: O nome da sua rede (fornecido pelo Livefyre.) por exemplo, mynetwork.fyre.co
   * **** user_id: A ID de usuário exclusiva para o usuário no sistema de perfil do site. Deve ser somente caracteres alfanuméricos (A-Z, a-z, 0-9). Se as IDs de usuário do seu sistema contiverem caracteres inválidos, considere enviar o Livefyre um hash md5 da ID de usuário ou uma versão codificada base64. (Informe o seu gerente de conta se você fizer isso.)
   * **** expira: A data (em época) em que o token expira. Isso deve corresponder ao tempo de sessão dos logons em seu site, para que o estado de logon do Livefyre permaneça sincronizado com o estado de logon do site.
   * **** display_name: O nome de exibição do usuário no seu sistema de perfil, como deve ser exibido no fluxo de comentários.

1. Gere um token JWT assinado do dicionário, usando a chave de rede fornecida a você pelo Livefyre. Observe que você deve especificar o algoritmo hash correto, pois o pacote JWT não usa HS256 por padrão.

   ```
          string token = JWT.JsonWebToken.Encode(payload, networkKey, JWT.JwtHashAlgorithm.HS256);
   ```
