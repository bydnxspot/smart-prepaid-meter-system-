# SmartPrepaid Monitor

A portable browser-based demonstration of the proposed Low-Cost Smart Prepaid Electricity (PHCN) with Remote Monitoring System.

## Run locally
1. Download or clone this repository.
2. Open `index.html` in Chrome, Edge or Firefox.
3. No Node.js, npm, API key, database or installation is required.

## Demonstration features
- Simulated voltage, current, power, energy and prepaid balance.
- Appliance presets and simulated relay/load switching.
- Single-use demonstration recharge PINs.
- SMS command simulator: `BALANCE`, `STATUS`, `HELP`, `RECHARGE <PIN>`.
- Low-credit and zero-credit alerts.
- Usage and recharge history.
- Proposed software simulation checks.
- Hardware component overview and configurable tariff, threshold and power factor.
- Browser localStorage persistence and reset control.

## Demo PINs
- `SP-1000-4821`: ₦1,000 / 20 kWh (already redeemed as opening credit).
- `SP-500-2174`: ₦500 / 10 kWh.
- `SP-2000-6390`: ₦2,000 / 40 kWh.

The assumed tariff is ₦50/kWh, matching the example in the project document. It is not a current electricity tariff quotation.

## Calculations
- Real power: P = V × I × PF
- Energy: E = (P × t) / 1000, where t is in hours.
- Purchased units: recharge amount / assumed tariff.
- Remaining balance: previous credit + purchased units − consumed energy.

## Scope and safety
This is a front-end simulation only. It is not a certified meter, live PHCN service, live GSM connection or physical hardware controller. Sensor readings, SMS, recharge and relay switching are simulated. The project work requires physical construction, calibration and testing before real-world use.

The SIM800L needs a suitable separate stable supply capable of GSM current peaks. Mains AC work must be performed by qualified personnel using appropriate isolation and protection.

## Technology
HTML, CSS and vanilla JavaScript. No external dependencies.
