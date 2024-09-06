FROM node:lts-alpine

WORKDIR /app

COPY package.json package.json
RUN npm install

COPY next.config.mjs next.config.mjs
COPY postcss.config.js postcss.config.js
COPY tailwind.config.ts tailwind.config.ts
COPY tsconfig.json tsconfig.json

COPY .env .env

COPY public public
COPY src src

RUN npm run build

CMD npm start