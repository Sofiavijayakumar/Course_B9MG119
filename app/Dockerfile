FROM node:18-alpine
WORKDIR /app
# Install app dependencies
COPY . .
RUN yarn install --production
CMD ["node", "app/src/index.js"]
EXPOSE 3000