SIMULATION AND IMPLEMENTATION OF LOGIC GATES
module mux4_1(i, s, y);
    input [3:0] i;    // 4-bit input data
    input [1:0] s;    // 2-bit select signal
    output reg y;     // Single-bit output

    // Always block to implement the multiplexer logic
    always @(i, s) begin
        case(s)
            2'b00: y = i[0];  // If select signal is 00, assign y to i[0]
            2'b01: y = i[1];  // If select signal is 01, assign y to i[1]
            2'b10: y = i[2];  // If select signal is 10, assign y to i[2]
            2'b11: y = i[3];  // If select signal is 11, assign y to i[3]
            default: y = 1'b0; // Default case for invalid select signal
        endcase
    end

endmodule


Conclusion:

In this experiment, a 4:1 Multiplexer was successfully designed and simulated using Verilog HDL across four different modeling styles: Gate-Level, Data Flow, Behavioral, and Structural. The simulation results verified the correct functionality of the MUX, with all implementations producing identical outputs for the given input conditions.



  
