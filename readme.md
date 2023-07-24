# My personal blog written using rust!

This is my personal website i built using [leptos](https://leptos.dev) and [preline](https://preline.co)
---

[preview](itehax.com)

## How to run

If you don't have `cargo-leptos` installed you can install it with

```bash
cargo install cargo-leptos
```

Then run
```bash
cargo leptos new --git leptos-rs/start-axum
```

to generate a new project template.

```bash
cd {projectname}
```

to go to your newly created project.  
Feel free to explore the project structure, but the best place to start with your application code is in `src/app.rs`.  
Addtionally, Cargo.toml may need updating as new versions of the dependencies are released, especially if things are not working after a `cargo update`.

## Running your project

```bash
cargo leptos watch
```

## Installing Additional Tools

By default, `cargo-leptos` uses `nightly` Rust, `cargo-generate`, and `sass`. If you run into any trouble, you may need to install one or more of these tools, like npm dependencies.

1. `rustup toolchain install nightly --allow-downgrade` - make sure you have Rust nightly
2. `rustup target add wasm32-unknown-unknown` - add the ability to compile Rust to WebAssembly
3. `cargo install cargo-generate` - install `cargo-generate` binary (should be installed automatically in future)
4. `npm install -g sass` - install `dart-sass` (should be optional in future

## Compiling for Release
```bash
cargo leptos build --release
```

Will generate your server binary in target/server/release and your site package in target/site

## Testing Your Project
```bash
cargo leptos end-to-end
```

```bash
cargo leptos end-to-end --release
```

## Using the docker image

```bash
docker build ./ -t itehax-website
```

After it's builded.

```bash
docker run -p 3000:3000 itehax-website
```

