# Docker
## Treinamento Docker (Udemy  Argus Academy)

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
** docker pull <<image:tag>>  
Exemplo:     docker pull mcr.microsoft.com/mssql/server:2022-latest


 
