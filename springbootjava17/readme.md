# Getting Started
### Complie the code
mvn clean install

### Complie the code with debug option
mvn clean install -e

### package code
mvn clean package

### Run jar file
java -jar springbootjava17.jar 

### Build Docker Image
docker build -t springbootjava17:latest -f Dockerfile .

### Run Docker Image
docker container run -p 8080:8080 springbootjava17:latest

### Run jar file on specfic port
java -jar springbootjava17.jar --server.port=9090

### Run Docker Image
docker container run -p 9090:9090 springbootjava17:latest

## Build and run code using docker

### Build Docker Image
docker build -t springbootjava17:latest -f Dockerfilecodecomplie .

### Run Docker Image
docker container run -p 8080:8080 springbootjava17:latest