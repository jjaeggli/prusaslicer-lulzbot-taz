# prusaslicer-lulzbot-taz
LulzBot TAZ printer and material profiles for use with PrusaSlicer.

## Objective

This project intends to create standard LulzBot Taz printer profiles for use
with PrusaSlicer. The profiles here are derived from the LulzBot Cura defaults
with some modifications based on the behavior and style of PrusaSlicer
configurations.

## Supported Printers and Configurations

  * LulzBot Taz 6 Single Extruder (0.50mm)
  * LulzBot Taz 6 Single Extruder (0.25mm)

## Installation

The configuration can be loaded as a configuration bundle through the
PrusaSlicer interface. To import the file, select **File** > **Import** >
**Import Config Bundle ...** and select the downloaded configuration file.

## Notes

  * Wipe temperatures for calibration are currently hard-coded for PLA at
    160&deg;. For materials which require higher or lower nozzle cleaning
    temperatures, `start_gcode` will need to be adjusted manually for the
    necessary wiping temperature.
