# RS485-CH340

[![Order from OSH Park](https://oshpark.com/assets/badge-5b7ec47045b78aef6eb9d83b3bac6b1920de805e9a0c227658eac6e19a045b9c.png)](https://oshpark.com/shared_projects/ijwz2rTz)

![front](doc/front.png)

![back](doc/back.png)

## PCB
![PCB](doc/pcb.png)

## Schematic

![schematic](doc/schematic.png)

The BOM is in the doc folder.

## RS485 configuration:

The built-in CH340 3.3V LDO can provide a 3.3V supply for the RS485 transceiver which makes populating the linear voltage regulator U3 (XC6206P332MR) optional. For most applications it's better to populate U3 since the maximum number of RS485 nodes that can be connected to the bus might be limited by the current that the internal LDO can provide.

Note: SW1 controls "TX-RX echo" (pin1-1 closed) or "no echo" (pin2-3 closed, this is standard RS485 functionality). If switching isn't required the pads can be bridged with a bit of solder. Most people won't need switching and in a re-design I would certainly replace SW1 with a jumper.
