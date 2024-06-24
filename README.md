# ESP32-OTA-Update

This project implements an Over-The-Air (OTA) update mechanism for the ESP32 development board.

## Setup Instructions

1. Clone this repository.
2. Update the `ssid` and `password` variables in the code with your WiFi credentials.
3. Update the `version_url` variable with the URL of your `version.json` file on GitHub.
4. Compile and upload the initial firmware to your ESP32 board.

## OTA Update Process

1. The ESP32 checks the `version.json` file on GitHub every minute.
2. If a new version is available, it downloads the new firmware from the specified URL.
3. The new firmware is installed, and the ESP32 restarts.

## Testing the OTA Update

1. Compile your firmware and upload it to the ESP32.
2. Update the `version.json` file on GitHub with a new version number and the URL of the new firmware binary.
3. Wait for the ESP32 to check for updates (or reset it to trigger an immediate check).
4. The ESP32 should download and install the new firmware.

## Simulating a New Firmware Release

1. Make changes to your firmware code.
2. Compile the new firmware and upload the binary to your GitHub repository.
3. Update the `version.json` file with the new version number and the URL of the new firmware binary.
4. Commit and push these changes to GitHub.
5. Your ESP32 will detect the new version on its next check and perform the update.
