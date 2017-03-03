# Jenkins data volume container

## Create the data volume
```
docker build -t jenkins-data .
docker run --name=jenkins-data jenkins-data
```

## Start Jenkins container
```
docker pull jenkins
docker run -p 8080:8080 -p 50000:50000 --name=jenkins-master --volumes-from=jenkins-data jenkins
```
