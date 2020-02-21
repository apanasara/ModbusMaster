# ModbusMasterFP

## Overview
This is an Arduino library for communicating with Modbus slaves over RS232/485 (via RTU protocol) using 4-20ma/ModbusMaster & C++ Function Pointer.


## Features
The following Modbus functions are available:

Discrete Coils/Flags

  - 0x01 - Read Coils
  - 0x02 - Read Discrete Inputs
  - 0x05 - Write Single Coil
  - 0x0F - Write Multiple Coils

Registers

  - 0x03 - Read Holding Registers
  - 0x04 - Read Input Registers
  - 0x06 - Write Single Register
  - 0x10 - Write Multiple Registers
  - 0x16 - Mask Write Register
  - 0x17 - Read Write Multiple Registers

Both full-duplex and half-duplex RS232/485 transceivers are supported. Callback functions are provided to toggle Data Enable (DE) and Receiver Enable (/RE) pins.


## Installation

#### Manual
Refer to Arduino Tutorials > Libraries [Manual Installation](https://www.arduino.cc/en/Guide/Libraries#toc5).


## Hardware
This library has been tested with NodeMCU v1.0 controller and Selec Multifunction meter [MFM376-C](https://www.selec.com/product/maxmin-demandphase-angle-importexport-energy-thd-upto-31st-level-rs485-communication-modbus-rtu-protocol), connected via RS485 using a Maxim [MAX485](https://hobbycomponents.com/wired-wireless/663-max485-rs485-transceiver-module) transceiver.


## Caveats
Conforms to Arduino IDE 1.5 Library Specification v2.1 which requires Arduino IDE >= 1.5.

Arduinos prior to the Mega have one serial port which must be connected to USB (FTDI) for uploading sketches and to the RS232/485 device/network for running sketches. You will need to disconnect pin 0 (RX) while uploading sketches. After a successful upload, you can reconnect pin 0.

## Example
You can find example in the [crypt_Mqtt_Modbus_wifiManager](https://github.com/apanasara/crypt_Mqtt_Modbus_wifiManager) Repository.


_Project inspired by [Doc Walker's 4-20ma/ModbusMaster](https://github.com/4-20ma/ModbusMaster) Library._

```
Copyright:: 2009-2016 Doc Walker

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

    http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
```
