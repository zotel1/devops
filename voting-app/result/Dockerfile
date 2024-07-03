FROM node:alpine
WORKDIR /app
LABEL org.opencontainers.image.description="result"\
      org.opencontainers.image.authors="CristianSigel"
ENV PORT 80
COPY package*.json /app
RUN npm install
COPY . /app
EXPOSE 80
CMD [ "npm", "start" ]