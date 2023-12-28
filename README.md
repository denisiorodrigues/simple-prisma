# Simple Prisma

Aplicação de exemplo para entendimento do ORM Prisma, seguindo os passos da **[📄 Documentação oficial](https://www.prisma.io/docs/getting-started)**.

Para esse exemplo, vamos utilizar Docker para realizar a o laboratório. O docker será executado na distribuição Linux através da WSL2.

---

## Docker

### Bitnami

Usando a imagem **[bitnami/mongodb](https://hub.docker.com/r/bitnami/mongodb)**.

Comando pra criar o container.
`docker run -d --name mongodb-prisma -e ALLOW_EMPTY_PASSWORD=yes -e MONGODB_EXTRA_FLAGS='--wiredTigerCacheSizeGB=2' -p 27210:27210 bitnami/mongodb:latest`

__❌Não consegui realizer os teste__

### Atlas

Utilizando o passo a passo da **[documentação oficial do mongo](https://www.mongodb.com/docs/atlas/cli/stable/atlas-cli-deploy-docker/#std-label-atlas-cli-deploy-docker)**.

Rodando o container 
`docker run -p 27777:27017 --privileged -it mongodb/atlas bash`

Criando o arquivo de configuraçaõ dentro do container.
``atlas deployments setup --bindIpAll --username root --password root --type local --force`

Testar no mongosh
`mongosh {connection_string}`

Examplo:
`mongosh mongodb://root:root@localhost:27017/?directConnection=true`

---

## Configuração da máquina

> **Sistema Operacional**: Microsoft Windows 11 Pro
> **Prcessador**: 11th Gen Intel(R) Core(TM) i5-1135G7 @ 2.40GHz, 1382 Mhz, 4 Core(s), 8 Logical Processor(s)
> **Memória RAM**: 16,0 GB