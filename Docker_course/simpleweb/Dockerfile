FROM node:14-alpine

# "./" mentioned in next command after this "workdir" command points to the "/usr/app"
WORKDIR /usr/app

# We aren't running "npm install" before copy because "npm install" needs need package.json file.
# The cache of this command will only be invalidate if we change package.json file, or change any step above it.
# If i cahnge index.js, it will not have effect on the chache of this step and run npm install step.
COPY ./package.json ./

# npm will call package.json file. that's why it needs to be called before.
RUN npm install

# Now you can make changes in the index.js file and it will not invalidate the cache of "run npm install" and saves time to rebuilding "run npm install" step.
# First "./" refers to anything inside my local working directory, copy it to "./" inside container. Here "./" means copy inside "usr/app" of container.
COPY ./ ./

CMD ["npm", "start"]