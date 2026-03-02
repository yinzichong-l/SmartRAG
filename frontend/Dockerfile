FROM node:18-alpine

WORKDIR /app

COPY package.json pnpm-lock.yaml pnpm-workspace.yaml /app/
COPY packages/ /app/packages/
COPY src/ /app/src/
COPY public/ /app/public/
COPY index.html tsconfig.json vite.config.ts uno.config.ts /app/

RUN npm install -g pnpm
RUN pnpm install

EXPOSE 3000

CMD ["pnpm", "run", "dev"]