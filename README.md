# Clean Architecture Full Cycle

## Execução da Aplicação

Você pode executar a aplicação facilmente. Para isso, precisamos subir um docker com o banco de dados e rabbitmq:


```bash
docker-compose up -d
``` 

Após os containeres estarem de pé, basta você executar os comandos abaixo:


```bash
go mod tidy

make migrate

go run main.go
``` 