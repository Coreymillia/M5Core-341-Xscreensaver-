# 341 Effects Screensaver - M5Stack Core1 Port

A conversion of the XscreensCYD project to run on M5Stack Core1 hardware, featuring 341 unique visual effects.

## Hardware Requirements

- M5Stack Core1 (ESP32-based development kit)
- 320x240 LCD display (built-in)
- 3 physical buttons A, B, C (built-in)

## Features

- **341 Visual Effects**: All original effects preserved from XscreensCYD
- **M5Stack Integration**: Native M5Stack library support
- **Button Controls**: Simple 3-button interface
- **Auto-scroll Mode**: Automatic cycling through effects
- **Serial Monitoring**: Debug output and mode information

## Controls

- **Button A**: Next effect
- **Button B**: Previous effect  
- **Button C (Hold 1 sec)**: Toggle auto-scroll mode

## Auto-scroll Mode

When enabled, effects automatically change every 30 seconds. The screen flashes green when enabled, red when disabled.

## Build Instructions

1. Install PlatformIO
2. Clone this repository
3. Build and upload:
   ```bash
   pio run --target upload
   ```

## Technical Details

### Compatibility Layer

The project uses a compatibility layer that maps Arduino_GFX calls to M5Stack API calls, allowing all 341 original effects to work unchanged on M5Stack hardware.

### Effects List

The screensaver includes effects from categories like:
- Geometric patterns
- Particle systems
- Fractals and mathematical visualizations
- 3D simulations
- Abstract animations
- Classic screensaver effects

### Memory Usage

- RAM: ~18.2% (59,800 bytes)
- Flash: ~55.7% (730,669 bytes)

## Serial Output

Connect at 115200 baud to see:
- Mode switching notifications
- Auto-scroll status
- Effect names and numbers

## Conversion Notes

This project demonstrates how to port Arduino_GFX-based projects to M5Stack hardware by:
1. Creating a compatibility wrapper class
2. Mapping touch input to physical buttons
3. Updating PlatformIO configuration for M5Stack
4. Preserving all original effect code unchanged

What it should do -- The conversion maintains 100% of the original visual effects while adapting the hardware interface.
It may or may not maintain 100% of the original visual effects.. going to say it does not. I still have not really tried to build the actual source on a pi yet. Some were converted from 3D to 2D which were probably already conversions of 2D effects somewhere along the line. I doubt anyone cares. But I am still planning on starting this entire project over some day and get it organized a little better. 

With that being said, there are a LOT of cool things in this project with plenty of room to expand. 

License & Attribution
This project ports effects originally from XScreensaver by Jamie Zawinski and contributors. The XScreensaver license permits modification and distribution for non-Windows platforms.

Original XScreensaver: https://www.jwz.org/xscreensaver/
License: MIT-compatible (no Windows restriction clause applies)
