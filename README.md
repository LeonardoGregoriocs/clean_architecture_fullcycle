# Clean Architecture Full Cycle

## Execução da Aplicação

1. Subir os Containers Docker:
    Inicialize os containers Docker que contêm o banco de dados e o RabbitMQ usando o seguinte comando:
    
    ```bash
    docker-compose up -d
    ```

2. Preparar o Ambiente:
    Após os containers estarem em execução, execute os seguintes comandos para configurar o ambiente:
    
     ```bash
    go mod tidy
    make migrate
    ```
3. Executar a Aplicação:
    Por fim, inicie a aplicação executando o seguinte comando:
    
     ```bash
    go run main.go
    ```

4. Aqui estão as portas disponíveis e os respectivos serviços associados:

### GraphQL:
    Porta: 8080
    Descrição: Esta porta é usada para acessar o servidor GraphQL, que oferece consultas e mutações para interagir com a aplicação de forma flexível e eficiente.
  
### Banco de Dados MySQL:
    Porta: 3306
    Descrição: Esta porta é usada para se comunicar com o banco de dados MySQL, que armazena e gerencia os dados da aplicação.

### gRPC (Remote Procedure Call):
    Porta: 50051
    Descrição: Esta porta é usada para comunicação RPC entre os serviços da aplicação, proporcionando uma forma eficiente e padronizada de interação entre componentes distribuídos.
  
### API REST:
    Porta: 8000
    Descrição: Esta porta é usada para acessar a API REST da aplicação, que fornece pontos de extremidade HTTP para realizar operações CRUD (Create, Read, Update, Delete) nos recursos da aplicação.
