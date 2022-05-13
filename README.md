# servicoDeAgendamento

<h4 align="center"> 
	🚧 Em construção...  🚧
</h4>

<hr>

### Features

- [x] Cadastro de usuário
- [x] Validação de token
- [x] Login de usuário
- [x] Dados Pessoais
- [x] Soft-delete
- [x] Tratamento de exceções

### Pré-requisitos

Antes de começar, você vai precisar ter instalado em sua máquina as seguintes ferramentas:
[Git](https://git-scm.com), [Node.js](https://nodejs.org/en/), [npm](https://www.npmjs.com/) ou [yarn](https://yarnpkg.com/) e o [Docker](https://www.docker.com/). 
Além disto é bom ter um editor para trabalhar com o código como [VSCode](https://code.visualstudio.com/)

### Como usar

# Clone este repositório
$ git clone https://github.com/Andreferraz20

# Acesse a pasta do projeto (com o VSCode instalado)
Com o botão direito clique em "Abrir com code"<br>
ou <br>
Abra o vscode > Open Folder > Procure a pasta > Clique em open folder

# Instale as dependências
```
npm install
```
ou
```
yarn install
```

# Criar e executar os containers

```
docker-compose up
```

# Rode as migrations

```
yarn typeorm migration:run
```

## O servidor inciará na porta:3333

# Rotas

## Cadastro do usuário (post)
``` 
/signup
```
### Body
```
{
	"name": "teste",
	"email": "teste@gmail.com",
	"password": "teste2",
	"cpf": "1234",
	"birthdate": "01/01/2000",
	"phone": "9999999" ,
	"address": "Rua x numero y"
}
```

## Criando sessão/login (post)
```
/signin
```
### body 
``` 
{
	"email": "teste@gmail.com",
	"password": "teste2"
}
```
### Response
```
{
	"token": "Token Gerado pelo jwt",
	"user": {
		"email": "teste@gmail.com"
	}
}
```
## Dados Pessoais (get)

```
/me
```
Gerar token na rota de login e passar o bearer token

### Response
```
{
	"name": "teste",
	"email": "teste@gmail.com",
	"cpf": "1234",
	"birthdate": "01/01/2000",
	"phone": "9999999",
	"address": "Rua x numero y"
}
```

## Delete (delete)
Precisa ter sessão ativa e passar o bearer token
```
/me
```

### 🛠 Tecnologias

As seguintes ferramentas foram usadas na construção do projeto:
- [Node.js](https://nodejs.org/en/)
- Express
- [TypeScript](https://www.typescriptlang.org/)
- [Docker](https://www.docker.com/)
- [Jwt](https://jwt.io/)
- [TypeOrm](https://typeorm.io/#/)


<img src="https://img.shields.io/badge/license-MIT-blue">


