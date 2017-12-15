FROM golang:1.9

LABEL maintainer="hi@jhsc.io"

ENV GODEP_VERSION=v0.3.2

WORKDIR /go/src

RUN go get -u github.com/golang/dep/... \
  && cd /go/src/github.com/golang/dep \
  && git checkout ${GODEP_VERSION} \
  && go install github.com/golang/dep/... \
  && mv /go/bin/dep /usr/bin

# ENTRYPOINT ["dep"]
# CMD ["-h"]

CMD ["dep", "-h"]