FROM node:16-alpine
ENV NODE_ENV = 'production'
ENV PORT = 5000
ENV URL_DB_CONNECTION = 'mongodb://172.31.28.133:27017/bookstore'
# Create app directory
WORKDIR /usr/src/app

# Install app dependencies
# A wildcard is used to ensure both package.json AND package-lock.json are copied
# where available (npm@5+)
COPY package*.json ./



RUN npm install
# If you are building your code for production
# RUN npm ci --only=production

# Bundle app source
COPY . .

# Run this at the first time to save books on db
#CMD ["node","createBook.js"]
RUN node createBook.js
EXPOSE 5000
CMD [ "node", "server.js" ]
