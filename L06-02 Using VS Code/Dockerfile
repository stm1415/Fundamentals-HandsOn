FROM node:lts-alpine
ENV NODE_ENV=production
WORKDIR /usr/src/app
COPY ["package.json", "package-lock.json*", "npm-shrinkwrap.json*", "./"]
RUN npm install --production --silent && mv node_modules ../
COPY . .
EXPOSE 3000
RUN chown -R node /usr/src/app
USER node
CMD ["npm", "start"]


# run the following commands to build the image and run the container
# used the name `myexpressapp` based on the `name` field in your `package.json` file, which is `"myexpressapp"`. This is a common practice to keep the Docker image name consistent with the application name. You can choose any name you prefer for your Docker image.
# docker image build --pull --file "C:\Users\Magar Suman\Desktop\PythonBackendDevelopment\Containers\Fundamentals-HandsOn/L06-02 Using VS Code/Dockerfile" --tag "myexpressapp:latest" --label "com.microsoft.created-by=visual-studio-code" "C:\Users\Magar Suman\Desktop\PythonBackendDevelopment\Containers\Fundamentals-HandsOn/L06-02 Using VS Code" <
# docker run --rm -d -p 3000:3000/tcp --name myexpressapp_container myexpressapp:latest