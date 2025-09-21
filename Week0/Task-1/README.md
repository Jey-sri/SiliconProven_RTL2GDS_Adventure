### 📝 Task 1: RTL to GDSII Flow Summary

The RTL-to-GDSII flow is the complete process of converting a high-level Register Transfer Level (RTL) design into a physical layout (GDSII) ready for fabrication. This process is essential for manufacturing integrated circuits (ICs).

#### Key Stages of the Flow:

1.  **RTL Design:** The design starts with writing the chip's behavior in a Hardware Description Language (HDL) like Verilog. This stage defines the logic and functionality of the circuit.
2.  **Logic Synthesis:** The RTL code is translated into a gate-level netlist. Open-source tools like **Yosys** map the design to a standard cell library, optimizing for area, speed, and power.
3.  **Physical Design:** This is where the virtual design becomes a physical layout. It includes several sub-stages:
    * **Floorplanning:** Defining the chip's core size and placing major blocks.
    * **Power and Ground Planning:** Creating the power delivery network.
    * **Placement:** Arranging the standard cells on the chip.
    * **Clock Tree Synthesis (CTS):** Building a clock network to distribute the clock signal evenly.
    * **Routing:** Connecting all the standard cells with wires.
4.  **Design Rule Check (DRC) & Layout vs. Schematic (LVS):** Before tapeout, the physical layout is verified to ensure it meets manufacturing rules (DRC) and matches the original netlist (LVS). **Magic VLSI** is a tool used for this.
5.  **Tapeout Ready (GDSII):** The final output is a GDSII file, a binary format that contains the complete chip layout and is sent to the fabrication foundry.
