FROM node:10
WORKDIR /
COPY package*.json ./
RUN npm install
COPY ./ ./
EXPOSE 8000
ENV FRONT_URL=http://localhost:5000
CMD ["npm", "start"]
