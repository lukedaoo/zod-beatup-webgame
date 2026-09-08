# Beat Up

A rhythm game, built with a custom C game engine ([zod-ngine](https://github.com/lukedaoo/zod-ngine)) and compiled to WebAssembly so it runs right in the browser.

Source code for the game itself lives at [`ngine.example.beatup/`](https://github.com/lukedaoo/zod-ngine/tree/main/ngine.example.beatup) in the engine repo.

## Play

Open `index.html` (or the page this repo is deployed to) and hit space to start.

> **Note:** this is just a demo of the web build. Performance is noticeably worse than the native (Linux/Windows) build — the browser sandbox and WebAssembly add real overhead the native version doesn't have. If you want the smooth version, build and run it natively from the engine repo.

## Controls

Hit the arrows as they line up with the center marker:

| Key | Lane |
|-----|------|
| R | left-top |
| F | left-mid |
| V | left-bottom |
| I | right-top |
| K | right-mid |
| M | right-bottom |
| Space | center |
| P | pause |

## Console

The game has a built-in developer console — press the backtick key (`` ` ``) to open and close it. A few things you can do in there:

- `show-commands` — list everything the console understands
- `autoplay` — toggle a bot that plays the song for you
- `play-next` / `play-previous` — switch songs
- `restart-song` / `restart-playlist` — start over
- `volume <0-100>` — adjust the music volume
- `pause` — pause the song
- `toggle-ui` — hide or show the HUD
- `show-fps` — display the current frame rate
- `bind <action> <key>` — rebind a key on the fly
- `show-keybinding` — see the current key bindings

## Built with

The game runs on a small custom engine written in C23, with a rendering, input, and config system built from scratch, plus a console extension for the commands above. This build targets Emscripten/WebGL2 for the browser; the same code also runs natively on Linux and Windows.
