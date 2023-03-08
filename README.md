<h1 align="center">
<br>Docker
</h1>

Docker é um sistema de gerenciamento de contêineres que permite aos desenvolvedores embalar, implantar e executar aplicativos facilmente em qualquer ambiente. Ele usa contêineres para embalar aplicativos em unidades de software portáteis que contêm tudo o que é necessário para executar o aplicativo: código, runtime, bibliotecas e configurações. Os contêineres são isolados uns dos outros e do ambiente de hospedagem, o que significa que os aplicativos podem ser executados em qualquer lugar, independentemente do ambiente de hospedagem.

## Container

Um container Docker contém o código, as bibliotecas, o runtime e as configurações necessárias para executar um aplicativo. Além disso, os contêineres também contêm informações sobre o ambiente de execução, como as variáveis de ambiente, os arquivos de configuração e os recursos compartilhados.

## Imagem

Uma imagem Docker é um modelo de arquivo que contém todos os elementos necessários para executar um aplicativo em um container Docker. As imagens são criadas usando o comando docker build e contêm todos os arquivos, bibliotecas e configurações necessárias para executar o aplicativo. As imagens são usadas para criar containers Docker que podem ser implantados em qualquer ambiente.

## docker run

O comando docker run é usado para executar um container Docker. Ele aceita vários parâmetros, como o nome da imagem, as variáveis de ambiente e os recursos compartilhados. O comando docker run também pode ser usado para criar um novo container a partir de uma imagem existente.

Exemplo de docker run para node:

´´´
$ docker run -it --name my-node-app -p 3000:3000 -v ./:/app/src node:16 npm start
´´´ 

## docker-compose.yml

O Docker Compose é uma ferramenta para definir e executar aplicativos multi-container. Ele usa um arquivo YAML para configurar os serviços do aplicativo e criar os contêineres necessários. O Docker Compose permite que os desenvolvedores criem e executem aplicativos multi-container de forma rápida e fácil.

Exemplo de docker-compose.yml para node:

```
version: '3.7'
services:
  node-app:
    image: node:16
    ports:
      - "3000:3000"
    volumes:
      - ./:/app/src/
    command: npm start
```

## Dockerfile

Um Dockerfile é um arquivo de texto que contém instruções para a criação de uma imagem Docker. Ele contém instruções para o Docker sobre como construir a imagem, incluindo quais arquivos devem ser incluídos, quais bibliotecas devem ser instaladas e quais comandos devem ser executados. O Dockerfile é usado para criar imagens Docker que podem ser usadas para criar containers Docker.

Exemplo de Dokcerfile para node:

```
FROM node:16
WORKDIR /app/src
COPY . .
RUN npm install
EXPOSE 3000
CMD ["npm", "start"]
```

## Diferença entre dokcer run e docker compose:

A principal diferença entre o docker run e o docker compose é que o docker run é usado para executar um único container, enquanto o docker compose é usado para executar vários containers. O docker run aceita vários parâmetros, como o nome da imagem, as variáveis de ambiente e os recursos compartilhados. O docker compose usa um arquivo YAML para configurar os serviços do aplicativo e criar os contêineres necessários.

## Benefícios:

Os principais benefícios do Docker incluem:

- Facilidade de uso: O Docker é fácil de usar e permite que os desenvolvedores criem, implantem e executem aplicativos facilmente em qualquer ambiente.

- Portabilidade: Os contêineres Docker são portáteis e podem ser implantados em qualquer ambiente, independentemente do sistema operacional ou da infraestrutura.

- Isolamento: Os contêineres Docker são isolados uns dos outros e do ambiente de hospedagem, o que significa que os aplicativos podem ser executados em qualquer lugar, independentemente do ambiente de hospedagem.

- Segurança: Os contêineres Docker são seguros e isolados, o que significa que os aplicativos não podem interferir uns nos outros. Isso torna o Docker uma ótima opção para aplicativos que precisam de segurança adicional.

<div align="center">
  <br/>
  <br/>
  <br/>
    <div>
      <sub>Copyright © 2023 - <a href="https://github.com/robertolima-dev">robertolima-dev</sub></a>
    </div>
    <br/>
    <p> 
      <a href="https://github.com/robertolima-dev/licenca/blob/main/LICENSE.md">LICENÇA</a>
    </p>
</div>
