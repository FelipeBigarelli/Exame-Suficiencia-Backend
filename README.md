# Instalação do APP
**1:** Clone o repositório https://github.com/FelipeBigarelli/Exame-Suficiencia-Backend.git

**2:** Entre no projeto e instale as dependências de acordo com seu gerenciador de pacotes
  - yarn install
  - npm install

**3:** Configure o container do docker do banco de dados
  - docker run --name backend -p 3306:3306 -e MYSQL_ROOT_PASSWORD=1234 -d mysql

**4:** Verifique se a instância 'backend' foi criada
  - docker ps OU docker ps -a
  - Caso não tenha iniciado, execute o comando:
    - docker start backend

**5:** Conecte ao MySQL Container
  - docker exec -it backend mysql -uroot -p

**6:** Crie o database
  - CREATE DATABASE backend;

**7:** Execute a aplicação
  - yarn dev

**8:** No Postman ou Dbeaver, conecte ao database da aplicação com as configurações contidas no arquivo src/shared/database/index.js

**9:** Crie e execute a rota de criação de tabelas do banco de dados
  - POST: http://localhost:3000/models

