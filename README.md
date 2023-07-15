# pw_template

A minimal starter repo for Pigweed projects.

## Setup

1. `git submodule update --init --recursive` to make sure all deps install?

1. `. bootstrap.sh`

1. `pw package install pico_sdk`

1. `gn gen out && ninja -C out`

1. Hold BOOTSEL, press Reset button (on extension board), mount the Pico as USB Mass Storage, then:

       cp out/rp2040_pw_system.debug/obj/src/pico.uf2 /media/kayce/RPI-RP2/

## Notes

https://pigweed.dev/pw_system/#target-bringup should link to the exact
stm32cube source code file

RPC worked!

```
pw-system-console -d /dev/ttyACM0 -b 115200 \
        --proto-globs third_party/pigweed/pw_rpc/echo.proto
```

## Guidelines

* Minimal
* Complete
* Reproducible
* Enticing

https://stackoverflow.com/help/minimal-reproducible-example
