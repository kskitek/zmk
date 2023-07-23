# ZMK config cor Corne Wireless

[Corne wireless docs](https://docs.typeractive.xyz/build-guides/corne-wireless)


## Reflashing nice!nano

[Docs](https://nicekeyboards.com/docs/nice-nano/troubleshooting/#my-nicenano-seems-to-be-acting-up-and-i-want-to-re-flash-the-bootloader)

In this case you can most likely re-flash the bootloader using adafruit-nrfutil. Here are the steps you'll want to follow:

1. Follow the installation section [here](https://github.com/adafruit/Adafruit_nRF52_nrfutil#installation). Most likely you'll just need to run pip3 install --user adafruit-nrfutil.
2. Download the [DFU pkg of the nice!nano bootloader](https://nicekeyboards.com/assets/nice_nano_bootloader-0.6.0_s140_6.1.1.zip).
3. Connect your nice!nano and put it into the bootloader using a double-tap reset.
4. Run the following command in your terminal:

```
adafruit-nrfutil --verbose dfu serial --package nice_nano_bootloader-0.6.0_s140_6.1.1.zip -p SERIALPORT -b 115200 --singlebank --touch 1200
```


However, replace `SERIALPORT` with your respective serial port name on your OS.

On MacOS and Linux it will look something like `/dev/ttyS0`, but you'll of course need to double check the exact path name.
After this runs, you should have your bootloader all re-flashed and fresh.

## Keymap configurator

https://nickcoutsos.github.io/keymap-editor/
