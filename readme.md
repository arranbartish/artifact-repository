
```
$ docker build -t artifact-repository .
$ docker run -d --name repository-data artifact-repository echo "data-only container for Nexus"
$ docker run -d -p 8081:8081 --name repository --volumes-from repository-data artifact-repository
$ docker run -p 8081:8081 artifact-repository  
```

