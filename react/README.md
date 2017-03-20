## Create react image
```
docker build -t react .
```

## Create react app
```
docker run -v --rm /parent/path:/code create-react-app app-name
cd app-name
docker run -v --rm /path/app-name:/code -p 127.0.0.1:3000:3000 react
```

## Run react
```
docker run --rm -p 127.0.0.1:3000:3000 -v /tmp/blog:/code react
```

or 

```
docker run --rm -e HOST=0.0.0.0 -p 3000:3000 -v $(pwd):/code react
```
