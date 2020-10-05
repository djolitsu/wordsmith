FROM golang:1.15.2 as build
WORKDIR /go/src/github.com/djolitsu/wordsmith/web
COPY dispatcher.go .
RUN CGO_ENABLED=0 GOOS=linux go build -a -installsuffix cgo -o dispatcher .

FROM scratch
COPY --from=build /go/src/github.com/djolitsu/wordsmith/web .
COPY static/ .
EXPOSE 80
CMD ["./dispatcher"]

