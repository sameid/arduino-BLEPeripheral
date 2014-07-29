# Arduino BLEPeripheral

An [Arduino](http://arduino.cc) library for creating custom BLE peripherals.

## Compatible Hardware

### [Nordic Semiconductor nRF8001](http://www.nordicsemi.com/eng/Products/Bluetooth-R-low-energy/nRF8001)

 * [Adafruit](http://www.adafruit.com)
   * [Bluefruit LE - nRF8001 Breakout](http://www.adafruit.com/products/1697)
 * [RedBearLab](http://redbearlab.com)
   * [BLE Shield](http://redbearlab.com/bleshield/)
   * [Blend Micro](http://redbearlab.com/blendmicro/)
   * [Blend](http://redbearlab.com/blend/)

**Note:** Does not require use of [nRFgo Studio](http://www.nordicsemi.com/chi/node_176/2.4GHz-RF/nRFgo-Studio)!

#### Pinouts

| Shield/Board | REQ Pin | RDY Pin | RST Pin |
| ------------ | ------- | ------- | ------- |
| Bluefruit LE | 10 | 2 | 9 |
| BLE Shield, Blend | 9 | 8 | UNUSED |
| Blend Micro | 6 | 7 | UNUSED |

## Usage

### Download Library
```
cd ~/Documents/Arduino/libraries/
git clone https://github.com/sandeepmistry/arduino-BLEPeripheral BLEPeripheral
```

### Starter sketch
Load [starter.ino](examples/starter/starter.ino)

## API
See [API.md](API.md).

## Examples
See [examples](examples) folder.

## Memory usage

Creating dynamic setup messages for the nRF8001 uses a quite a lot of memory.

 * base services/characteristics: ~229 bytes
 * per characteristic: up to ~144 bytes (with notify/indicate property)
 * per descriptor: ~70 bytes


## Useful Links
 * [@lizardo](https://github.com/lizardo)'s [nRF8001 Experiments](https://github.com/lizardo/nrf8001)
   * used as a starting point to reverse engineer the proprietary setup message format for the chips
 * [@NordicSemiconductor](https://github.com/NordicSemiconductor)'s [ble-sdk-arduino](https://github.com/NordicSemiconductor/ble-sdk-arduino)
   * Original Arduino SDK for nRF8001
 * [@guanix](https://github.com/guanix)'s [arduino-nrf8001](https://github.com/guanix/arduino-nrf8001)
   * nRF8001 support for Arduino




