- 2 micro-serviços (gRPC)

-> User (credenciais, todas as outras informações) - ADONIS
routeamento
models

-> Purchases user_id ou Compras user_id - gRPC (server)

API REST -> Express (/users, /purchases) - gRPC (client)

/purchases/:user_id

requisição
POST api.auth0.com -> (email, name, username, password) -> REST 2s
express

axis.post('api.auth0.com' ...) JSON {}

requisição
api.auth0.com:500121 -> createUser(email, name, username, password) ->
0.4s

express
grpc.client.createUser( ... ) BUFF {} -> contrato
