# bbakraid-cplds
Battle Bakraid CPLDs dumps.

Xilinx devices in this game PCB are known to fail over time, producing a variety of symptoms. Most common are:

* Wrong text layer element indexing: Text layer is shown with wrong tiles/letters.
* Fails in layers priorities: Text layer or sprites layer don't show properly.
* Game doesn't boot at all: as some of those devices manages the DMA and system bus arbitration.
* Issues when flipping screen
* some more...

Notice that those symptoms are usually related to a bad CPLD, but this is not always the reason of the fault.

Sometimes they could be mitigated by lowering the input voltage in the PCB (down to around 4.55V), but this is a workaround that will only work for some time until device will completely die.

So, here are the dumps for those CPLDs in order to replace them and perform a full repair.

## JTAG

**CN011 pinout:**

1. VREF
2. GND
3. TCK
4. TDO
5. TDI
6. TMS

## Files

They can be in-system programmed using JTAG connector (except for U048), or externally using a compatible programmer.

| File | Position | CPLD Model | Dumped by | Tested by |
| ---- | ---- | ---- | ---- | ---- |
| 1_xc95108_C_u0130.jed | U0130 | Xilinx XC95105 | [@sergiopolog](https://github.com/sergiopolog) | *trusted friend of [@Mikejmoffitt](https://github.com/Mikejmoffitt)* |
| 2_xc95144_T_u0626.jed | U0626 | Xilinx XC95144 | [@sergiopolog](https://github.com/sergiopolog) | [@sergiopolog](https://github.com/sergiopolog) & [@Mikejmoffitt](https://github.com/Mikejmoffitt) |
| 3_xc95108_U_u0719.jed | U0719 | Xilinx XC95105 | [@sergiopolog](https://github.com/sergiopolog) | *trusted friend of [@Mikejmoffitt](https://github.com/Mikejmoffitt)* |
| u048_afb_ct2.jed | U048 | Lattice MACH211 | [@Mikejmoffitt](https://github.com/Mikejmoffitt) | [@Mikejmoffitt](https://github.com/Mikejmoffitt) |

## Programming service

As we are talking of a pretty much valuable pcb nowadays and some specific hardware is needed to achieve the repair, I could offer a programming service (only CPLDs) for a *decent* price if you have a faulty PCB in the Europe area, with the aim to avoid repair services by thirds asking ridiculous amounts of money taking advantage of making these dumps public and the current high value of this pcb. Please, don't spent a big dollar feeding people whom using other's work to make big profit. This was made public to help retro arcade community with no aim of profit.

Keep in mind that I will not be responsible of damages or loss PCBs while shipping, and that should be managed by the owner of pcbs. I recommend fully-ensured shipping for the current marked cost of the PCB.

You can reach me on Twitter for more details: [@Recre_Piscis](https://twitter.com/Recre_Piscis)
