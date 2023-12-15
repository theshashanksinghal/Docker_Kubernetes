FROM node:14-alpine

WORKDIR '/app'

# Now we don't want to rebuild the image if we make any changes to index.js file. This image should be rebuild only when package.json gets changed, which will be rare case.
COPY package.json .

RUN npm install

COPY . .

CMD ["npm", "start"]