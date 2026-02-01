# THEORY:
On this day, we learned the principles of effective floorplanning and gained an introduction to standard library cells. The following key concepts were covered:

Utilization Factor and Aspect Ratio

After generating the RTL netlist, the design consists of gates, flip-flops, and multiplexers, which are treated as individual blocks during floorplanning. These blocks are placed within the core area of the chip.

Utilization Factor indicates how much of the core area is occupied by the standard cells:

Utilization Factor = Area occupied by the netlist / Total core area

Typically, the utilization is kept around 50% to allow routing resources and reduce congestion.

Aspect Ratio defines the shape of the core and is calculated as:

Aspect Ratio = Height / Width

Pre-Placed Cells

Pre-placed cells are reusable functional blocks that are frequently accessed within the design. Instead of duplicating these blocks multiple times, they are placed at fixed locations in the layout. These locations are reserved and cannot be used by other logic.

Common examples include memory blocks, clock-gating cells, multiplexers, and comparators. Floorplanning involves organizing the remaining logic around these pre-placed cells.

Decoupling Capacitors

Decoupling capacitors are used to stabilize the power supply and keep voltage levels within acceptable noise margins. Due to parasitic resistance, capacitance, and inductance in interconnects, voltage drops may occur, leading to unstable circuit behavior. Decoupling capacitors provide local charge storage and help maintain consistent power delivery.

Power Planning

Power planning ensures reliable power distribution across the chip. When many cells switch simultaneously, voltage fluctuations such as IR drop and ground bounce can occur. To mitigate this, multiple power and ground lines are distributed across the layout, ensuring stable operation and preventing noise-related failures.

Repeaters

Repeaters are inserted between distant logic blocks to restore signal integrity. Long interconnects can cause signal degradation, and repeaters help maintain proper signal levels. However, inserting repeaters increases area usage and slightly reduces the utilization factor.

Cell Design and Characterization Flow

The cell design flow consists of inputs, design steps, and outputs:

Inputs: Process Design Kit (PDK), DRC/LVS rules, SPICE models, and user specifications

Design Steps: Circuit design, layout creation, and characterization

Outputs: CDL file, LEF, SPICE netlist, and timing, power, and noise libraries

Characterization Process

In the characterization flow, SPICE models are read, extracted netlists are analyzed, buffer behavior and drive strengths are evaluated, and input stimuli are applied. Output load capacitance is defined, power and ground are connected, and simulation control commands are executed to generate accurate timing and power data.
![image alt](https://github.com/Sivananth-G/VSDNASSCOM---Digital-VLSI-SoC-design-and-planning/blob/6040fe3270712910a95a16197015a1fbabe8dd00/Day2/Screenshot%202026-01-29%20214838.png)

![image alt](https://github.com/Sivananth-G/VSDNASSCOM---Digital-VLSI-SoC-design-and-planning/blob/6040fe3270712910a95a16197015a1fbabe8dd00/Day2/Screenshot%202026-01-30%20204355.png)

![image alt](https://github.com/Sivananth-G/VSDNASSCOM---Digital-VLSI-SoC-design-and-planning/blob/6040fe3270712910a95a16197015a1fbabe8dd00/Day2/Screenshot%202026-01-30%20204529.png)

![image alt](https://github.com/Sivananth-G/VSDNASSCOM---Digital-VLSI-SoC-design-and-planning/blob/6040fe3270712910a95a16197015a1fbabe8dd00/Day2/Screenshot%202026-01-30%20204638.png)

![image alt](https://github.com/Sivananth-G/VSDNASSCOM---Digital-VLSI-SoC-design-and-planning/blob/6040fe3270712910a95a16197015a1fbabe8dd00/Day2/Screenshot%202026-01-30%20204716.png)

![image alt](https://github.com/Sivananth-G/VSDNASSCOM---Digital-VLSI-SoC-design-and-planning/blob/6040fe3270712910a95a16197015a1fbabe8dd00/Day2/Screenshot%202026-01-30%20204746.png)

![image alt](https://github.com/Sivananth-G/VSDNASSCOM---Digital-VLSI-SoC-design-and-planning/blob/6040fe3270712910a95a16197015a1fbabe8dd00/Day2/Screenshot%202026-01-30%20205019.png)

![image alt](https://github.com/Sivananth-G/VSDNASSCOM---Digital-VLSI-SoC-design-and-planning/blob/6040fe3270712910a95a16197015a1fbabe8dd00/Day2/Screenshot%202026-01-30%20205350.png)

![image alt](https://github.com/Sivananth-G/VSDNASSCOM---Digital-VLSI-SoC-design-and-planning/blob/6040fe3270712910a95a16197015a1fbabe8dd00/Day2/Screenshot%202026-01-30%20210845.png)

![image alt](https://github.com/Sivananth-G/VSDNASSCOM---Digital-VLSI-SoC-design-and-planning/blob/6040fe3270712910a95a16197015a1fbabe8dd00/Day2/Screenshot%202026-01-30%20211224.png)

![image alt](https://github.com/Sivananth-G/VSDNASSCOM---Digital-VLSI-SoC-design-and-planning/blob/6040fe3270712910a95a16197015a1fbabe8dd00/Day2/Screenshot%202026-01-30%20211326.png)

![image alt](https://github.com/Sivananth-G/VSDNASSCOM---Digital-VLSI-SoC-design-and-planning/blob/6040fe3270712910a95a16197015a1fbabe8dd00/Day2/Screenshot%202026-01-30%20211354.png)

![image alt](https://github.com/Sivananth-G/VSDNASSCOM---Digital-VLSI-SoC-design-and-planning/blob/6040fe3270712910a95a16197015a1fbabe8dd00/Day2/Screenshot%202026-01-30%20211743.png)

![image alt](https://github.com/Sivananth-G/VSDNASSCOM---Digital-VLSI-SoC-design-and-planning/blob/6040fe3270712910a95a16197015a1fbabe8dd00/Day2/Screenshot%202026-01-30%20211826.png)

![image alt](https://github.com/Sivananth-G/VSDNASSCOM---Digital-VLSI-SoC-design-and-planning/blob/6040fe3270712910a95a16197015a1fbabe8dd00/Day2/Screenshot%202026-01-30%20211945.png)

![image alt](https://github.com/Sivananth-G/VSDNASSCOM---Digital-VLSI-SoC-design-and-planning/blob/6040fe3270712910a95a16197015a1fbabe8dd00/Day2/Screenshot%202026-01-30%20212912.png)
