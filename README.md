# Material Components for Slint Rust Template

A template for a Rust Application using Slint with [material components](https://github.com/slint-ui/material-components). Based on the material gallery. 

## About

This template helps you get started developing a Rust application with Slint as a toolkit
for the user interface and the material component set. It demonstrates the integration between the `.slint`
UI markup and Rust code, how to react to callbacks, get and set properties, and use of all available
material components for Slint.

## Disclaimer

The material components are currently available as a technical preview. Some components are still missing and changes to the api
are possible. We will inform as soon as the component set is read for release.

## Usage

We recommend using an IDE for development, along with our [LSP-based IDE integration for `.slint` files](https://github.com/slint-ui/slint/blob/master/tools/lsp/README.md). You can also load this project directly in [Visual Studio Code](https://code.visualstudio.com) and install our [Slint extension](https://marketplace.visualstudio.com/items?itemName=Slint.slint).

1. Install Rust by following its [getting-started guide](https://www.rust-lang.org/learn/get-started).
   Once this is done, you should have the `rustc` compiler and the `cargo` build system installed in your `PATH`.
2. Clone this repository

   ```sh
   git clone --recurse-submodules https://github.com/slint-ui/material-rust-template.git my-project
   cd my-project
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
