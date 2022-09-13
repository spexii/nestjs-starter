FROM node:16

WORKDIR /app

RUN chown -R node /app
USER node

COPY --chown=node src src
COPY --chown=node package.json .
COPY --chown=node tsconfig.json .
COPY --chown=node tsconfig.build.json .
COPY --chown=node yarn.lock .
COPY --chown=node .env .

RUN yarn install --frozen-lockfile
RUN yarn build

CMD ["node", "dist/main.js"]
