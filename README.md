# NAME     :KARTHICKKUMAR.R

# ROLL NO  :23012023

# Experiment 05 Implementation of flipflops using verilog

### AIM: 
To implement all the flipflops using verilog and validating their functionality using their functional tables

## EQUIPMENTS REQUIRED

 HARDWARE REQUIRED:  – PC, Cyclone II , USB flasher
 SOFTWARE REQUIRED:   Quartus prime


### THEORY 
SR Flip-Flop
SR flip-flop operates with only positive clock transitions or negative clock transitions. Whereas, SR latch operates with enable signal. The circuit diagram of SR flip-flop is shown in the following figure.

![image](https://user-images.githubusercontent.com/36288975/167910294-bb550548-b1dc-4cba-9044-31d9037d476b.png)

This circuit has two inputs S & R and two outputs Qtt & Qtt’. The operation of SR flipflop is similar to SR Latch. But, this flip-flop affects the outputs only when positive transition of the clock signal is 
applied instead of active enable.The following table shows the state table of SR flip-flop.

![image](https://user-images.githubusercontent.com/36288975/167910648-ced88e69-869c-42e2-9718-a285a3902446.png)

Here, Qtt & Qt+1t+1 are present state & next state respectively. So, SR flip-flop can be used for one of these three functions such as Hold, Reset & Set based on the input conditions, when positive transition of clock signal is applied. The following table shows the characteristic table of SR flip-flop.
Present Inputs	Present State	Next State

![image](https://user-images.githubusercontent.com/36288975/167908180-5fc9d589-1cb5-41f5-b2c8-927e04f5f387.png)

By using three variable K-Map, we can get the simplified expression for next state, Qt+1t+1. The three variable K-Map for next state, Qt+1t+1 is shown in the following figure.

![image](https://user-images.githubusercontent.com/36288975/167908214-25b30a54-db20-4bcb-9385-5f93a1982a09.png)

The maximum possible groupings of adjacent ones are already shown in the figure. Therefore, the simplified expression for next state Qt+1t+1 is
Q(t+1)=S+R′Q(t)Q(t+1)=S+R′Q(t)

### D Flip-Flop
D flip-flop operates with only positive clock transitions or negative clock transitions. Whereas, D latch operates with enable signal. That means, the output of D flip-flop is insensitive to the changes in the input, D except for active transition of the clock signal. The circuit diagram of D flip-flop is shown in the following figure.
 
This circuit has single input D and two outputs Qtt & Qtt’. The operation of D flip-flop is similar to D Latch. But, this flip-flop affects the outputs only when positive transition of the clock signal is applied instead of active enable.The following table shows the state table of D flip-flop.

![image](https://user-images.githubusercontent.com/36288975/167908342-e03f0cbb-5958-43bb-b74a-5e3ec2341675.png)

![image](https://user-images.githubusercontent.com/36288975/167910325-aeef0739-0a54-40e2-bebd-6f5fa0cad10e.png)

Therefore, D flip-flop always Hold the information, which is available on data input, D of earlier positive transition of clock signal. From the above state table, we can directly write the next state equation as
Qt+1t+1 = D

![image](https://user-images.githubusercontent.com/36288975/167908850-d39d07ba-7f9d-490a-b9f2-274e189fd047.png)

Next state of D flip-flop is always equal to data input, D for every positive transition of the clock signal. Hence, D flip-flops can be used in registers, shift registers and some of the counters.


### JK Flip-Flop
JK flip-flop is the modified version of SR flip-flop. It operates with only positive clock transitions or negative clock transitions. The circuit diagram of JK flip-flop is shown in the following figure.

![image](https://user-images.githubusercontent.com/36288975/167910378-d2d984a7-2815-4d17-8c41-ee4bdf59ec24.png) 

This circuit has two inputs J & K and two outputs Qtt & Qtt’. The operation of JK flip-flop is similar to SR flip-flop. Here, we considered the inputs of SR flip-flop as S = J Qtt’ and R = KQtt in order to utilize the modified SR flip-flop for 4 combinations of inputs.The following table shows the state table of JK flip-flop.

![image](https://user-images.githubusercontent.com/36288975/167908575-59c35afb-50d3-46a2-888c-47478a3179d5.png)

Here, Qtt & Qt+1t+1 are present state & next state respectively. So, JK flip-flop can be used for one of these four functions such as Hold, Reset, Set & Complement of present state based on the input conditions, when positive transition of clock signal is applied. The following table shows the characteristic table of JK flip-flop.Present Inputs	Present State	Next State

![image](https://user-images.githubusercontent.com/36288975/167908664-c854ffe9-0bd3-44c2-bfa6-e53928181c69.png)

By using three variable K-Map, we can get the simplified expression for next state, Qt+1t+1. Three variable K-Map for next state, Qt+1t+1 is shown in the following figure.
 
 ![image](https://user-images.githubusercontent.com/36288975/167908688-fa93c3e9-8323-4864-947d-c11d163d5a90.png)

The maximum possible groupings of adjacent ones are already shown in the figure. Therefore, the simplified expression for next state Qt+1t+1 is
Q(t+1)=JQ(t)′+K′Q(t)Q(t+1)=JQ(t)′+K′Q(t)

### T Flip-Flop

T flip-flop is the simplified version of JK flip-flop. It is obtained by connecting the same input ‘T’ to both inputs of JK flip-flop. It operates with only positive clock transitions or negative clock transitions. The circuit diagram of T flip-flop is shown in the following figure.

![image](https://user-images.githubusercontent.com/36288975/167911534-5f3c445d-bc68-46e2-9a9c-7efce5febc60.png)

This circuit has single input T and two outputs Qtt & Qtt’. The operation of T flip-flop is same as that of JK flip-flop. Here, we considered the inputs of JK flip-flop as J = T and K = T in order to utilize the modified JK flip-flop for 2 combinations of inputs. So, we eliminated the other two combinations of J & K, for which those two values are complement to each other in T flip-flop.
The following table shows the state table of T flip-flop.

Here, Qtt & Qt+1t+1 are present state & next state respectively. So, T flip-flop can be used for one of these two functions such as Hold, & Complement of present state based on the input conditions, when positive transition of clock signal is applied. The following table shows the characteristic table of T flip-flop.
Inputs	Present State	Next State

![image](https://user-images.githubusercontent.com/36288975/167909015-53aa9450-3f28-4202-887a-79d88228f8a0.png)

From the above characteristic table, we can directly write the next state equation as
Q(t+1)=T′Q(t)+TQ(t)′
⇒Q(t+1)=T⊕Q(t)

### Procedure

The SR flip-flop is the simplest type of flip-flop. It has two inputs, S (Set) and R (Reset), and two
outputs, Q and Q' (not Q). The output of the SR flip-flop is set to 1 when the S input is high and the
R input is low. The output is reset to 0 when the R input is high and the S input is low. If both inputs
are high, the output is unpredictable.The JK flip-flop is more versatile than the SR flip-flop. It has
two inputs, J and K, and two outputs, Q and Q'. The output of the JK flip-flop toggles (changes from
0 to 1 or 1 to 0) when both inputs are high. When one input is high and the other is low, the output
remains unchanged. When both inputs are low, the output depends on the previous state of the
flip-flop. The D flip-flop is also known as a data flip-flop. It has one data input, D, and two outputs,
Q and Q'. The output of the D flip-flop follows the data input on the rising edge of the clock pulse.
The T flip-flop is also known as a toggle flip-flop. It has one input, T, and two outputs, Q and Q'.
The output of the T flip-flop toggles on the rising edge of the clock pulse.

### PROGRAM 

# SR FLIPFLOP

![WO5 SR P](https://github.com/vasanthkumarch/Experiment--05-Implementation-of-flipflops-using-verilog/assets/150005103/91f50cd4-55fd-4d27-8e34-ad21a40d4c39)


# D FLIPFLOP

![WO5 D P](https://github.com/vasanthkumarch/Experiment--05-Implementation-of-flipflops-using-verilog/assets/150005103/0e9626a0-118d-45ef-a18e-10249084c5ed)


# JK FLIPFLOP

![WO5 JK P](https://github.com/vasanthkumarch/Experiment--05-Implementation-of-flipflops-using-verilog/assets/150005103/2e71a7ab-2f47-48fa-9e61-f651fcbd46c2)


# T FLIPFLOP

![WO5 T P](https://github.com/vasanthkumarch/Experiment--05-Implementation-of-flipflops-using-verilog/assets/150005103/a45bf1bf-50c3-43ba-9040-67c18e223bb1)


### RTL REALIZATION

# SR FLIPFLOP

![WO5 LSR](https://github.com/vasanthkumarch/Experiment--05-Implementation-of-flipflops-using-verilog/assets/150005103/134d9046-2dec-4eb3-8797-378ee0413b79)


# D FLIPFLOP

![WO5 LD](https://github.com/vasanthkumarch/Experiment--05-Implementation-of-flipflops-using-verilog/assets/150005103/47fec311-874c-4747-b383-6d949647297d)


# JK FLIPFLOP

![WO5 LJK](https://github.com/vasanthkumarch/Experiment--05-Implementation-of-flipflops-using-verilog/assets/150005103/21424d59-2a5c-4ac1-bd20-775a542c20f2)

# T FLIPFLOP
![WO5 LT](https://github.com/vasanthkumarch/Experiment--05-Implementation-of-flipflops-using-verilog/assets/150005103/9c28d1e7-ba7a-44f0-bf7a-3dd3a5bc3d50)

# TRUTH TABLE 

# SR FLIPFLOP

![WO5 SR TT](https://github.com/vasanthkumarch/Experiment--05-Implementation-of-flipflops-using-verilog/assets/150005103/8cc97e4d-84e5-45ec-9cf6-94106071b103)


# D FLIPFLOP

![WO5 D TT](https://github.com/vasanthkumarch/Experiment--05-Implementation-of-flipflops-using-verilog/assets/150005103/f16c6a2f-989d-4dc1-90bf-5d5f401b35e8)


# JK FLIPDLOP

![WO5 JK TT](https://github.com/vasanthkumarch/Experiment--05-Implementation-of-flipflops-using-verilog/assets/150005103/922c0a51-5cb4-462d-b4b0-c7036653142b)


# T FLIPFLOP

![WO5 T TT](https://github.com/vasanthkumarch/Experiment--05-Implementation-of-flipflops-using-verilog/assets/150005103/b31ad322-8226-4078-8b78-148ce6d70160)


### TIMING DIGRAM 

# SR FLIPFLOP

![WO5 SR TD](https://github.com/vasanthkumarch/Experiment--05-Implementation-of-flipflops-using-verilog/assets/150005103/87ffb8d5-67be-43b7-8bc6-a14aa47ec833)


# D FLIPFLOP

![WO5 D TD](https://github.com/vasanthkumarch/Experiment--05-Implementation-of-flipflops-using-verilog/assets/150005103/b608fa9e-41f1-453e-9741-e6585e7a51a7)


# JK FLIPFLOP

![WO5 JK TD](https://github.com/vasanthkumarch/Experiment--05-Implementation-of-flipflops-using-verilog/assets/150005103/8f242f0e-45a8-4587-88bb-536106ca3a48)


# T FLIPFLOP

![WO5 T-TD](https://github.com/vasanthkumarch/Experiment--05-Implementation-of-flipflops-using-verilog/assets/150005103/e18aae77-3321-4042-8fb9-cf4c5cc27ac4)


### RESULTS 

Thus, the implementation of SR,JK,D and T flipflops using nand gates are done sucessfully
