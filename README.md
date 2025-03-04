Passos para o Deploy

Configurar o Ambiente de Desenvolvimento: Certifique-se de ter o Node.js e o Yarn instalados no seu sistema.

Instale todas as dependências necessárias executando:

bash

Copiar

yarn install

2\. Configurando o Docker:

Dockerfile.backend: Este arquivo é usado para criar uma imagem Docker do backend da aplicação.

Dockerfile.postgres: Este arquivo configura o PostgreSQL para ser usado como banco de dados.

docker-compose.yml: Este arquivo orquestra os serviços necessários, incluindo o backend da aplicação e o banco de dados PostgreSQL.

3\. Geração de Chaves e Configuração de Banco de Dados:

O script generateKeys.sh pode ser utilizado para gerar chaves de segurança necessárias (dependendo da configuração de segurança do projeto).

init.sql é usado para inicializar o banco de dados PostgreSQL com as tabelas e dados necessários.

4\. Subir os Contêineres com Docker Compose:

Execute o seguinte comando para subir os serviços definidos no docker-compose:

bash

Copiar

docker-compose up --build

Isso irá compilar as imagens Docker e iniciar os contêineres para o backend e o banco de dados.

Rodar a Aplicação: Se desejar rodar a aplicação no modo dev ou prod especificamente, use os comandos:

bash

Copiar

Modo de desenvolvimento

yarn run start:dev

Modo de produção

yarn run start:prod

6\. Teste a Aplicação:

Verifique se a aplicação está funcionando corretamente executando testes:

bash

Copiar

yarn run test

Considerações Finais

Verifique as Configurações em Arquivos .env: Antes de iniciar os serviços com Docker, certifique-se de verificar e ajustar qualquer configuração relevante em arquivos .env para garantir que credenciais e variáveis de ambiente estejam corretas.

Recursos Adicionais e Suporte:

Consulte a documentação oficial do NestJS para mais detalhes sobre boas práticas de deploy:

docs.nestjs.com

.

Seguindo essas etapas, você conseguirá fazer o deploy do projeto de forma eficiente. Se surgir qualquer dúvida, consulte também os recursos mencionados no README do projeto ou busque suporte na comunidade.


User

ONE
