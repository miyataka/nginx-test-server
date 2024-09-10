# nginx-test-server

## requirements
- docker

## how to run
```bash
docker build . -q | xargs -I {} docker run  -p 8080:80 {}
```
