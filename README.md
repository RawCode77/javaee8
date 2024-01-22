# Build
mvn clean package && docker build -t learning.restfulapi/hello-javaee8 .

# RUN

docker rm -f hello-javaee8 || true && docker run -d -p 8080:8080 -p 4848:4848 --name hello-javaee8 learning.restfulapi/hello-javaee8 