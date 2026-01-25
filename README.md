# PTC Heated bed fans mod for Voron 2.4 Printers
Installed on Voron 2.4 bed rails. 

Can be placed on the outside, center or both.

Outer placement will be covered by the bed for 300 and 350 size but exposed on 250 size.

Mods that lift the bed such as Whoppingpochard kinematic bed mount are highly recommended 
to increase air flow and prevent damage to the bed heater.

## Es ist "verboten"

:fire: :fire: :fire:

Installation of this mod involves wiring mains AC voltage and addition of heaters without thermistor feedback. 

Careful wiring and component selection can reduce the risk of injury or fire, 
but only similar to the existing components of a v2.4 but never zero.

This mod should not be attempted without experience and caution.

:fire: :fire: :fire:

**Do NOT ask about this mod in the Voron Design Discord.**

---

## Design
* 
* emphasis on flat 

### Results
* A twin bedburner test rig setup:
  * <img src="Pictures/test_setup_uncovered.jpg" alt="test_setup_uncovered" width="400"/>
  * <img src="Pictures/test_setup_covered.jpg" alt="test_setup_covered.jpg" width="400"/>
  * Thermocouples were placed at the fan intake, on the block surface and at the block exhaust.
  * Combined amperage was measured and recorded along with temperature readings.
  * was inside an thinly insulated box with a simulated V2.4 configuration.
  * Heaters output over 70 watts each at 25C ambient.
  * Output dropped to roughly 60 watts each at 75C ambient.
* Twin bedburner setup installed in a v2.4 300:
  * <img src="Pictures/prototype_install.jpg" alt="prototype_install" height="500"/>
  * Stock panels and doors, stock exhaust, no blanket or insulation.
  * Nevermore micro v6 recirculating and exaust fan off.
  * Heatsoaking bed at 105C and 100% bedburner.
  * Chamber temperature reached stable 65C.

---

## Parts List
* Heater block
  * Heatsink - 50mm x 50mm x 20mm
  * Machined with component pockets and tapped holes.
  * For best results use a CNC Mill.
  * Can be machined with hand tools if you have the resolve.
    * 3D printable guides and templates provided.
    * Drill guide uses 2.0mm bit. Step up to 2.5mm bit for M3 tap.
    * Have multiple drill bits. You will break multiple.
    * Have multiple M3 start & end taps. You will likely break one.
    * Drill/tap depth is 4mm
    * Use a 5/16" OD Router bushing for router templates
    * Prototype set was made with hand tools. It was painful.
* Mouting brackets
  * Cut and bend in 16ga steel using the DXF files.
  * Mirror pairs can be made using bend up and bend down.
  * Prototype set made with SendCutSend.
* Component straps
  * Cut and bend in 22ga steel using the DXF files.
  * One ptc and one tswitch strap each.
  * Prototype set made with SendCutSend.
* PTC heater
  * Aluminum shell PTC heater.
  * Nominal size 35mm x 20mm x 5mm size.
  * Quality control is loose so test draw and max temp before usage.
* Thermal switch (tswitch)
  * KSD9700 insulated bimetal temperature/thermostat switch.
  * Recommended 120C Normally Closed.
  * Quality control is loose so test trigger temp before usage.
* Optional thermal paste/grease
  * use to improve conductivity between PTC shell or thermal switch and heater block.
  * operation temperature should be higher than PTC or Thermal switch rating.
* Fan duct
  * Typical voron print settings.
  * 2 x printed screw diam spacers are optional.
* 5015 radial (blower) fan
* 2 x short M3 heatset insert (M3 x 4.6mm x 3mm)
  * not common but [CNC Kitchen](https://cnckitchenus.store/products/heat-set-insert-m3-x-3-short-version-100-pieces) make them.
* 4 x M3, 8mm BHCS/SHCS - for the PTC and tswitch.
* 2 x M3, 4mm BHCS/SHCS - for block to bracket.
* 2 x M3, 18mm BHCS/SHCS - for fan to duct.
  * Not a common size. Cut down longer screws.
* 1 x M3, 6mm BHCS/SHCS - for bracket to extrusion.
* 1 x M3, 8mm BHCS/SHCS - for duct to extrusion.
* 2 x 2020 M3 t-nuts (twist-in or roll-in preferred).
