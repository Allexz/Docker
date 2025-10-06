# Docker
## Treinamento Docker (Udemy - Argus Academy)

**Conceitos Fundamentais do Docker:**

- **Container**: Unidade leve e isolada que executa uma aplicação e suas dependências, baseada em uma imagem.
- **Imagem**: Pacote imutável com código, bibliotecas, configurações e dependências para criar containers.
- **Dockerfile**: Script com instruções para construir uma imagem Docker.
- **Repositório/Registry**: Armazena imagens Docker (ex.: Docker Hub).
- **Docker Engine**: Motor que executa e gerencia containers, composto por CLI, API e runtime.
- **Isolamento**: Containers usam namespaces e cgroups do Linux para isolar processos, rede e sistema de arquivos.
- **Portabilidade**: Containers rodam consistentemente em diferentes ambientes (local, nuvem, etc.).
- **Composição**: Uso de `docker-compose` para definir e gerenciar múltiplos containers (serviços, redes, volumes).
- **Volume**: Persistência de dados fora do ciclo de vida do container.
- **Rede**: Conexão entre containers, com modos como bridge, host ou overlay.

# Comandos básicos  
Repositório (Registry) oficial do Docker - **https://hub.docker.com/**
1. **docker pull <<image:tag>>**  (Resgata a imagem do repositório (Registry)
Exemplo:     **docker pull mcr.microsoft.com/mssql/server:2022-latest**  
2. **docker ps --all / docker ps -a** (lista todos os contêiners)  
Obs.: **docker ps** (lista somente os contêineres em execução)    
3. **docker run -e "ACCEPT_EULA=Y" -e "MSSQL_SA_PASSWORD=SuaSenhaForte123" -p 1433:1433 --name sqlserver -d mcr.microsoft.com/mssql/server:2022-latest**  
   3.1 -e "ACCEPT_EULA=Y" - aceitação dos termos de licença do SQL Server  
   3.2 -e "MSSQL_SA_PASSWORD=SuaSenhaForte123" - define a senha para o usuário SA  
   3.3 -p 1433:1433 - mapeia a porta 1433 do contêiner para a 1433 do HOST  
   3.4 --name sqlserver - nomeia o contêiner  
   3.5 -d - executa o contêiner em modo DETACHED (o terminal fica livre)
4. O arquivo DOCKERFILE contém instruções da configuração da imagem que se pretende construir  
   Exemplo:  
   **FROM node:alpine** // usa uma imagem leve do NODEJS    
   **COPY ./opt** //copia o conteúdo do diretório atual para dentro do diretório OPT no contêiner    
   **WORKDIR /opt** //define o diretório OPT como diretório de trabalho    
   **CMD node server.js** // executa o comando node server.js quando o contêiner for iniciado.  
   **docker build -t <<nome:da:imagem>>**  Constrói a imagem de acordo com as instruções do arquivo dockerfile;
5. **docker run <<nome:da:imagem>>** Executa uma imagem;
6. Comandos para listar e remover imagens:  
   **docker image ls** (lista as imagens)  
   **docker image rm <<nome:da:imagem>>** (remove a imagem)  
   **docker rmi <<nome:da:imagem>>** (atalho para o comando que remove a imagem)
7. Comando para adicionar um NAMESPACE à imagem:  
   **docker tag <<nome:da:imagem>> <<namespace/repository:version>>**
8. Comando para inspecionar a imagem:  
   **docker inspect <<nome:da:imagem>>**
9. Comando para executar e acessar interativamente um contêiner:  
   **docker run -it <<nome:da:imagem>>**  



 
