# n8n-keep-memory-postgresql

## Create postgres command.
docker run 
  --name postgres_container 
  --network ollama-network 
  --volume postgres_data:/var/lib/postgresql/data 
  -e POSTGRES_USER=myuser 
  -e POSTGRES_PASSWORD=mypassword 
  -e POSTGRES_DB=mydatabase 
  -d 
  -p 5432:5432 
  postgres:17.5

  ## Create Postgress admin Command
  docker run -d 
  --name pgadmin_container 
  --network ollama-network 
  -e PGADMIN_DEFAULT_EMAIL=admin@example.com 
  -e PGADMIN_DEFAULT_PASSWORD=mypassword 
  -p 8080:80 
  dpage/pgadmin4

<img width="1390" height="583" alt="image" src="https://github.com/user-attachments/assets/caf1c4d9-ccc6-4096-bc7c-6e09e8e75a49" />

