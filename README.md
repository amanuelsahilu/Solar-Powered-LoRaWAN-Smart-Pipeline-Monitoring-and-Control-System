# Solar-Powered LoRaWAN Smart Pipeline Monitoring and Control System

**LINE GUARD** is a capstone prototype for solar-powered pipeline monitoring and remote valve control. The proposed field node measures pressure, flow, temperature, and vibration; records data locally; and sends telemetry over LoRaWAN. Fault detection and remote isolation are planned capabilities, not yet validated product functions.

## Project status

This repository currently contains the project structure and report-derived design material. Firmware, editable PCB designs, gateway and dashboard implementations, datasets, and trained models have not yet been added. The existing [design overview and report figures](LINE_GUARD_GitHub_Starter/line_guard_github/README.md) describe the design and distinguish preliminary work from planned implementation.

The planned field node uses an ESP32-S3, a LoRaWAN radio, GPS, pressure/flow/temperature/vibration sensors, local microSD logging, an OLED, and a motorized valve driver. The intended validation environment is a low-pressure water test loop; this prototype is not a certified pipeline safety or SCADA system.

## Repository layout

| Path | Purpose |
|---|---|
| `docs/` | Architecture, requirements, reports, and test documentation |
| `firmware/field-node/` | Embedded software for the sensor and valve-control node |
| `hardware/main-pcb/` | Editable controller PCB design files |
| `hardware/power-pcb/` | Editable solar charging and power-conversion PCB files |
| `hardware/bom/` | Bill of materials and sourcing notes |
| `gateway/` | LoRaWAN gateway and network integration |
| `dashboard/` | Monitoring, alarms, and operator interface |
| `machine-learning/` | Dataset notes, training, and model evaluation |
| `tests/` | Hardware-in-the-loop, integration, and acceptance tests |
| `data/` | Dataset documentation; raw and processed data are not committed by default |
| `LINE_GUARD_GitHub_Starter/line_guard_github/` | Existing report-based overview and associated figures |

Component folders include a README describing their intended contents and current status. Add implementation files as they become available.

## Safety and scope

Use the system only for supervised prototype testing. Do not connect it to live pipelines or rely on it for safety-critical isolation. Validate sensor calibration, radio delivery, valve behavior, power autonomy, and fail-safe behavior on a controlled test rig before any field trial.
