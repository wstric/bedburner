# BedBurner Detailed BOM

## Common Components 
* Heater block
  * Heatsink - 50mm x 50mm x 20mm
  * Machined with component pockets and tapped holes
  * Variant of block should match the thermal fail-safe option selected
  * Detailed instructions in [fabrication section](./README_fabrication.md#Heater-Heatsink)

* Mouting bracket
  * Cut and bend from 16ga mild steel
  * Requires front, rear or both brackets
    * Rear bracket least compact but accessible screws makes easier to install and service
    * Front bracket covers extrusion screws and makes hard to align
    * Can use both front and rear brackets for extra sturdy mounting
  * STEP models and DXF files are provided
  * Detailed instructions in [fabrication section](./README_fabrication.md#Heater-Bracket)

* PTC heater
  * Aluminum shell PTC heater
  * Nominal size 35mm x 20mm x 5mm size
  * Quality control is loose so test current draw and max temp before usage

* PTC component strap
  * Cut from 22ga mild steel
  * Detailed instructions in [fabrication section](./README_fabrication.md#Component-Straps)

* 5015 radial (blower) fan
  * Recommended to use fans rated for high performance and chamber temperatures

* Fan duct
  * [STLs](/STL/fan_duct) provided
  * Typical voron print settings
    * ABS/ASA, 0.4mm extrusion, 0.2mm layer, 4 wall, etc.
  * 2 x printed screw diam spacers are optional

* 2 x M3, 8mm BHCS/SHCS - for PTC strap
* 2 x M3, 6mm BHCS/SHCS - for bracket to extrusion (per bracket)
* 2 x M3, 4mm BHCS/SHCS - for block to bracket (per bracket)
* 2 x M3, 18mm BHCS/SHCS - for fan to duct
  * Not a common size
  * Cut down longer screws if needed
* 1 x M3, 8mm BHCS/SHCS - for duct to extrusion
* 2 x 2020 M3 t-nuts (twist-in or roll-in preferred) (per bracket)

* 2 x short M3 heatset insert (M3 x 4.6mm x 3mm)
  * not common but [CNC Kitchen](https://cnckitchenus.store/products/heat-set-insert-m3-x-3-short-version-100-pieces) makes them

* One thermal safety option
  * Not recommended to rely on PTC maximum temperature in case of failure
  * Thermal fail-safe options provided below with required BOM

* Optional thermal paste/grease
  * use to improve conductivity between PTC shell or thermal switch/fuse and heater block
  * operation temperature should be higher than PTC or thermal switch/fuse rating

## Thermal Switch Option

* (Use ptc_tswitch variant block)

* Thermal switch
  * KSD9700 insulated bimetal temperature/thermostat switch
  * Recommended 120C Normally Closed
  * Quality control is loose so test trigger temp before usage

* TSwitch component strap
  * Cut from 22ga mild steel.
  * Detailed instructions in [fabrication section](./README_fabrication.md#Component-Straps)

* 2 x M3, 8mm BHCS/SHCS - for tswitch strap

## Thermal Fuse Option

* (Use ptc_tfuse variant block)

* Thermal fuse
  * RH series ceramic thermal cut-off fuse
  * Commonly used as a fail-safe for voron bed heaters
  * Recommended 125C 10A 250V rating

* 1 x M3, 8mm FHCS - for tfuse.
  * SHCS and BHCS can also work but might need a washer

## Thermistor Option

* (Recommended ptc_tfuse variant block)

* M3 hex screw thermistor
  * 3mm length of M3 x 0.5mm screw thread
  * Typically 100K 3950 or 104GT-2
