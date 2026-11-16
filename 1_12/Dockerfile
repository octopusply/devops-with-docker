FROM ubuntu
EXPOSE 5001

WORKDIR /usr/src/app

RUN apt-get update && apt-get install -y curl
RUN curl -sL https://deb.nodesource.com/setup_16.x | bash
RUN apt-get install -y nodejs


COPY . .
RUN npm install
RUN npm install -g serve

RUN npm run build

CMD ["serve", "-s", "-l", "5001", "build"]