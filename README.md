# gRPC example

## Prerequisites

- go
- protocol buffer

```
brew install protobuf
```
- go plugins
```
$ go install google.golang.org/protobuf/cmd/protoc-gen-go@v1.26
$ go install google.golang.org/grpc/cmd/protoc-gen-go-grpc@v1.1
$ export PATH="$PATH:$(go env GOPATH)/bin"
```

## run

```
$ go mod tidy
$ go run greeter_server/main.go
$ go run greeter_client/main.go
$ go run greeter_client/main.go --name=Alice
```



