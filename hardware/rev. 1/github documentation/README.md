## TESEO-LIV3F Breakout Board

This repo represents a [Teseo-LIV3F](https://www.st.com/en/positioning/teseo-liv3f.html) tiny GNSS Module  breakout board, purposed to check around and play with the module itself.

<img width="400px" src="https://user-images.githubusercontent.com/15846193/63805964-d4523200-c91a-11e9-9adf-0ff3d9ac2a98.png" />
<img width="400px" src="https://user-images.githubusercontent.com/15846193/63806015-ec29b600-c91a-11e9-9ca8-fdc9a693bfe2.png" />

### Features



### Schematic

The schematic was developed using [KiCAD][ec3408c0] ver. 5.0.2.

Main components included in the schematic are the GNSS module [TESEO-LIV3F][e3990006] module, RF amplifier (LNA), SAW RF filter, power supply circuit (converter) as well as some additional RF and filtering components.

[ec3408c0]: http://kicad-pcb.org/ "KiCAD"
[e3990006]: https://www.st.com/en/positioning/teseo-liv3f.html "TESEO-LIV3F"




- BGA725L6 is used as LNA. The LNA provides 20.0 dB gain and 0.65 dB noise
figure at a current consumption of 3.6 mA. Next TDK's BG
For filtering the output signal from the amplifier a SAW RF filter
- the bypassing circuit is added
- blocking capacitors
- battery

_schematic_ <br />
<img width="800px" src="https://user-images.githubusercontent.com/15846193/63805748-66a60600-c91a-11e9-800a-514d694b7f79.png" />

The ST1S12 is a step down DC-DC converter optimized for powering low-voltage digital cores in HDD applications and, generally, to replace the high current linear solution when the power dissipation may cause high heating of the application environment. It provides up to 0.7 A over an input voltage range of 2.5 V to 5.5 V. A high switching frequency (1.7 MHz) allows the use of tiny surface-mount components. In addition to the resistor divider to set the output voltage value, only an inductor and two capacitors are required. Moreover, a low output ripple is guaranteed by the current mode PWM topology and by the use of low ESR SMD ceramic capacitors. The device is thermally protected and the current is limited to prevent damage due to accidental short-circuit. The ST1S12 is available in the TSOT23-5L package.

### PCB design

The PCB is designed as standard 2 layers module. The LNA, SAW filter and GNSS module and most of the RF components are placed on the top side of the board. The power supply and the filtering capacitors are placed on the bottom side of the board. By the bypassing circuit (R2, R3) the input signal could be routed directly to the input of the GNSS module so the mounting of the LNA and the SAW filer could be skipped. The PCB is designed as a breadboard friendly module.

_top side_ <br />
<img width="400px" src="https://user-images.githubusercontent.com/15846193/63806091-19766400-c91b-11e9-8c45-199750adbfcc.png" />

_bottom side_ <br />
<img width="400px" src="https://user-images.githubusercontent.com/15846193/63806137-36ab3280-c91b-11e9-9f75-7150b648044f.png" />

### BOM

You can find the list of components

### Project Status

- not tested yet

### Ordering

The PCB can be purchased from [PCBs.io](https://PCBs.io/share/zal7j) web store.

## License
