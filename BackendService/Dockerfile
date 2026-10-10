FROM node:26-slim

WORKDIR /app

COPY package*.json ./

RUN npm ci --omit=dev

COPY --chown=node:node . .

RUN chmod +x /app/entrypoint.sh

ENV NODE_ENV=production

USER node

EXPOSE 8083

ENTRYPOINT ["/app/entrypoint.sh"]
