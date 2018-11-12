FROM golang:1.8

WORKDIR /Users/tim/go/src/
COPY . .

RUN curl https://glide.sh/get | sh
RUN glide init
RUN edit glide.yaml
RUN glide update
RUN glide install

RUN glide get github.com/foo/bar

RUN go get -d -v glide
RUN go install -v glide
CMD ["app"]