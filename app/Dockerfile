FROM node:18-alpine
WORKDIR /app
# Install app dependencies
COPY . .
RUN yarn install --production
RUN npm install ./app
CMD ["node", "src/index.js"]
EXPOSE 3000