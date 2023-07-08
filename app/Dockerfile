FROM node:18-alpine
WORKDIR /app
# Install app dependencies
COPY ./app .
RUN yarn install --production
RUN npm install 
CMD ["node", "src/index.js"]
EXPOSE 3000