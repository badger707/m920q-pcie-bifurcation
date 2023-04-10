# m920q-pcie-bifurcation

![](https://github.com/badger707/m920q-pcie-bifurcation/blob/main/pictures/lenovo_tiny_bif.jpeg)

Lenovo M920Q and M720Q PCIe x8 bifuration to x4x4 hardware mod by soldering missing components to the board.

# PCIe x8 bifurcation mod to x4x4 <br><br>
<b> *** It looks like this might work, placeholder, WIP. ***</b><br>
Referring to ![this](https://forums.servethehome.com/index.php?threads/lenovo-thinkcentre-thinkstation-tiny-project-tinyminimicro-reference-thread.34925/page-25#post-351254) post on STH, M720Q/M920Q models have the x8 PCI-E slot directly wired to the CPU.<br>
Looking at soldered SMD components and board schematics, I see board is in CFG[6:5]:1:0" configuration, which is "10 = 2 x8 PCI Express" mode.
This makes sense, we have lines 0-7 in slot available. Goal would be to make "CFG[6:5]:0:0" configuration which will give "00 = 1 x8, 2 x4 PCI Express" mode. <br><br>
![](https://github.com/badger707/m920q-pcie-bifurcation/blob/main/pictures/bifurcation_table1.jpeg)
<br><br>
After that, need to reverse PCIe lines (0-7 --> 7-0) with CFG[2]:0 configuration which should give us x4x4 lanes. This looks too easy to be true, need some testing...<br>
![](https://github.com/badger707/m920q-pcie-bifurcation/blob/main/pictures/bifurcation_map2.jpg)

## Testing
Does not work with Supermicro AOC-SLG3-2M2. Now ordered this x8 adapter for further testing [https://www.amazon.de/dp/B09MSB4TXT](https://www.amazon.de/dp/B09MSB4TXT)<br><br>
## Components location on the board
> placeholder, wip

