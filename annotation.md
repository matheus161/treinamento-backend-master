//Endpoint
//Rotas
// localhost:3333/api/v1/
// localhost:3333/api/v1

//Recurso
// localhost:3333/api/v1/user

// Verbos HTTP
// GET
// POST
// PUT
// PATCH
// DELETE

// Parametros da Requisição

// Resquest Param
// Resquest Body
// Resquest Query

// MongoDB
// Mongoose

// Modulo de Usuario

// localhost:3333/api/v1/users - GET - Todos os usuarios - index
// localhost:3333/api/v1/users - POST - Criar os usuarios - store
// localhost:3333/api/v1/users/:id - PUT - Atualizar os usuarios - update
// localhost:3333/api/v1/users/:id - DELETE - Deletar os usuarios - delete
// localhost:3333/api/v1/users/:id - GET - Retornar um usuarios - show

// nome
// email
// senha

// MiddleWare de validação, antes de passar a rota ele verifica os dados
// npm install celebrate
// npm install helmet 
// npm install express-rate-limit
// npm install express-slow-down
// npm install swagger-ui-express


// INICIANDO SERVIDOR DE TESTS NO DOCKER 
docker run --name mongooseTreinamento -e MONGO_INITDB_ROOT_USERNAME=root -e MONGO_INITDB_ROOT_PASSWORD=example -e MONGO_INITDB_DATABASE=treinamento -p 27017:27017 -d mongo
docker run --name adminerTreinamento -p 8081:8081 --link mongooseTreinamento:mongo -d mongo-exxpress

// PARA INICIAR TUDO DE UMA VEZ, INCLUINDO API 
docker-compose up -d 


### Desafios

1. Criar um CRUD de Books (Básico)
   1. Pelo menos conter 3 dados
2. Construir Relacionamento entre User e Books (Intermediario)
   1. Dica Modificar o Model
3. Modificar a rota de Show(User e Books) para retornar os dados desse relacionamento (Avançado)
4. Criar um novo Controller, criar um método retorna o book e seu usuário e o outro método retorna o usuário e os seus livros
5. Retornar o id pelo token na rota show

// aggregate $match - coloca nesse campo o id

// Não consegui cadastrar o book junto do usuário (Estava repetindo o id do book para novos usuários)
// Deixei o book no Schema de user, pois não consegui puxar sem ele (Eu não consigo guardar os ids de book)
// Ao atualizar o book eu consigo colocar dois id's de user, mas não deveria 

// docker-compose up -d