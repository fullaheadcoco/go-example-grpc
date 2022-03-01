# gRPC example

## Prerequisites

- go
```
brew install go
```
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


## Generate gRPC code 
```
$ protoc --go_out=. --go_opt=paths=source_relative \
    --go-grpc_out=. --go-grpc_opt=paths=source_relative \
    helloworld/helloworld.proto
```

## Run

```
$ go mod tidy
$ go run greeter_server/main.go
$ go run greeter_client/main.go
$ go run greeter_client/main.go --name=Alice
```



