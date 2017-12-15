# Golang + dep

Golang docker image with Dep Package Management.

## Usage
### Build the image
To create the image `creativebit/go-dep`, execute the following command.
```
$ docker build -t creativebit/go-dep 1.x/
```
### Run the image
To run the image:
```
$ docker run --rm creativebit/go-dep --help
$ docker run --rm -v $GOPATH/src:/go/src -w /go/src/github.com/your-account/project creativebit/go-dep ensure
```
### Docker Compose
With docker-compose.yml
```
ensure:
  image: creativebit/go-dep
  command: ensure
  volumes:
    - $GOPATH/src:/go/src
  working_dir: /go/src/github.com/your-account/project
```

## License

This project is released under the MIT license. See [LICENSE](https://github.com/jhsc/docker-golang-tools/blob/master/LICENSE) for more details.