# Lesson 2: Sequential Logic & The D-Flip Flop 🔄

In Lesson 1, we learned about **Combinational Logic** (logic that changes instantly). Now, we enter the world of **Sequential Logic**, where things happen only when a "Clock" signal tells them to.

### What is a Clock?
A clock is a signal that oscillates between `0` and `1` at a regular interval. In Verilog, we usually look for the **Positive Edge** (the exact moment the signal jumps from 0 to 1).

### The D-Flip Flop (DFF)
The DFF is the most basic memory element. It "captures" the value of the input **D** and moves it to the output **Q** only when the clock ticks.



### The Code:
```verilog
module d_flip_flop (
    input wire clk, // Clock signal
    input wire d,   // Data input
    output reg q    // Data output (reg is used for sequential logic)
);

    // This block triggers ONLY at the positive edge of the clock
    always @(posedge clk) begin
        q <= d; // We use <= (non-blocking) for sequential logic
    end

endmodule
