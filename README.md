# Build
mvn clean package && docker build -t learning.restfulapi/hello-javaee8 .

# RUN

docker rm -f hello-javaee8 || true && docker run -d -p 8080:8080 -p 4848:4848 --name hello-javaee8 learning.restfulapi/hello-javaee8 

# Deploy
C:\BLOCK6\internship\javaEE-projects>java -jar pm.jar --deploy C:\BLOCK6\internship\javaEE-projects\netbeans\hello-javaee8\target\hello-javaee8.war --port 8080
