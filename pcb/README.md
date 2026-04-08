# ESPHome RGBCCT LED Controller PCB

<p align="center">
  <img src="pcb/meta/esphome-rgbcct-led-controller-top-view.png" width="48%" />
  <img src="pcb/meta/esphome-rgbcct-led-controller-side-view.png" width="48%" />
</p>

The PCB is designed in [KiCad](https://www.kicad.org/). Fabrication and is tuned toward [JCLPCB](https://jlcpcb.com/). I using my [Whizoo Controleo3](https://whizoo.com/) oven to handle all but the Thru-Hole stuff which is hand soldered.

* **Rev A**: Has been fabricated, assembled, tested and is use in four places. There is one issue TMP1075 (U1) is connected to VINP and will burn when powered by 24V and must be left off the PCB.

## Testing Notes

Only the 5A configuration has been tested. Short circuit on LED outputs will not damage the board but the red LED will not light up. This type of short circuits will recover automatically recover when removed. Short circuits on the fan connector will cause the red LED to light up and. Short circuits of this type are latching and require power-cycling to release. Over-voltage and Under-Voltage Lo ck Out work fine.

## Schematic
<p align="center">
    <a href="pcb/esphome-rgbcct-led-controller-schematic.pdf"><img src="pcb/meta/esphome-rgbcct-led-controller-schematic.png" width="70%"></a> <br />
    Schematic
</p>

### Do Not Populate (DNP) Notes

TMP1075 (U1) cannot be populated due to a PCB error. It will burn with 24V Vin.

## Bill of Materials
<p align="center">
    <a href="https://htmlpreview.github.io/?https://github.com/mikelawrence/esphome-rgbcct-led-controller/blob/main/pcb/interactive-bom/index.html"><img src="pcb/meta/esphome-rgbcct-led-controller-bom.png" width="70%"></a> <br />
    Interactive BOM
</p>

## PCB Info

* 6 layers with many vias to support high currents. vias should be filled to improve thermals.
* Two configurations, 5A Continuous, 10A Short Circuit and 10A Continuous and 20A Short Circuit.
* Dimensions are 100mm X 45mm.
* Requires oven reflow or hot air to assemble most components.

