# D_FLIP_FLOP

AIM:

To implement D flipflop using verilog and validating their functionality using their functional tables

SOFTWARE REQUIRED:
         Quartus prime

THEORY

D Flip-Flop

D flip-flop operates with only positive clock transitions or negative clock transitions. Whereas, D latch operates with enable signal. That means, the output of D flip-flop is insensitive to the changes in the input, D except for active transition of the clock signal. The circuit diagram of D flip-flop is shown in the following figure.

<img width="805" height="410" alt="1" src="https://github.com/user-attachments/assets/99a4ece2-3835-4d2a-9803-edf20a8b1ee4" />

This circuit has single input D and two outputs Qtt & Qtt’. The operation of D flip-flop is similar to D Latch. But, this flip-flop affects the outputs only when positive transition of the clock signal is applied instead of active enable. The following table shows the state table of D flip-flop.

<img width="464" height="170" alt="2" src="https://github.com/user-attachments/assets/1b58afce-075a-4e23-976e-9cc669669d8c" />

Therefore, D flip-flop always Hold the information, which is available on data input, D of earlier positive transition of clock signal. From the above state table, we can directly write the next state equation as Qt+1t+1 = D

<img width="463" height="260" alt="3" src="https://github.com/user-attachments/assets/087cf1d4-9bd8-4035-915f-21bf4c9004fb" />

Next state of D flip-flop is always equal to data input, D for every positive transition of the clock signal. Hence, D flip-flops can be used in registers, shift registers and some of the counters.

PROGRAM:

```
module data_flip_flop (
    input  wire clk, rst, D,
    output reg  Q
);
    always @(posedge clk or posedge rst) begin
        if (rst)
            Q <= 1'b0;   // Reset
        else
            Q <= D;      // Capture D at clock edge
    end
endmodule

```

IMAGE: 
[EX 08 Dia.pdf](https://github.com/user-attachments/files/24149304/EX.08.Dia.pdf)

WAVEFORM: 
[unknown.bmp](https://github.com/user-attachments/files/24149317/unknown.bmp)

NAME: HEMA PRIYA

REF NO : 25017270

RESULT: Thus the D flipflop using verilog and validating their functionality using their functional tables is verified
