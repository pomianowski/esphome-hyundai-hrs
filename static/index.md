# ESPHome Hyundai HVAC Controller

A comprehensive ESPHome template for controlling Hyundai HVAC systems using Modbus over RS485 protocol. This project enables you to integrate your Hyundai HVAC unit into your home automation setup.

## Features

- 🔄 Real-time climate control status monitoring via Modbus
- 🌡️ Temperature control
- 💨 Fan speed adjustment
- ❄️ Cooling/Heating mode control
- 🔌 Remote start/stop capability
- 📱 Mobile-friendly web interface
- 🔐 Secure authentication
- 📊 Detailed climate statistics

## Prerequisites

- ESP32 or ESP8266 board
- Hyundai HVAC unit with RS485 interface
- RS485 to USB/TTL converter
- Home Assistant instance (optional)

## Hardware Setup

1. Connect the RS485 interface to your ESP32/ESP8266:
   - A+ to GPIO21 (or your configured RX pin)
   - B- to GPIO22 (or your configured TX pin)
   - GND to GND
   - VCC to 5V (if required by your RS485 converter)

## Installation

### Option 1: Direct Installation (Recommended)

You can install the pre-built firmware directly to your device via USB from the browser:

<esp-web-install-button manifest="firmware/hyundai-hrs.manifest.json"></esp-web-install-button>

<script type="module" src="https://unpkg.com/esp-web-tools@10/dist/web/install-button.js?module"></script>

### Option 2: Manual Installation

1. Clone this repository
2. Copy `hyundai-hvac.yaml` to your ESPHome configuration
3. Update the configuration with your Modbus settings
4. Compile and flash to your device

## Configuration

The template requires Modbus configuration settings including UART pins, baud rate, and device address. See the example configuration in `hyundai-hvac.yaml` for detailed setup instructions.

## Integration with Home Assistant

This template automatically creates the following entities in Home Assistant:

- Climate entity for temperature control
- Fan entity for fan speed control
- Binary sensors for various HVAC states
- Sensors for temperature and system information

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgments

- ESPHome team for the amazing framework
- All contributors who have helped improve this project