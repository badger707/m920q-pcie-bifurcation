# m920q-pcie-bifurcation

![](https://github.com/badger707/m920q-pcie-bifurcation/blob/main/pictures/lenovo_tiny_bif.jpeg)

Lenovo M920Q and M720Q PCIe x8 bifuration to x4x4 hardware mod by soldering missing components to the board.

# PCIe x8 bifurcation mod to x4x4 <br><br>
<b> *** It looks like this might work, placeholder, WIP. ***</b><br>
Looking at soldered SMD components and board schematics, I see board is in CFG[6:5]:1:0" configuration, which is "10 = 2 x8 PCI Express" mode.
This makes sense, we have lines 0-7 in slot available. Goal would be to make "CFG[6:5]:0:0" configuration which will give "00 = 1 x8, 2 x4 PCI Express" mode. <br><br>
![](https://github.com/badger707/m920q-pcie-bifurcation/blob/main/pictures/bifurcation_table1.jpeg)
<br><br>
After that, need to reverse PCIe lines (0-7 --> 7-0) with CFG[2]:0 configuration which should give us x4x4 lanes. This looks too easy to be true, need some testing...<br>
If this will work, we can stick Supermicro AOC-SLG3-2M2 or something similar to bifurcated PCIe slot. Need some testing over the weekend.<br><br>
![](https://github.com/badger707/m920q-pcie-bifurcation/blob/main/pictures/bifurcation_map2.jpg)

## Components location on the board
> placeholder, wip

