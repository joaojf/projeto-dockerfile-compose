# Projeto Dockerfile Compose Nginx

Este projeto permite a criação e execução de um ambiente Docker com Nginx utilizando um Dockerfile e um docker-compose.yml. O Dockerfile é responsável por criar uma imagem do Nginx com um arquivo index.html customizado, enquanto o docker-compose.yml define a configuração para executar o contêiner Nginx e mapear a porta 8080.

## Pré-requisitos

Antes de começar, certifique-se de que o seguinte software esteja instalado em seu sistema:

- [Docker](https://www.docker.com/)

## Configuração

1. Clone o repositório do projeto para o seu ambiente local:

   ```shell
   git clone https://github.com/joaojf/projeto-dockerfile-compose.git

2. Acesse o diretório do projeto:
   ```shell
   cd projeto-dockerfile-compose

3. Execute o comando Docker para fazer o build da imagem do Nginx:
   ```shell
   docker image build -t nginx:1.0 .
   ```
   Esse comando cria uma imagem Docker com a tag nginx:1.0, utilizando o Dockerfile       
   fornecido no projeto.
4. Execute o comando docker compose para iniciar o contêiner Nginx:
   ```shell
   docker compose -f docker-compose.yml up -d
   ```
   O docker compose lerá o arquivo docker-compose.yml e iniciará o contêiner Nginx em 
   segundo plano, mapeando a porta 8080 do host para a porta 80 do contêiner
5. Pode fazer um teste pela linha de comando usando o curl:
   ```shell
   curl localhost:80/cep.html
   ```
   - Pode fazer pelo navegador também acessando `htt://localhost:80/cep.html` para ver a página do html.

## Notas

- Certifique-se de ter privilégios de administrador para executar o Docker.
- Lembre-se de modificar as configurações do Dockerfile de acordo com suas necessidades.
- Verifique se possui uma conexão de rede adequada para acessar o Nginx no navegador.
- O arquivo cep.html está incluído no projeto para ser copiado para o contêiner. Caso deseje alterar o conteúdo do arquivo, basta modificá-lo antes de executar o build da imagem.
- Você pode modificar a configuração do Nginx editando o arquivo de configuração dentro do container.

## Contribuição
Contribuições são bem-vindas! Se você encontrar algum problema ou tiver sugestões para melhorar este projeto, sinta-se à vontade para abrir uma issue ou enviar um pull request.

