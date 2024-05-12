# Quick Start with gRPC

## Install protobuffs
- `sudo dnf install protobuf-compiler`
- `go install google.golang.org/protobuf/cmd/protoc-gen-go@v1.28`
- `go install google.golang.org/grpc/cmd/protoc-gen-go-grpc@v1.2`
- `echo 'export PATH="$PATH:$(go env GOPATH)/bin"' >> ~/.bashrc`
- `mkdir -p gen/go`
- `protoc -I proto proto/sso/sso.proto --go_out=./gen/go --go_opt=paths=source_relative --go-grpc_out=./gen/go/ --go-grpc_opt=paths=source_relative`
