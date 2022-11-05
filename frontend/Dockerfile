FROM node:16-alpine

WORKDIR /src

COPY . .

RUN npm i

RUN npm run build

EXPOSE 3000

RUN npm install -g serve

CMD ["serve", "-s", "build"]