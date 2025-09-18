# bingo-driven
Sistema para a administração de jogos de bingo.

![demonstração do bingo](demo-bingo.gif)

## Funcionalidades
- Criação de jogos de bingo.
- Geração de números para um jogo (sorteio).
- Finalização de jogos.
- Armazenamento dos jogos e seus números sorteados.

## Tecnologias
- Back-end: Node.js, Express, Typescript, Jest e Prisma.
- Banco de dados: Postgres.
- Front-end: React e Vite.

## Desenvolvimento
- O projeto é fullstack e é necessário subir ambos front-end e back-end separadamente.
- Para o back-end:
  - Instalar as dependências com o `npm i`;
  - Criar o arquivo `.env` com base no exemplo do `.env.example`;
  - Preparar o banco de dados usando o prisma (`prisma migrate dev`);
  - Executar o comando `npm run dev`.
- Para executar os testes do back-end:
  - Criar o arquivo `.env.test` com base no exemplo do `.env.example`;
  - Prearar o banco de dados usando o Prisma (`npm run test:migration`);
  - Executar o comando `npm run test`.
- Para o front-end:
  - Instalar as dependências com o `npm i`;
  - Criar o arquivo `.env` com base no exemplo do `.env.example`;
  - Executar o comando `npm run test`. 