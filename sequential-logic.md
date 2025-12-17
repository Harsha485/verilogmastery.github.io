# Lesson 2: Sequential Logic & The D-Flip Flop 🔄

In Lesson 1, we learned about **Combinational Logic**. Now, we enter the world of **Sequential Logic**, where things happen based on a "Clock" signal.

### What is a Clock?
A clock is the "heartbeat" of digital systems. It tells the hardware exactly when to update its values.

### The D-Flip Flop (DFF)
A DFF captures the value of input **D** only when the clock rises (Positive Edge).



### The Verilog Code:
```verilog
module d_flip_flop (
    input wire clk, 
    input wire d,   
    output reg q    
);

    // This triggers ONLY at the positive edge of the clock
    always @(posedge clk) begin
        q <= d; // Use non-blocking (<=) for sequential logic
    end

endmodule
