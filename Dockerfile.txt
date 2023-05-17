FROM node:14.18.2
WORKDIR /app
# Copy app code
COPY /package*.json /app/
RUN npm install
#IT WILL COPY THE ENTIRE DIR FORECAST TO /app/src INSIDE DOCKER
#hehe
COPY . .
EXPOSE 3000
CMD [ "npm","start"]