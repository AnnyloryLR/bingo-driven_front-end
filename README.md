# bingo-driven
Sistema para a administração de jogos de bingo.

![demonstração do bingo](demo-bingo.gif)

## Funcionalidades
- Criação de jogos de bingo.
- Geração de números para um jogo (sorteio).
- Finalização de jogos.
- Armazenamento dos jogos e seus números sorteados.

## Tecnologias
- Front-end: React e Vite.

## Link
- https://bingo-driven-front-end-orpin.vercel.app/

## Usando o Docker para rodar o projeto manualmente
Os passos para subir manualmente são:
- Implementação do "Dockerfile" na raiz do projeto;
- Realizar o build da imagem:
    $ docker build -t nomedaimagem .
- Subir o front-end em um container:
    $ docker run -d --name nomedocontainer --network nomedarede -p 8000:80 nomedaimagem

## Usando o Docker Compose para rodar somente o front-end
- Faça o build da imagem: docker build -t frontend .

O docker compose permite a automatização do processo para rodar o projeto através da criação do arquivo "docker-compose.yml", nesse caso, subiremos somente o front-end:

    services:
        <nome do serviço de front-end>:
            image: frontend
            container_name: <nome do container>
            build: frontend/
            ports:
              - 8000:80 #porta padrão de tráfego web
            networks:
              - <nome da rede do backend>
        
    networks:
        <nome da rede do backend>:
            external: true

    volumes:
        <nome do volume>:
    
Comandos para rodar o projeto usando o docker compose:
- Subir o projeto:
    $ docker compose up 
- Parar o projeto:
    $ docker compose stop
- Desmontar o projeto:
    $ docker compose down
- Recriar o projeto:
    $ docker compose up --build
               

