My Bank API
Esta é uma API simples para um sistema bancário que permite gerenciar contas bancárias. A API utiliza Node.js e o framework Express.js.

O código é uma aplicação de API RESTful desenvolvida em Node.js usando o framework Express. Ele define um servidor web que escuta na porta 3000 e gerencia recursos de contas bancárias usando HTTP verbs (GET, POST, PUT, DELETE) para acessar o banco de dados de contas armazenado em um arquivo JSON.

O código usa o pacote de logging Winston para registrar informações de depuração, bem como o pacote Cors para permitir solicitações de origens diferentes e o pacote swagger-ui-express para documentar a API com um arquivo Swagger JSON.

Além disso, o código define um middleware de autorização usando o pacote express-basic-auth, permitindo que apenas usuários autorizados acessem recursos protegidos. O middleware de autorização verifica se o usuário tem as permissões necessárias para acessar um recurso específico.

Se o arquivo de banco de dados de contas não existir, o código cria um arquivo JSON inicial com um objeto vazio de contas. Se o arquivo já existir, o código lê seu conteúdo e inicia a API.

Em resumo, este código é um servidor de API RESTful que gerencia recursos de conta bancária, com recursos de autenticação e autorização, documentação de API e logging.
Dependências
As seguintes dependências são necessárias para executar esta API:

Express.js
Winston
Módulo de sistema de arquivos (fs) do Node.js
CORS
Swagger UI Express
Express Basic Auth
Iniciando
Para começar a usar esta API, siga estes passos:

Clone o repositório em sua máquina local.
Execute o comando npm install para instalar as dependências necessárias.
Execute o comando npm start para iniciar o servidor.
Endpoints
Atualmente, a API possui os seguintes endpoints:

/doc
Este endpoint serve a interface do usuário do Swagger UI, que permite explorar os endpoints da API.

/account
Este endpoint permite gerenciar contas bancárias. Os seguintes métodos HTTP são suportados:

GET /account - retorna uma lista de todas as contas
GET /account/:id - retorna a conta com o id especificado
POST /account - cria uma nova conta
DELETE /account/:id - exclui a conta com o id especificado
PUT /account - atualiza uma conta existente
Autenticação
Para acessar o endpoint /account, o usuário deve estar autenticado. Atualmente, dois usuários são suportados:

admin com senha admin
fabricio com senha 1234
Logs
A API utiliza o Winston para logging. Os logs são escritos tanto no console quanto em um arquivo de log chamado my-bank-api.log.

Tratamento de erros
Se o arquivo accounts.json não for encontrado quando o servidor iniciar, a API tentará criar o arquivo com um objeto JSON inicial.

Licença
Esta API é lançada sob a Licença MIT.
