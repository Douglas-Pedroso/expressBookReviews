📚 Express Book Reviews

Express Book Reviews é uma aplicação web backend construída com Node.js e Express.js para gerenciar livros e avaliações (reviews).
Este projeto é inspirado no final project do curso de desenvolvimento backend usando Express.js, fornecido pelo IBM Developer Skills Network.

Ele oferece uma API REST simples para visualizar livros, registrar usuários, autenticar sessões, e permitir que usuários façam, editem ou excluam avaliações de livros.

🧠 Visão Geral

Express Book Reviews é uma API server-side que permite:

📘 Listar livros disponíveis

🔍 Buscar livros por ISBN, título ou autor

👤 Registrar e autenticar usuários

✍️ Criar, modificar e remover avaliações de livros

Ela utiliza o framework Express.js, um dos frameworks web mais populares para Node.js.

🚀 Tecnologias

✔️ Node.js
✔️ Express.js
✔️ JSON para persistência de dados simples
✔️ JWT (JSON Web Tokens) para autenticação (se implementado)
✔️ Middleware para rotas autenticadas

📁 Estrutura do Projeto (exemplo)
expressBookReviews/
├── final_project/
│   ├── index.js               # Servidor principal
│   ├── package.json
│   ├── router/
│   │   ├── general.js         # Rotas públicas
│   │   └── auth_users.js      # Rotas autenticadas
├── .gitignore
├── LICENSE
└── README.md


O nome e a estrutura podem variar um pouco conforme sua versão, mas em geral seguem este padrão.

📥 Instalação

Clone o repositório:

git clone https://github.com/Douglas-Pedroso/expressBookReviews
cd expressBookReviews


Instale as dependências:

npm install

▶️ Executando a Aplicação

Para iniciar o servidor em modo de desenvolvimento:

npm start


ou, se você tiver o nodemon instalado:

nodemon final_project/index.js


Depois disso, o servidor normalmente ficará disponível em:

http://localhost:3000


(Verifique o PORT configurado no package.json ou index.js.)

📌 Endpoints Principais (Exemplos)

Os endpoints podem variar conforme implementação final do código.

🔓 Rotas Públicas
Verbo	Rota	Descrição
GET	/books	Lista todos os livros
GET	/books/:isbn	Detalhes de um livro por ISBN
GET	/books/author/:name	Busca livros por autor
GET	/books/title/:name	Busca livros por título
🔒 Rotas Autenticadas
Verbo	Rota	Descrição
POST	/register	Registrar novo usuário
POST	/login	Login do usuário
POST	/books/:isbn/review	Adicionar/modificar avaliação
DELETE	/books/:isbn/review	Excluir avaliação do usuário atual

Dependendo da implementação, alguns detalhes podem mudar — por exemplo, o uso de JWT ou sessões.

🧪 Teste da API

Você pode testar usando ferramentas como:

Postman

Insomnia

curl

Exemplo de requisição:

curl http://localhost:3000/books

📜 Licença

Este projeto está sob a Apache-2.0 License (a mesma usada pelo projeto original).

🎯 Próximos Passos / Melhorias

✨ Adicionar uma interface frontend (React, Next.js etc.)
✨ Persistência em banco de dados real (MongoDB, PostgreSQL)
✨ Autenticação completa com JWT
✨ Documentação API com Swagger
