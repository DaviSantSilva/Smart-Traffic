### Documentação de Instalação e Uso do Projeto

#### Clonando o Repositório

1. Clone o repositório.
2. Certifique-se de ter Maven, Oracle Data Base, Oracle SQL Developer e Java instalados em sua máquina.
3. Configure o arquivo `application.yml` de acordo com suas especificações, como mostrado no exemplo abaixo:
   - `username:`
   - `password:`

#### Utilizando Docker

1. Clone o repositório.
2. Navegue até a pasta `Smart_Traffic`.
3. Abra o Git Bash e execute o comando:
   ```sh
   mvn clean package -D --skipTests
   ```
4. Retorne à pasta raiz do projeto.
5. Abra o PowerShell e utilize o comando:
   ```sh
   cd {caminho_para_a_pasta_raiz_do_projeto}
   ```
6. Execute o comando:
   ```sh
   docker compose up -d --build
   ```
7. Aguarde o banco de dados iniciar completamente.
8. Certifique-se de que a imagem do banco de dados foi iniciada corretamente.
9. Inicialize a aplicação pelo Docker Desktop.

#### Acessando a Documentação do Projeto

Após a inicialização completa do projeto, utilize o endereço `http://localhost:8080/swagger-ui/index.html#/` no navegador de sua preferência para acessar a documentação do projeto.

**Importante:** Para utilizar corretamente todas as rotas do projeto, é necessário um Bearer Token que deve ser passado no header da requisição. Para isso:
1. Cadastre um usuário.
2. Faça login para receber seu token.
3. Utilize o token fornecido para acessar as outras rotas do projeto.
