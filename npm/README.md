
This npm package was generated automatically from the `lnrpc/rpc.proto` file in https://github.com/lightningnetworks/lnd.

To regenerate it, run:

```sh
git clone https://github.com/lightningnetworks/lnd
git clone https://github.com/googleapis/googleapis
cd lnd/npm
npm install
npm install -g grpc-tools
rm -r google/api
cp -r ../../googleapis/google/api google/ # because the `.js` files will be generated next to the `.proto` files
grpc_tools_node_protoc --js_out=import_style=commonjs,binary:../npm --grpc_out=../npm --plugin=protoc-gen-grpc=`which grpc_tools_node_protoc_plugin` rpc.proto
npm test
