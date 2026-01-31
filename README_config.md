# BedBurner Software Configuration

Klipper does not make chamber heaters easy.
They are, in effect, modeled as bed heaters which causes complications in most configurations.
The two main paths for configuring are to work around the Klipper or implement custom control.

## Klipper Control Solution

Klipper control gets hacky, but has the advantage of being controlled in real time.
It is always running and will not be blocked by the command queue.
The macro is also much easier to understand even if what is can do is narrow.
The only real downside it you are working around the limitations and opinions of Klipper.
Depending on your setup this might be no downside at all.

Some limitations you might need to work around include:
  * Heaters can only be controlled by a temperature sensor
  * Using verify_heater is impossible using the chamber temp. No safety for you.
  * Nether heater_fan or controller_fan can cycle off except during cool down.
  * If you have one chamber termistor, duplicate pin validation.

Provided example barely tested in Kalico v0.12 but provides control of
chamber heater & fan, filter and exhaust.

#### [klipper control example config](/Firmware/klipper/klipper_control)

## Custom Control Solution
Custom control gives a lot of freedom to customize how it behaves.
I have implemented my own version using delayed_gcode which makes it simple to implement,
but comes with the limitation that it can be interrupted temporally by long running commands
(like a typical print start macro).

The configuration is simple configuration and can model the filter, exhaust, heater fan
and heater element as `fan_generic` so that a macro may control without Klipper stepping in.
Practically, you are limited to watermark (aka bang-bang) control in a custom macro,
but this is quite suitable for chamber temperature regulation.

Provided example was extensively tested in Klipper v0.12 and provides control of
chamber heater & fan, filter and exhaust.

#### [custom control example config](/Firmware/klipper/custom_control)

---

For examples given above chamber temperature control is abstracted by `HEAT_CHAMBER` and `COOL_CHAMBER` macros.
The `HEAT_CHAMBER` should be called in your print start (and heatsoak if you have one) macros.
`COOL_CHAMBER` should be called in your print end macro.
