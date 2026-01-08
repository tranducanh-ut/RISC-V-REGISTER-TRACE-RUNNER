============================================================
            RISC-V REGISTER TRACE RUNNER
============================================================

Author  : Tran Duc Anh
Project : RISC-V CPU Simulation
Tool    : Xilinx Vivado (xsim)
Purpose : Generate register update trace during simulation

------------------------------------------------------------
I. OVERVIEW
------------------------------------------------------------
This application is a console-based utility that:

- Runs a RISC-V CPU simulation using Vivado xsim
- Tracks changes of registers x0..x31 at each clock cycle
- Generates a trace log file named "regtrace.txt"
- Prints the trace output directly to the terminal

------------------------------------------------------------
II. REQUIRED DIRECTORY STRUCTURE
------------------------------------------------------------
The working directory must contain the following files:
  ouput folder: contain TracRunnerSetup.exe (IMPORTANT)          
  run_trace.bat          (main execution script)
  run_launcher.bat       (launcher script)
  README_TRACE.txt       (this guide)

  riscv_top.v
  regfile.v
  mem.v
  alu.v
  brc.v
  controller.v
  ImmGen.v
  lsu.v
  tb_regtrace.v

  sim_work/              (auto-generated during execution)

------------------------------------------------------------
III. HOW TO USE
------------------------------------------------------------

STEP 1:
- Go to Ouput folder 
- Double-click "TracRunnerSetup.exe" and tick "create shortcut"
- Choose the destinaton you want to save (you should remember your path because your output is loacated in this folder)


STEP 2:
- Read the instructions displayed in the terminal
- Press ENTER to continue

STEP 3:
- Enter the full path to vivado.bat
  Example:
    C:\Xilinx\Vivado\2024.2\bin\vivado.bat

STEP 4:
- Enter the full path to the memory initialization file (mem.h)
  Example:
    C:\Users\...\mem.h

------------------------------------------------------------
IV. OUTPUT
------------------------------------------------------------
After the simulation completes successfully:

- The file "regtrace.txt" will be generated in the sim_work
  directory
- You may open "regtrace.txt" with any text editor

------------------------------------------------------------
V. COMMON ISSUES
------------------------------------------------------------



1. Vivado does not start
   - Verify the vivado.bat path is correct

2. Simulation stops too early
   - Check the MAX_CYCLES parameter in tb_regtrace.v

------------------------------------------------------------
VI. NOTES
------------------------------------------------------------
- xsim runs inside sim_work/xsim.dir/
- The batch script automatically collects the output file
- All paths are handled internally by the launcher

============================================================
END OF README
============================================================
