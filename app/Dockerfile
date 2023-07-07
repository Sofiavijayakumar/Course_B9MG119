FROM node:18-alpine
WORKDIR /app
# Install app dependencies
COPY . .
RUN npm install
RUN yarn install --production
CMD ["node", "src/index.js"]
EXPOSE 3000