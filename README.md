# prusaslicer-lulzbot-taz

LulzBot TAZ printer and material profiles for use with PrusaSlicer.

## Objective

This project intends to create standard LulzBot Taz printer profiles for use
with PrusaSlicer. The profiles were originally derived from the LulzBot Cura
defaults and have evolved based on PrusaSlicer features and changes.

## Supported Printers and Configurations

  * LulzBot Taz 5 Single Extruder (0.50mm)
  * LulzBot Taz 6 Single Extruder (0.50mm)
  * LulzBot Taz Mini Single Extruder (0.50mm)
  * LulzBot Taz Mini 2 Aero (0.50mm)

## Installation

The configuration can be loaded as a configuration bundle through the
PrusaSlicer interface. To import the file, select **File** > **Import** >
**Import Config Bundle ...** and select the downloaded configuration file.

## Notes

  * 2024-04-24: Updated profiles to work with PrusaSlicer 2.9.2. Adjusted
    speed and quality parameters based on testing. Specifically, settings
    for PolyLite PLA increased cooling to reduce swelling and distortion.
    Speeds were increased for the *0.4mm High Speed Taz* profile, which still
    provides reasonably good quality for larger structural prints.

  * Wipe temperatures for calibration use an expression based on the bed and
    nozzle temperature of the material. This gets reasonably close to correct
    wipe temperatures for common materials such as PLA. However, for materials
    with some higher printing temperatures don't precisely fit the curve.

    ```
    {temperature[0] * 0.848 + bed_temperature[0] * 0.135 - 36.8}
    ```

    To guarantee that the nozzle is clean, the print will pause following wipe
    and before probe in all Taz models capable of automatic probing. Probe
    temperature is fixed at 145 deg C.
