# Syncthing wrapper
If you regularly use syncthing, but it is inconvenient for you to work with it in a browser, you can use this application. Synching wrapper was created on Rust and using tauri, and therefore works lightning fast and does not consume extra RAM

## Install
**Dependencies**:
- Rust
- Cargo
- Synctghing

I will assume that you have already configured syncthing to run automatically on a specific port on your system
1. Clone this repo:
```sh
git clone git@github.com:Alchemmist/syncthing-wrapper.git
cd syncthing-wrapper
```
2. Set port
If you have configured synching in such a way that it does not run on the default port (8384), then you need to open the `./src-tauri/tauri.conf.json` and change the `devPath` and `ur` there, setting your port there
3. Build app
```sh
cargo tauri build
```
After build in `src-tauri/target/release` will be create `syncthgin-wrapper` binary 
4. Add to PATH. 
Next, you need to add `./src-tauri/target/release` to your PATH variable

5. *optional* Create app
If you use Linux you can create .desktop file and run Syncthing from your application manager. You neeed to create file `~/.local/share/applications/Synctghin.desktop`:
```desktop
[Desktop Entry]
Name=Syncthing
Exec=syncthgin-wrapper
Icon=/path/to/project/icon.png
Type=Application
Categories=Utility;
```

