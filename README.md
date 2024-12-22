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

1. Type the program in Quartus software.

2. Compile and run the program.

2. Generate the RTL schematic and save the logic diagram.

4. Create nodes for inputs and outputs to generate the timing diagram.

5. For different input combinations generate the timing diagram.

**PROGRAM**

```
Developed by:AISHWARIYA S RegisterNumber:24900840

module exp11(out,clk,rstn);
input clk,rstn;
output reg [3:0]out;
always @ (posedge clk)
begin 
	if(!rstn)
		out<=0;
	else
		out <= out+1;
end
endmodule
```

Developed by:Kamlesh.y 
RegisterNumber:24003690


**RTL LOGIC UP COUNTER**
![image](https://github.com/user-attachments/assets/2fc0c7eb-069a-44c6-a0b2-9543b7e7c68b)


**TIMING DIAGRAM FOR IP COUNTER**
![396355021-99b5fe74-a743-4e8d-828d-e4f9b3ef2927](https://github.com/user-attachments/assets/5b2b3b76-9e72-49e7-ae0c-8302229b429a)


**TRUTH TABLE**

![image](https://github.com/user-attachments/assets/35e8ac5e-f4e9-4507-9d05-8164961e7d01)


**RESULTS**

4 bit synchronous up counter and validate functionality.
