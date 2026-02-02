# PTC Heated bed fans mod for Voron 2.4 Printers
Spicy _bed_ fan mod with an "after _burner_" -> BedBurner.

Installed on Voron 2.4 bed rails. Can be placed on the outside, center or both.

Outer placement will be covered by the bed for 300 and 350 size but exposed on 250 size.

Requires raising the bed for clearance and to prevent damage to the bed heater.
Mods like Whoppingpochard kinematic bed mount do this with other benefits.

:fire: :fire: :fire:

> [!CAUTION]
> Installation of this mod involves wiring mains AC voltage and addition of heaters without thermistor feedback.
>
> Careful wiring and component selection can reduce the risk of injury or fire,
> but only similar to the existing components of a v2.4 but never zero.
>
> This mod should not be attempted without experience and caution.
> I am not responsible for any resulting damage or harm.

> [!Warning]
> Do NOT ask about this mod in the Voron Design Discord.

:fire: :fire: :fire:

## Design

The goal of this mod was to create a minium height chamber heater for the Voron V2.4 that
could slip into the unused space under the bed and provide enough thermal output to match
the extruder. This would allow the printer to more easily heatsoak at the same temperatures
that would be reached during printing. More active chamber temperature control was a bonus
and a slight increase in temperatures was welcome. While typically much more powerful,
existing setups were simply too bulky and had to mounted in the open or be in the way of
existing components.

After much research and trying to make hotend cartridge heater work I found the aluminum shell
PTC heater form factor. While lacking in surface area it is very compact, electrically isolated
and could be easily mounted heatsink. Balancing space, thermal out, and availability lead to
35mm x 20mm x 5mm nominal size PTC and 50mm x 50mm x 20mm heatsink. This left enough space for
safety features such as a thermal switch as a fail safe and further cap the maximum temperature.

Modifying the off the shelf heatsink ending up being one of the most challenging part. While
the steel brackets (metal for safety in the worst case, and steel for poor conductivity) would
have been impossible to make myself they were easy to outsource to services like SendCutSend.
The modified heatsink would have been prohibitive to outsource machined from raw stock and
a struggle to do with hand tools. There were easier ways to mount but was decided that retaining
components in pockets strapped in with screws was necessary for safety.

The resulting setup ended being a little too tall for a stock V2.4 bed spacers. This wasn't an
issue since the Whooping kinematic bed mod already gave plenty of height. Matched with common
5015 radial blower fans it two could be fit in betwee the bed extrusions and another two could
be hidden under a 300mm bed on the outside.

### Results
* Twin BedBurner test rig setup:
  * <img src="Pictures/test_setup_uncovered.jpg" alt="test_setup_uncovered" width="400"/>
  * <img src="Pictures/test_setup_covered.jpg" alt="test_setup_covered.jpg" width="400"/>
  * Thermocouples were placed at the fan intake, on the block surface and at the block exhaust.
  * Combined amperage was measured and recorded along with temperature readings.
  * was inside an thinly insulated box with a simulated V2.4 configuration.
  * Heaters output over 70 watts each at 25C ambient.
  * The block surface peaked at rough 80C in 25C ambient.
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

---

Special thanks to the Fabreeko discord and Delmar for tolerating these shenanigans. 
