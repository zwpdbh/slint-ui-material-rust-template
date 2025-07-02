# Material Components for Slint Rust Template

A template for a Rust Application using Slint with [material components](https://github.com/slint-ui/material-components). Based on the material gallery. 

## My Notes 

After git clone this project, run following commands to sync submodule and update them.

```sh 
git submodule sync
git submodule update --init --recursive
```

## Run your application on desktop

1. Build with `cargo`:
    ```
    cargo build
    ```

2. Run the application binary:

    ```
    cargo run
    ```

## Run your application on a web browser

You can then use wasm-pack (which you may need to obtain with `cargo install wasm-pack`).
This will generate the wasm in the `./pkg` directory, which the `index.html` file will open.
Since wasm files cannot be served from `file://` URL, you need to open a wab server to serve
the content

```sh
wasm-pack build --release --target web
python3 -m http.server
```

## Run your application on Android

First, [set up your Android environment](https://slint.dev/snapshots/master/docs/rust/slint/android/#building-and-deploying).
Then, you can run the demo on an Android device with the following command:

```sh
cargo apk run --target aarch64-linux-android --lib
```

## Next Steps

We hope that this template helps you get started, and that you enjoy exploring making user interfaces with Slint. To learn more
about the Slint APIs and the `.slint` markup language, check out our [online documentation](https://slint.dev/docs). Check out
also the [material components documentation](https://material.slint.dev/overview/)

Don't forget to replace the contents of this readme with your own project details. As well as dit the `name =` field in `Cargo.toml` to match the name of your
project.
