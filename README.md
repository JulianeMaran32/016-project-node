# API with Nodejs, express and MongoDB  

**Criando API em Node:**        
1. Instalar o NodeJS     
2. Criar uma pasta no local que deseja implementar o projeto    
3. Abrir a pasta no prompet de comando (CMD), insira o comando: `npm init` para inicializar     

```bash

# inicializando o projeto
npm init 

# inserir informações a baixo (opcionais)
package name: (api-nodejs-express-mongodb) api-nodejs
version: (1.0.0)    # inserir a versão
description: API com NodeJS + Express + MongoDB  # descrição
entry point: (index.js) app.js # arquivo.js que será inicializado 
test command: # comandos de teste
git repository: https://github.com/JulianeMaran32/016-project-node.git # repositório git
keywords: api nodejs mongodb # palavra chave
author: Juliane Maran
license: (ISC)  

Is this OK? (yes) yes

# as informações acima serão inseridas no arquivo package.json

# verifica os arquivos que estão dentro da pasta
dir 

```

mongodb = mongodb+srv://julianemaran:<password>@cluster0.ad0lk.mongodb.net/myFirstDatabase?retryWrites=true&w=majority

## Commands   

```powershell
node -v
npm init  
dir

npm install express --save
npm install mongoose --save
npm install body-parser --save
npm install bcrypt --save
npm install jsonwebtoken --save

node app.js
```

## create    

| URL                         | Method |  
|:----------------------------|:-------|  
| localhost:3000/users/create | POST   |   

### Request body    

```json
{
    "email": "teste@email.com",
    "password": "123456"
}
```

### Response   

```json

```

## Deprecated

app.js

```js
const url = config.bd_string;
const opcoes = { 
    reconnectTries: Number.MAX_VALUE, 
    reconnectInterval: 500, 
    poolSize: 5,
     useNewUrlParser: true 
};

mongoose.connect(url, opcoes);
mongoose.set('useCreateIndex', true);
```

Substituir onde consta: <password>

## Links   

[mongoose](https://mongoosejs.com/)  
[npm](https://www.npmjs.com/)   


## Status Code   

| Status | Description           | Observações                                                    |
|:-------|:----------------------|:---------------------------------------------------------------|   
| 200    | OK                    | Sucesso                                                        |
| 201    | Created               |                                                                |
| 202    | Accepted              |                                                                |
| 400    | Bad request           |                                                                |
| 401    | Unauthorized          | Autenticação, tem caráter temporário                           |   
| 403    | Forbidden             | Autenticação, tem caráter permanente                           |    
| 404    | Not found             |                                                                |
| 500    | Internal server error |                                                                |
| 501    | Not implemented       | a API não suporta essa funcionalidade                          |  
| 502    | Service Unavailable   | a API executa essa operação, mas no momento está indisponvível |  

