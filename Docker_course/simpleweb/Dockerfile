FROM node:14-alpine

# "./" mentioned in next command after this "workdir" command points to the "/usr/app"
WORKDIR /usr/app

#first "./" refers to anything inside my local working directory, copy it to "./" inside container. Here "./" means copy inside "usr/app" of container.
COPY ./ ./
# npm will call package.json file. that's why it needs to be called before.
RUN npm install

CMD ["npm", "start"]