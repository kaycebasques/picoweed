# picoweed

Raspberry Pi Pico + Pigweed

## Setup

```
git clone git@github.com:kaycebasques/picoweed.git --recursive
# Only needed if you forgot to run `git clone` with `--recursive`.
git submodule update --init --recursive
source bootstrap.sh
pw package install pico_sdk
gn gen out
```

## Build

```
ninja -C out
```

## Flash

1. Hold **BOOTSEL**.
2. Press **Reset**.
3. Mount the Pico as USB Mass Storage.
4. `cp out/rp2040_pw_system.debug/obj/src/<app>.uf2 /media/<user>/RPI-RP2/`
