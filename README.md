# 4-BIT-RIPPLE-COUNTER

DHINESHKUMAR E ( 24900879 )

**AIM:**

To implement  4 Bit Ripple Counter using verilog and validating their functionality using their functional tables

**SOFTWARE REQUIRED:**

Quartus prime

**THEORY**

**4 Bit Ripple Counter**

A binary ripple counter consists of a series connection of complementing flip-flops (T or JK type), with the output of each flip-flop connected to the Clock Pulse input of the next higher-order flip-flop. The flip-flop holding the least significant bit receives the incoming count pulses. The diagram of a 4-bit binary ripple counter is shown in Fig. below.

![image](https://github.com/naavaneetha/4-BIT-RIPPLE-COUNTER/assets/154305477/cb4b74d4-31ab-4359-95d0-d22e67daba13)

In timing diagram Q0 is changing as soon as the negative edge of clock pulse is encountered, Q1 is changing when negative edge of Q0 is encountered(because Q0 is like clock pulse for second flip flop) and so on.

![image](https://github.com/naavaneetha/4-BIT-RIPPLE-COUNTER/assets/154305477/a573a7d6-014e-4e54-93e6-e2ac9530960b)

![image](https://github.com/naavaneetha/4-BIT-RIPPLE-COUNTER/assets/154305477/85e1958a-2fc1-49bb-9a9f-d58ccbf3663c)

**Procedure**

/** 1.Write the Verilog code in Quartus Prime for the 4-bit ripple counter.

2.Compile and run the program to ensure it is error-free.

3.Generate the RTL schematic to visualize the flip-flop connections.

4.Create nodes for the clock input (CLK) and counter outputs (Q0, Q1, Q2, Q3).

5.Simulate the design for multiple clock cycles to observe the ripple effect.

6.Verify the timing diagrams to ensure the counter toggles through all states (0000 to
1111).

7.Save the RTL schematic and timing diagrams for documentation and validation.*/

**PROGRAM**

```
module EX12(out,clk,rst);
input clk,rst;
output reg [3:0]out;
always @ (posedge clk)
begin
   if(rst)
     out<=0;
   else 
     out <= out-1;
end
endmodule
```

**RTL LOGIC FOR 4 Bit Ripple Counter**

![Screenshot 2024-12-26 140920](https://github.com/user-attachments/assets/3b314743-a8eb-4c64-aa68-ac595fe33275)

**TIMING DIGRAMS FOR 4 Bit Ripple Counter**

![image](https://github.com/user-attachments/assets/58c6762f-57fd-419f-8f2c-27d845cf8b0b)

**RESULTS**

 Thus the program executed succesfully.
 
