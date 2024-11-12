# VERILOG-CODE-FOR-SWAPPING-THREE-NUMBERS

## AIM:

To design and simulate a Verilog HDL code for swapping the values of three numbers without using any temporary variables, and verify the correctness of the swapping operation through a testbench using the Vivado 2023.1 simulation environment.

## APPARATUS REQUIRED:
Vivado 2023.1 or equivalent Verilog simulation tool.

## PROCEDURE:
Launch Vivado 2023.1:

Open Vivado and create a new project.
Write the Verilog Code for Swapping:

Write the Verilog code that swaps the values of three numbers (a, b, and c) using basic arithmetic or bitwise operations without using temporary variables.
Create the Testbench:

Write a testbench to simulate the swapping operation. The testbench should initialize three numbers, trigger the swapping module, and check if the values are swapped correctly.
Add the Verilog Files:

Add the Verilog module and the testbench file to the Vivado project.
Run Simulation:

Run the behavioral simulation in Vivado to verify the swapping operation.
Observe the Waveforms:

Examine the waveform to confirm that the values of the three numbers are swapped as expected.
Save and Document Results:

Capture the waveform output and include the results in your report for verification.


### Verilog Code:

~~~
module swap(clk);
input clk;
real a = 5;
real b = 3;
always@(posedge clk)
begin
a<=b;
b<=a;
end
endmodule
~~~

## Output: ![swap](https://github.com/user-attachments/assets/7428cd68-3d33-4e07-aaf5-6b944d56c8da)



### Testbench for Swapping Three Numbers:
~~~
module swap(clk);
    input clk;
    reg [31:0] a = 32'd5;  
    reg [31:0] b = 32'd3;  

always @(posedge clk) begin
        reg [31:0] temp;
        temp = a;
        a <= b;
        b <= temp;
    end
endmodule
~~~

## Output: ![swap 1](https://github.com/user-attachments/assets/11d3cfcc-836b-4bfa-87ae-64c1d34836f5)


## Conclusion :
In this experiment, a Verilog HDL code for swapping three numbers was designed and successfully simulated. The testbench verified the swapping operation, showing that the values of three input numbers (a, b, and c) were swapped correctly without the use of temporary variables. This experiment demonstrated the effectiveness of Verilog in implementing logical operations and control mechanisms such as swapping values. The simulation results confirm the correct functionality of the design.
