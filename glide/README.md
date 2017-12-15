# Golang + Glide

Golang docker image with Glide Package Management.

## Usage
### Build the image
To create the image `creativebit/go-glide`, execute the following command.
```
$ docker build -t creativebit/go-glide 1.x/
```
### Run the image
To run the image:
```
$ docker run --rm creativebit/go-glide --version
```
### Docker Compose
With docker-compose.yml
```
glide:
  image: creativebit/go-glide
  command: install
  volumes:
    - $GOPATH/src:/go/src
  working_dir: /go/src/github.com/your-account/project
```

## License

This project is released under the MIT license. See [LICENSE](https://github.com/jhsc/docker-golang-tools/blob/master/LICENSE) for more details.