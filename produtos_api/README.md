API-PRODUTOS

API REST desenvolvida para gerenciamento de produtos, permitindo cadastrar, consultar, alterar e excluir registros. O projeto utiliza Node.js, Express e MongoDB, com o Mongoose responsável pela comunicação com o banco de dados.

Tecnologias utilizadas
Node.js
Express 5
MongoDB com Mongoose
dotenv para configuração das variáveis de ambiente
nodemon para reinicialização automática durante o desenvolvimento
Requisitos

Antes de iniciar, certifique-se de ter:

Node.js instalado, preferencialmente na versão 18 ou mais recente
Um banco MongoDB disponível para conexão, podendo ser:
uma instância hospedada no MongoDB Atlas
um servidor MongoDB executado localmente
Executando a aplicação
1. Baixe o projeto
git clone <url-do-repositorio>
cd API-PRODUTOS

2. Instale os pacotes

Dentro da pasta do projeto, execute:

npm install

3. Defina as configurações do ambiente

Utilize o arquivo .env.example para criar seu arquivo .env:

cp .env.example .env


Em seguida, informe os dados necessários para conexão com o MongoDB:

DB_CONNECTION_STRING=sua_string_de_conexao_do_mongodb
PORT=8000


⚠️ Não compartilhe nem envie o arquivo .env para o repositório. Ele já deve estar protegido pelo .gitignore. Cada ambiente precisa utilizar suas próprias configurações e credenciais.

4. Inicie o servidor

Para executar a aplicação em modo de desenvolvimento:

npm run dev


Uma inicialização bem-sucedida deverá apresentar mensagens semelhantes a:

servidor escutando!
Conexão realizada com sucesso!


Por padrão, a API poderá ser acessada através de:

http://localhost:8000


Caso outra porta seja informada na variável PORT, o endereço deverá ser ajustado de acordo com essa configuração.

Rotas disponíveis
Método	Endpoint	Função
GET	/	Verifica o funcionamento da API
GET	/produtos	Retorna os produtos cadastrados
GET	/produtos?nome=	Realiza uma busca por nome
GET	/produtos/:id	Obtém um produto específico
POST	/produtos	Adiciona um novo produto
PUT	/produtos/:id	Modifica os dados de um produto
DELETE	/produtos/:id	Exclui um produto
Dados enviados no POST e PUT

Para inserir ou alterar um produto, o corpo da requisição deve seguir este formato:

{
  "nome": "Caneta",
  "preco": 2.5,
  "quantidade": 100
}

Respostas HTTP

A aplicação utiliza os seguintes códigos para indicar o resultado das requisições:

200 — operação concluída corretamente
201 — novo produto registrado
400 — informações enviadas são inválidas ou o ID possui formato incorreto
404 — registro solicitado não existe
500 — ocorreu um problema no servidor
Organização dos arquivos
API-PRODUTOS/
├── server.js                        # arquivo responsável por iniciar a aplicação
├── src/
│   ├── app.js                       # configura o Express e a aplicação
│   ├── config/
│   │   └── dbConnect.js             # responsável pela conexão com o MongoDB
│   ├── controllers/
│   │   └── produtosController.js    # controla as operações relacionadas aos produtos
│   ├── models/
│   │   └── Produto.js               # definição do modelo de produto
│   └── routes/
│       ├── index.js                 # reúne as rotas da aplicação
│       └── produtosRoutes.js        # endpoints relacionados aos produtos
├── .env.example                     # exemplo das configurações necessárias
└── package.json                     # dependências e scripts do projeto