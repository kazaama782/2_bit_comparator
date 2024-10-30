# 2_bit_comparator

`timescale 1ns / 1ps


module two_bit_comparator(gt,lt,eq,a1,a0,b1,b0);
input a1,a0,b1,b0;
output reg gt,lt,eq;
always @(*)
begin
gt=({a1,a0}>{b1,b0});
lt=({a1,a0}<{b1,b0});
eq=({a1,a0}=={b1,b0});
end
endmodule
