FROM node:26-slim
WORKDIR /app
COPY package*.json ./
RUN  npm ci
ENV NODE_ENV=production
RUN  chmod +x ./entrypoint.sh
USER node
EXPOSE 8083
ENTRYPOINT ["./entrypoint.sh"]

