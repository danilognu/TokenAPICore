<!-- ABOUT THE PROJECT -->
## PROJETO GERANDO TOKEN

Criando Migrations.
* dotnet
```sh
dotnet ef migrations add sistema_login
dotnet ef database update sistema_login
```
# Gerando Token

Utilizando Postman ou programa similar

Criando usuario para teste 

Adicionar o seguinte endereço para chamar a API 
```html
https://localhost:44347/api/usuarios/criar
```

Adiconar o seguinte paramentro no Boby (raw) arquivo JSON

```js
{
   "email" : "teste@teste.com",
   "password" :  "Senha#123456"
}
```

Será gerado o **TOKEN** da seguinte formar:

```JSON
{
    "token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ1bmlxdWVfbmFtZSI6ImRhbmlsb0BlbWFpbC5jb20iLCJtZXVWYWxvciI6Im9xdWUgdm9jZSBxdWlzZXIiLCJqdGkiOiI0OWIwMzhhNy1hZWQyLTQ4M2UtYTk5Yi0zOWUyZDlkNTgyNWQiLCJleHAiOjE1Nzg2NTk5OTZ9.iOpVoyo4ZG4eI1WWiiOlLLUjgDyxv_wP_mRj742L7HY",
    "expiration": "2020-01-10T12:39:56.0918867Z"
}
```

Após o **TOKEN** gerado vamos fazer o login

Adicionar o seguinte caminho para a API

```html
https://localhost:44347/api/usuarios/login
```

Onde vamos fazer o Login na API 

Adiconar o seguinte paramentro no Boby (raw) arquivo JSON

```js
{
   "email" : "teste@teste.com",
   "password" :  "Senha#123456"
}
```

Será gerado um **TOKEN** onde esta definido ao acesso 

Copie o **TOKEN** e acesse o segunte endereço

```html
https://localhost:44347/api/values
```

No campo Authorization selecionar o campo Bearer Token copie o Token gerado e cole no campo Exemplo

```JSON
"eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ1bmlxdWVfbmFtZSI6ImRhbmlsb0BlbWFpbC5jb20iLCJtZXVWYWxvciI6Im9xdWUgdm9jZSBxdWlzZXIiLCJqdGkiOiI0OWIwMzhhNy1hZWQyLTQ4M2UtYTk5Yi0zOWUyZDlkNTgyNWQiLCJleHAiOjE1Nzg2NTk5OTZ9.iOpVoyo4ZG4eI1WWiiOlLLUjgDyxv_wP_mRj742L7HY"
```

Pronto esta autenticado na API
