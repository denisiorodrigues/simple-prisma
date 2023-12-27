# Simple Prisma

Aplicação de exemplo para entendimento do ORM Prisma, seguindo os passos da **[📄 Documentação oficial](https://www.prisma.io/docs/getting-started)**.

Para esse exemplo, vamos utilizar Docker para realizar a o laboratório. O docker será executado na distribuição Linux através da WSL2.

## Docker

Imagem utilizada: **[bitnami/mongodb](https://hub.docker.com/r/bitnami/mongodb)**

Comando pra criar o container.
`docker run -d --name mongodb-prisma -e ALLOW_EMPTY_PASSWORD=yes -e MONGODB_EXTRA_FLAGS='--wiredTigerCacheSizeGB=2' -p 27210:27210 bitnami/mongodb:latest`

### Configuração da máquina

> **Sistema Operacional**: Microsoft Windows 11 Pro
> **Prcessador**: 11th Gen Intel(R) Core(TM) i5-1135G7 @ 2.40GHz, 1382 Mhz, 4 Core(s), 8 Logical Processor(s)
> **Memória RAM**: 16,0 GB