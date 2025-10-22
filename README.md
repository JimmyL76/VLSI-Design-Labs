# VLSI-Design-Labs

Currently working on schematics/layouts for VLSI IC designs, including logic simulation, verification, custom layout/APR, and post-layout simulation.

## Tools

**EDA Tools**: Cadence Virtuoso (schematic/layout), NC Verilog (logic sim), Spectre (analog sim), Calibre (DRC/LVS/Parasitic Extraction), HSPICE (post-layout sim), PrimeTime (static timing analysis)

**Technology**: FreePDK45 (45nm CMOS)

## Lab 0 - Inverter (Completed)

- Basic inverter design (schematic & layout)
- Logic and analog simulation
- Physical verification (DRC/LVS)
- Parasitic extraction and post-layout simulation

<table>
  <tr>
    <td align="center">
      <strong>Inverter Schematic</strong><br>
      <img src="lab0/InvSchematic.png" alt="lab0schematic" style="width:80%; max-width:300px; height:auto;">
    </td>
    <td align="center">
      <strong>Initial Layout (DRC/LVS Passed)</strong><br>
      <img src="lab0/InvLayout1.png" alt="lab0layout1" style="width:100%; max-width:300px; height:auto;">
    </td>
    <td align="center">
      <strong>Cleaner Layout 2</strong><br>
      <img src="lab0/InvLayout2.png" alt="lab0layout2" style="width:100%; max-width:300px; height:auto;">
    </td>
  </tr>
</table>

*For the following, reach out on LinkedIn for more details or images!*

## Lab 1 - 4-Bit SRAM Memory Cell (Completed)

<img src="lab1/memcell.png" alt="lab1memcell" style="width:60%; max-width:250px; height:auto;">

**Part A: 4-Bit Memory Cell**

- Inverter characterization across input slews and output load capacitances (HSPICE)
- 4-bit latch-based memory array with area optimization
- Logical/physical verification (Spectre/HSPICE)

**Part B: 32x32 Memory Array**

- Simulate and measure worst-case access time (Spectre)
- Wire delay modeling/simulation using RC networks

## Lab 2 - 16-Bit Adder and ALU (Completed)

<img src="lab2/alu.png" alt="lab2alu" style="width:60%; max-width:250px; height:auto;">

**Part A: 16-Bit Adder**

- Created schematic for 16-bit adder with signed/unsigned add, sub, overflow bit, and increment/decrement
- Verified full functionality with NC Verilog test cases and waveform analysis
- Analyzed static timing delays with PrimeTime, optimizing for delay - including a Kogge-Stone adder, efficient set/clearing for increment/decrement, optimized decoder for control signals, FO4 buffers to reduce fanout delays, and buffers to isolate branching non-critical paths

**Part B: 16-Bit ALU**

- Designed ALU schematic to perform logic (OR, XOR, NOT, AND), compare, arithmetic (from previous adder), and shift operations
- Verified full functionality, with emphasis on correct logic vs arithmetic vs rotate shifting as well as arithmetic shifting overflow
- Optimized funnel shifter to minimize delay - reduce large fanout, place faster control signals on delay path before slower ones, ensure overflow bit from shifter utilizes the least amount of gates and logic levels possible
- Also optimized for the final critical path delay through the adder to compare operation 

## Lab 3 - Synchronous Serial Port (SSP) and Wishbone Bus Interface (In Progress)
