# AXI4-Lite Master-Slave Communication with Fork-Join Transactions in SystemVerilog
==================================================================================

📌 Overview
-----------
This project implements and verifies an AXI4-Lite protocol-based communication system between a master and a slave module using SystemVerilog. The design simulates multiple read and write transactions executed in parallel using the fork-join construct in the testbench.

The simulation is performed in Vivado Simulator (XSim), with output logs printed to the TCL console and signal transitions visualized via the waveform viewer.

🎯 Aim
------
To design and verify an AXI4-Lite master-slave communication system using SystemVerilog, perform concurrent read and write transactions using the fork-join construct in the testbench, and validate functional correctness via simulation output and waveform analysis.

🧠 Key Concepts
---------------
- AXI4-Lite Protocol: A lightweight version of the AXI protocol for memory-mapped read/write.
- Master-Slave Design: Master initiates read/write; slave responds accordingly.
- Fork-Join: SystemVerilog construct to allow parallel execution of tasks in simulation.
- Vivado XSim: Simulation tool used for verifying design behavior and waveforms.

🏗️ Project Structure
--------------------
axi4_lite_master.sv        → AXI4-Lite Master module  
axi4_lite_slave.sv         → AXI4-Lite Slave module  
top_axi4_lite.sv           → Top-level integration of master and slave  
tb_axi4_lite.sv            → Testbench using fork-join for concurrent transactions  
axi4_lite.vcd              → Waveform dump file (generated during simulation)  
README.txt                 → Project documentation (this file)

🔬 Testbench Features
---------------------
- Executes multiple read and write transactions concurrently using fork-join.
- Distinct data and address for each transaction.
- $display output for each transaction is printed to the TCL console.
- Generates VCD waveform for visual analysis.
- Final message indicates all transactions are completed.

▶️ How to Run
-------------
1. Open Vivado (2023.2 or later).
2. Create a project and add all `.sv` files to simulation sources.
3. Set `tb_axi4_lite.sv` as the simulation top module.
4. Run behavioral simulation.
5. View:
   - TCL console logs for transaction flow
   - Waveform viewer for signal activity (via axi4_lite.vcd)

✅ Sample Output
----------------
[0] Starting AXI4-Lite Master-Slave Verification  
[10] Master: Writing A5A5A5A5 to Address 0x10  
[15] Master: Reading from Address 0x10 → Data: A5A5A5A5  
[20] Master: Writing 5A5A5A5A to Address 0x20  
[25] Master: Reading from Address 0x20 → Data: 5A5A5A5A  
[30] All fork-join transactions completed successfully  

📚 Learning Outcomes
--------------------
- Deepen understanding of the AXI4-Lite protocol.
- Gain experience in SystemVerilog testbench design.
- Learn parallel simulation techniques using fork-join.
- Build skills in debugging and protocol verification using TCL console and waveform viewer.


