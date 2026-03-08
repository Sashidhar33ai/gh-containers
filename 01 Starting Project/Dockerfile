FROM node:20-alpine

ENV MONGODB_CONNECTION_PROTOCOL: mongodb+srv
ENV MONGODB_DB_NAME: gha-demo1
ENV MONGODB_CLUSTER_ADDRESS: samplecluster.npslotd.mongodb.net
ENV MONGODB_USERNAME: ${{ secrets.MONGODB_USERNAME }}
ENV MONGODB_PASSWORD: ${{ secrets.MONGODB_PASSWORD  }}

WORKDIR /app

COPY package*.json .

RUN npm install

COPY . .

CMD ["npm", "start"]