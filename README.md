Design code:

// Gate level modelling

module logicgates(a,b,y);
input a,b;
output y;
buf(y,a);
not(y,a);
and(y,a,b);
or(y,a,b);
nand(y,a,b);
or(y,a,b);
xor(y,a,b);
xnor(y,a,b);
endmodule

//Data flow modelling

module logicgates(a,b,y);
input a,b;
output y;
assign y=a;
assign y=~a;
assign y= a&b;
assign y=a|b;
assign y=~(a&b);
assign y=~(a|b);
assign y=a^b;
assign y=~(a^b);
endmodule

Test bench :

// Gate level modelling

module logicgates_tb(a,b,y);
reg a,b;
wire y;
logicgates uut(a,b,y);
initial begin
a=0;
b=0;
#10;
a=1;
b=0;
#10
a=0;
b=1;
#10
a=1;
b=1;
#10
end
$finish();
endmodule












