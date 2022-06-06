brew install protobuf

go get google.golang.org/protobuf/cmd/protoc-gen-go
go get google.golang.org/grpc/cmd/protoc-gen-go-grpc

go install google.golang.org/protobuf/cmd/protoc-gen-go
go install google.golang.org/grpc/cmd/protoc-gen-go-grpc

example : protoc *.proto --go_out=../server --go-grpc_out=../server

protoc *.proto --go_out={pathที่จะไปสร้าง} --go-grpc_out={pathที่จะไปสร้าง}