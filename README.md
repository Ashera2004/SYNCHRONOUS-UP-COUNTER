### SYNCHRONOUS-UP-COUNTER

**AIM:**

To implement 4 bit synchronous up counter and validate functionality.

**SOFTWARE REQUIRED:**

Quartus prime

**THEORY**

**4 bit synchronous UP Counter**

If we enable each J-K flip-flop to toggle based on whether or not all preceding flip-flop outputs (Q) are “high,” we can obtain the same counting sequence as the asynchronous circuit without the ripple effect, since each flip-flop in this circuit will be clocked at exactly the same time:

![image](https://github.com/naavaneetha/SYNCHRONOUS-UP-COUNTER/assets/154305477/d5db3fa0-e413-404c-b80e-b2f39d82e7e8)


![image](https://github.com/naavaneetha/SYNCHRONOUS-UP-COUNTER/assets/154305477/52cb61eb-d04b-442d-810c-31185a68410b)

Each flip-flop in this circuit will be clocked at exactly the same time.
The result is a four-bit synchronous “up” counter. Each of the higher-order flip-flops are made ready to toggle (both J and K inputs “high”) if the Q outputs of all previous flip-flops are “high.”
Otherwise, the J and K inputs for that flip-flop will both be “low,” placing it into the “latch” mode where it will maintain its present output state at the next clock pulse.
Since the first (LSB) flip-flop needs to toggle at every clock pulse, its J and K inputs are connected to Vcc or Vdd, where they will be “high” all the time.
The next flip-flop need only “recognize” that the first flip-flop’s Q output is high to be made ready to toggle, so no AND gate is needed.
However, the remaining flip-flops should be made ready to toggle only when all lower-order output bits are “high,” thus the need for AND gates.

**Procedure**

1. Create a New Verilog Project in Quartus:

    • Open Quartus Prime software.
   
    • Create a new project and file (Verilog HDL).
   
2. Write Verilog Code for the 4-bit Synchronous Up Counter:

    • Define the module, inputs, and outputs.
    • Use JK flip-flops and connect them in a way that each higher-order flip-flop toggles based on the output of the previous flip-flop.

3. Simulate and Verify the Functionality:

    • Compare the simulation results with the expected truth table to verify correctness.
   

**PROGRAM**


![synchronous_up_code](https://github.com/user-attachments/assets/9f74ceb4-a7f4-4fcb-bcba-84eae7170665)



Developed by: A S SIDDARTH 

RegisterNumber: 212224040316


**RTL LOGIC UP COUNTER**


![synchronous_up_rtl](https://github.com/user-attachments/assets/1a53b42c-b2a4-40c9-b0a7-214f2334e537)


**TIMING DIAGRAM FOR IP COUNTER**


![synchronous_up_waveform](https://github.com/user-attachments/assets/10859e94-1bf6-4497-8c57-534a937f60b6)



**RESULTS**

The 4-bit synchronous up counter has been successfully implemented and simulated in Quartus Prime using Verilog. The counter operates as expected, incrementing the output by 1 on each clock pulse.
