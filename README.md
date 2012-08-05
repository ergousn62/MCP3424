
==================
MCP3424_arduinolib
==================

Arduino library for using the MCP3424 ADC to I2C converter

First create a MCP3424 instance:

MCP3424 myMCP3424(I2Caddress, gain, resolution);
  - the I2C address depends on the way the chip is connected, see datasheet. standard = 0x68
  - gain = {0,1,2,3} and represents {x1,x2,x4,x8}
  - resolution = {0,1,2,3} and represents {12,14,16,18} bits and also influences the sample rate

Most important function used:

getChannelMv(channel);
  - reads data from a chosen channel, and converts the ADC values to mV


Contains 4 files:
- MCP3424.h - library header file
- MCP3424.cpp - library source code file
- README
- ADC_MCP3424.ino - Arduino example application
