### A aplicação

A aplicação consiste de uma API REST em [Node.JS](https://nodejs.org/en/).

Essa API será um serviço que gerencia posts de texto do tipo `tweet` (inspirado no [twitter](https://twitter.com/)):
- Criação de um _tweet_ que será identificado por um [uuid](https://en.wikipedia.org/wiki/Universally_unique_identifier) versão 4
- Acrescentar _likes_ nos _tweets_ cadastrados
- Listar os top _tweets_ com mais _likes_

## Pré-requisitos

**Disclaimer**: O setup não foi testado em sistema operacional _Windows_ então pode ser que não funcione.
Recomendo a utilização de alguma distribuição _Linux_ ou _Mac_.

Para conseguir acompanhar o workshop será necessário ter no ambiente
- [Docker](https://www.docker.com/) e [docker-compose](https://docs.docker.com/compose/)
- [Git](https://git-scm.com/)
- Conta no [Github](https://github.com/)
- Última versão de [Node.JS](https://nodejs.org/en/) (14+)
  - recomendo a utilização do [NVM](https://github.com/nvm-sh/nvm)
- Preparar sua versão do repositório
  - [fork](https://github.com/rodrigobotti/rs-ws-2020-env/fork) desse repositório
  - _git clone_ do repositório
  - executar no diretório do projeto
  ```sh
  # caso tenha optado pelo uso do nvm
  # (a versão de node vem do arquivo .nvmrc na raíz)
  nvm install
  nvm use

  # instalar as dependências
  npm install

  # verificar:

  # executar testes unitários e de integração
  # como falta o mongodb e o redis, deve falhar com timeout de conexão
  npm test

  # tentar subir a aplicação localmente em modo debug
  # como falta o mongodb e o redis, deve falhar por erro de conexão
  npm run start:dev
  ```
