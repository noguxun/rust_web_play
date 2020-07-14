# Introduction
This project shows how to start a plain rust wasm application that could be easily deployed to any web server, no npm is required.  
Verified on Ubuntu and MacOS

# Enviroment Setup
```
# Install build essential packages for rust building on Ubuntu
# only needed for Ubuntu
sudo apt install build-essential

# Install rust toolchain
curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh

# Install wasm-pack 
curl https://rustwasm.github.io/wasm-pack/installer/init.sh -sSf | sh

# Install basic-http-server for simple test
cargo install basic-http-server

```

# Build Project
```
# build rust wasm project
# the output will be in the pkg folder
cd rust_wasm_template
wasm-pack build --target web
```

# Test Rust Wasm Application
Run basic-http-server to server index.html file in www folder.  
index.html imports ../pkg/first_wasm.js, which is web-pack build output. 
```
cd rust_wasm_template
basic-http-server --addr 0.0.0.0:4000
```
In browser, access html file in the www folder
http://localhost:4000/www/index.html


```
https://rustwasm.github.io/wasm-bindgen/examples/fetch.html
https://github.com/rustwasm/wasm-bindgen/tree/master/examples/fetch

```

