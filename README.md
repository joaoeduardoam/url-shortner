# Projeto de Estudo AWS S3, Lambda e API Gateway com Spring Boot

Aplicação serverless com Java e Maven para  redirecionamento de urls. Realizado a integração com AWS S3 para
criação e gerenciamento de buckets, exposição de endpoints via API Gateway, uso de AWS Lambda para 
processamento serverless, e manipulação de dados em JSON com Jackson.

## Estrutura do Projeto

O projeto trata-se de um sistema de encurtamento de URLs utilizando a AWS como
infraestrutura serverless. O objetivo é permitir que os usuários criem URLs curtas que
redirecionem para URLs originais, com um tempo de expiração configurável. O sistema é
composto por duas funções Lambda: a primeira função é responsável por gerar e armazenar os
URLs encurtados; a segunda função gerencia o redirecionamento do link.


![image](https://github.com/user-attachments/assets/43600f31-dd31-4050-80c4-3765ab9891e4)


### Primeira Função Lambda - Encurtador de URL **(repositório atual)**
  - Responsável por gerar e armazenar os links encurtados em um bucket S3, junto com informações
como a URL original e o tempo de expiração

### Segunda Função Lambda - Redirecionador de URL https://github.com/joaoeduardoam/redirect-url-shortener
  - Gerencia o redirecionamento, verificando o código da URL curta e validando se a URL ainda
está dentro do prazo de expiração antes de redirecionar o usuário.



  ## Tecnologias Utilizadas:
- Java : Linguagem de programação principal.
- Spring Boot: Framework para criação de aplicações Java, facilitando a configuração e a implementação de APIs.
