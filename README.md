# Raspberry Pi Pico WebUSB demo

Builds the tinyusb webusb demo for Raspberry Pi Pico.


# Build instructions

```bash
# 1. Create a build directory

mkdir build ; cd build


# 2. Clone pico-sdk

git clone https://github.com/raspberrypi/pico-sdk
(cd pico-sdk && git submodule update --init)


# 3. cmake & build  

cmake -DPICO_SDK_PATH .. && make
```
