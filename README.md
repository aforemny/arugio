# arugio
a bevy multiplayer browser game example

![client screenshot](screen.png)

made possible with
[bevy](https://github.com/bevyengine/bevy),
[mrks-its/bevy_webgl2](https://github.com/mrk-its/bevy_webgl2)
 and
[smokku/bevy_networking_turbulence](https://github.com/smokku/bevy_networking_turbulence)

## requirements
- [install Nix](https://nixos.org/download.html)
- `nix-shell`

## run server
```bash
cd arugio_server
cargo run --release
```

## run client
```bash
cd arugio_client
cargo build --release
cd ..
wasm-bindgen --no-typescript --out-dir dist --target web ./target/wasm32-unknown-unknown/release/arugio_client.wasm
python -m http.server -d dist
```
