# Utilizando o Docker Compose

O Docker-Compose é uma ferramenta para definir e executar aplicativos Docker multi-contêiner com facilidade. Ele permite que você defina todos os serviços, redes e volumes em um arquivo docker-compose.yml.

1. **Criar e iniciar contêineres em segundo plano:** 

```bash
docker compose up -d # Execute o comando dentro do diretório que está o arquivo docker-compose.yaml para iniciar a stack
``` 
3. **Parar e remover contêineres criados pelo compose:** 

```bash
docker compose down
``` 
4. **Listar Contêineres:** 

```bash
docker container ps
``` 
5. **Ver Logs dos Contêineres:** 

```bash
docker container logs -f id_do_container
``` 

