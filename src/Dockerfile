# Stage 1: Build & Minimal Runtime Base
FROM node:20-alpine AS runner

# Create non-root user for container security compliance
USER node

WORKDIR /home/node/app

COPY --chown=node:node package*.json ./
COPY --chown=node:node src/ ./src/

EXPOSE 8080

CMD ["node", "src/server.js"]
