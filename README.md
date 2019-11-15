# grpc-ts-test

To get started, make sure to install the NPM dependencies:

`$ npm install`


# To generate code in Protocol Buffers:

### generate js codes:
```
protoc-gen-grpc \
--js_out=import_style=commonjs,binary:./src/proto \
--grpc_out=./src/proto \
--proto_path ./proto \
./proto/book.proto
```

### generate d.ts codes:
```
protoc-gen-grpc-ts \
--ts_out=service=true:./src/proto \
--proto_path ./proto \
./proto/book.proto
```


# To build:

### bash1 (server)
```
cd ./
sh ./bash/build.sh  # build js & d.ts codes from proto file, and tsc to build/*.js
sh ./bash/server.sh # start the grpc server
```

### bash2 (client)
```
cd ./
sh ./bash/client.sh # start the grpc client & send requests
```
