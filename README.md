# Projeto `Manutenção e Evolução de Software`

## Equipe 3

- Anthony Kauã
- Carlos Souza
- David Daniel
- Esther Santos
- Rafael Kanda
- Saile Santos
- Vitória Beatriz

## Stack

1. FrontEnd: Handlebars + BootStrap + TypeScript
2. BackEnd: Spring Boot + MySQL (+ Docker)

## Docs do FrontEnd

### 1. Pré-Requisitos:

```
Git, 
Node.js, 
IDE/Editor de Código (preferência ao VS Code)
```

### 2. Como executar:

1. Instalar pacotes NPM: `$ npm install`
2. Gerar arquivo `.env` (analisar `.env.example`)
3. Rodar aplicação: `$ npm run start`

## Docs do BackEnd

### 1. Pré-Requisitos: 

```
Git, 
Java (JDK) v17 (ou superior),
MySQL (preferência ao XAMPP),
IDE/Editor de Código (preferência ao VS Code),
Java Extension Pack (no VS Code)
```

### 2. Como executar:

1. Inicialize os módulos 'Apache' e 'MySQL' do XAMPP (ou configure o MySQL em outras ferramentas - MySQL Community Edition)
2. Crie um banco de dados no "http://localhost/phpmyadmin/index.php" (com o nome 'mes_db')
3. Tendo configurado o DB, inicialize a aplicação Spring com o botão 'Run'

### 3. Rotas a serem utilizadas

1 - (**POST**) "http://localhost:8080/user"

Entrada:

```json
{
  "nome": "Carlos Souza",
  "login": "Carlitos",
  "email": "email-test@email.org.com",
  "senha": "admin123"
}
```

Saída:

```json
{
    "id": 1,
    "status": 1,
    "menssage": "Usuário incluído com sucesso..."
}
```

2 - (**GET**) "http://localhost:8080/user/list"

Saída:

```json
[
  {
    "id": 1,
    "nome": "Carlos",
    "login": "Carlitos",
    "email": "email-carlos@email.com"
  },
]
```

3 - (**GET**) "http://localhost:8080/user/1"

Saída:

```json
{
  "id": 1,
  "nome": "Carlos",
  "login": "Carlitos",
  "email": "email-carlos@email.com"
}
```

4 - (**DEL**) "http://localhost:8080/user/1"

Saída:

```json
{
  "id": 1,
  "status": 1,
  "menssage": "Usuário deletado com sucesso..."
}
```

5 - (**POST**) "http://localhost:8080/user/validarLogin/Carlitos/carlos-pwd"

Saída:

```json
{
    "id": 1,
    "nome": "Carlos Souza",
    "login": "Carlitos",
    "email": "email-test@email.org.com"
}
```

6 - (**GET**) "http://localhost:8080/user/search/Carlos Souza"

Saída:

```json
[
  {
    "id": 1,
    "nome": "Carlos Souza",
    "login": "Carlitos",
    "email": "email-test@email.org.com"
  }
]
```
