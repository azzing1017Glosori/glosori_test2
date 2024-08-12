FROM node:18

WORKDIR /usr/src/app
COPY package.json package-lock.json ./
RUN npm install -g pnpm
RUN pnpm install
# RUN npm install
COPY . .
# RUN pnpm install --save-dev
# RUN pnpm build
EXPOSE 3000
# CMD [ "npm", "run", "start-watch" ]
CMD ["pnpm", "start"]