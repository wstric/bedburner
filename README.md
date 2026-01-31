# PTC Heated bed fans mod for Voron 2.4 Printers
Spicy _bed_ fan mod with an "after _burner_" -> BedBurner.

Installed on Voron 2.4 bed rails. Can be placed on the outside, center or both.

Outer placement will be covered by the bed for 300 and 350 size but exposed on 250 size.

Requires raising the bed for clearance and to prevent damage to the bed heater.
Mods like Whoppingpochard kinematic bed mount do this with other benefits.

## Es ist "verboten"

:fire: :fire: :fire:

Installation of this mod involves wiring mains AC voltage and addition of heaters without thermistor feedback. 

Careful wiring and component selection can reduce the risk of injury or fire, 
but only similar to the existing components of a v2.4 but never zero.

This mod should not be attempted without experience and caution.

:fire: :fire: :fire:

**Do NOT ask about this mod in the Voron Design Discord.**

---

## Design (WIP)
* The 

### Results
* Twin BedBurner test rig setup:
  * <img src="Pictures/test_setup_uncovered.jpg" alt="test_setup_uncovered" width="400"/>
  * <img src="Pictures/test_setup_covered.jpg" alt="test_setup_covered.jpg" width="400"/>
  * Thermocouples were placed at the fan intake, on the block surface and at the block exhaust.
  * Combined amperage was measured and recorded along with temperature readings.
  * was inside an thinly insulated box with a simulated V2.4 configuration.
  * Heaters output over 70 watts each at 25C ambient.
  * Output dropped to roughly 60 watts each at 75C ambient.
* Twin BedBurner setup installed in a v2.4 300:
  * <img src="Pictures/prototype_install.jpg" alt="prototype_install" height="500"/>
  * Stock panels and doors, stock exhaust, no blanket or insulation.
  * Nevermore micro v6 recirculating and exaust fan off.
  * Heatsoaking bed at 105C and 100% BedBurner.
  * Chamber temperature reached stable 65C. 
  * Measured at gantry rear extrusion with toolhead centered and 120mm over bed

## Parts List
* Machined heater block
* Cut and bent bracket and straps
* PTC heater and thermal switch
* 5015 radial (blower) fan
* 3D printed fan duct
* Assorted M3 hardware

### [Detailed BOM](./README_bom.md)

## Instructions

### [Assembly](./README_assembly.md) __WIP__

### [Configuration](./README_config.md)
