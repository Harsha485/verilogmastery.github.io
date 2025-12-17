# Lesson 2: Combinational vs. Sequential Logic

In Verilog, there are two ways to describe how hardware behaves.

### 1. Combinational Logic
Think of this like a simple light switch. When you flip the switch, the light turns on immediately. 
* **Verilog Keyword:** `assign`
* **Example:** The AND gate from Lesson 1.

### 2. Sequential Logic
This is logic that "remembers" things. It only changes when a **Clock (CLK)** signal tells it to.
* **Verilog Keyword:** `always @(posedge clk)`
* **Example:** A D-Flip Flop (the basic unit of memory).



### The Code: D-Flip Flop
```verilog
module d_flip_flop (
    input wire clk,
    input wire d,
    output reg q
);

    // This block triggers every time the clock goes from 0 to 1
    always @(posedge clk) begin
        q <= d; // Non-blocking assignment
    end

endmodule
