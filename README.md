# assignment-1
# solution for react application task
Creating dockerfile for react-image
# content in docker file
    FROM node:alpine
    WORKDIR /app
    COPY package.json .
    RUN npm install 
    COPY . .
    EXPOSE 3000
    CMD [npm”,“start”]
# building the image by using dockerfile
docker build -t react-image .
# After sucessful built the image, create a container for this image
docker run -d -p 3000:3000 --name react-app react-iamge 
# To check the application is working or not.
https://ipaddress:3000 (docker is installed in cloud)
https://localhost:3000 (docker is installed in local system)


