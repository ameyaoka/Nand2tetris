# nand2tetris
Building a modern computer from first principles

## table of content 


1.  Boolean logic 
2.  Boolean arithmetic
3.  Sequential logic
4.  Machine Language 
5.  Computer Architecture  
6.  Assembler 
7.  Virtual Machine 1 Stack Arithmetic 
8.  Virtual Machine 2 Program control 
9.  High-Level language 
10. Compiler 1 Syntax Analysis 
11. Code generation 
12. Operating System 
13. Postscript More Fun To Go 
 

## logic gates 
- Gate is a physical device that implements boolean function .

-

-Primitive and composite gates:

-All logic gates have same I/O semantics (0 and 1), they can be chained together.

-Ex Xor gate , output of Xor is 1 when a=0.b=1 or a=1,b=0.
Xor(a,b)=Or(And(a,Not(b))).There may be multiple ways to implement a particular gate .From Efficiency standpoint the general rule is to do more with less,that is , use few gates as possible.

-** Hardware description language (HDL)**
- DHL is used to plan and optimize the chip on computer using formalism like hardware description language .


-** Nand gate**
-**chip name:** Nand 
-**Inputs:** a,b
-**output** out
-**function** if a=b=1 then out=o else out=1

-**Basic logic gates**

-**chip name:** not (also known as converter)
-**Inputs:** in
-**output** out
-**function** if in=0 then out =1 else out=0

--**chip name:** and 
-**Inputs:** a,b
-**output** out
-**function** if a=b=1 then out =1 else out=0

**chip name:** or
-**Inputs:** a,b
-**output** out
-**function** if a=b=0 then out=0 else out=1

**chip name:** xor
-**Inputs:** a,b
-**output** out
-**function** if a/=b then out=1 else out=0

**chip name:** Mux  	(Multiplexor)
-**Inputs:** a,b,sel
-**output** out
-**function** if sel=0 then out=a else out=b


**chip name:** DMux  	(Demultiplexor)
-**Inputs:** in,sel
-**output** a,b 
-**function** if sel=0 then (a=in) else (b=in) 


### Multu-bit version of basic gates

