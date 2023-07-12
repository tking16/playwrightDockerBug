FROM node:18-alpine

WORKDIR /app
COPY package*.json ./
RUN npx playwright install --with-deps
RUN npm install @playwright/test -D

COPY playwright.config.ts /app/
COPY . /app/

CMD npx playwright test
