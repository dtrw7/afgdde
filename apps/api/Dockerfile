
FROM node:20-alpine


RUN npm i -g pnpm
RUN npm i -g turbo


WORKDIR /unkey

COPY . .


RUN pnpm install -r
RUN pnpm turbo run build --filter=api

ENV NODE_ENV production

CMD ["node", "apps/api/dist/main.mjs"]
