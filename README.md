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
 

### logic gates 
- Gate is a physical device that implements boolean function .

-

- Primitive and composite gates:

- All logic gates have same I/O semantics (0 and 1), they can be chained together.

- Ex Xor gate , output of Xor is 1 when a=0.b=1 or a=1,b=0.
Xor(a,b)=Or(And(a,Not(b))).There may be multiple ways to implement a particular gate .From Efficiency standpoint the general rule is to do more with less,that is , use few gates as possible.

- **Hardware description language (HDL)**
- DHL is used to plan and optimize the chip on computer using formalism like hardware description language .


- **Nand gate**
- **chip name:** Nand 
- **Inputs:** a,b
- **output** out
- **function** if a=b=1 then out=o else out=1

- **Basic logic gates**

- **chip name:** not (also known as converter)
- **Inputs:** in
- **output** out
- **function** if in=0 then out =1 else out=0
 
- **chip name:** and 
- **Inputs:** a,b
- **output** out
- **function** if a=b=1 then out =1 else out=0
 
**chip name:** or
- **Inputs:** a,b
- **output** out
- **function** if a=b=0 then out=0 else out=1
 
 **chip name:** xor
- **Inputs:** a,b
- **output** out
- **function** if a/=b then out=1 else out=0
 
 **chip name:** Mux  	(Multiplexor)
- **Inputs:** a,b,sel
- **output** out
- **function** if sel=0 then out=a else out=b
 
 
**chip name:** DMux  	(Demultiplexor)
- **Inputs:** in,sel
- **output** a,b 
- **function** if sel=0 then (a=in) else (b=in) 


### Multu-bit version of basic gates








### Sequential logic 

- Computer must not only compute values but also store them and recall them .
- Thus computers must be equipped with memory that can preserve data data over time .
- boolean and arithmetic chips compute function (ALU)but cannot maintain state.
- memory involves synchronization ,clocking and feedback loop.
- memory elements can be built with flip-flop.
- The act of remembering something is inherently time-dependant
- In order to build chips that remember information we must build some standard means of representing progress of time


**clock** 
- The passage of time is representated by master clock
- The oscillator alternates between two phases 0-1,low-high.
- Time between the two phases is called a  cycle .
- The signal is continuously Broadcast to every sequential chip.

**Flip-Flop** 
- DFF (data flipflop) consist of single bit data  input and single bit data output and a clock input .
- implements time-based behavior out(t)=in(t-1).
- DFF simply outputs input values from previous time unit.

**Registers**
- A register is a storage device that can store or remember a value [ out(t)=out(t-1).
- Implemented using multiplexor and DFF 
- Feeding back output of DFF back into its input.
- if you want to sore new values set mux sel=1 or else 0 .
- The design parameter for register is width-the number of its it can hold

**Memories**
- Memory can be built by  stacking together registers to form RAM (Random Access Memory).
- RAM can access any word in memory irrespective of its physical location-be accessed , in equal speed.

### Machine Language
- A machine language can be viewed as an agreed upon formalism, d>

### Memory
- The term memory loosely refers to collection of hardware device>

- From programmers point of view all memories have same structre >


### Processor
- Central processing unit
- Performs fixed set of operations
- arithmetic and logical operations, memory access operations and>

### Registers

- Memory access is slow operation .
- Most processors are equipped with registers capable of holding >
- These registers are located in immediate proximity ,Registers s>

**Memory access**

- Memory access commands are of two categories.
- arithmetic and logical commands are allowed to operate not only>

- explicit load and store commands ,designed to move data between>

- Three memory access modes which are always supported .
        1. **direct addressing :** express a specific address or >

        load R1,67 // R1<- memory[67]
        or
        LOAD R1,bar  // assume that bar refers to memory address >

        2. **immediate addressing :**
        - Used to load constants.
        - Loads value of field itself into the register.
        - eg: LOADI R1,67 //R1 <- 67

        3. **Indirect addressing :**
        - Instruction specify memory location that holds the requ>
**Flow of the control**
- Programs occasional branches to locations other than next comma>
- Branching is used for **repetition** or **conditional execution>





**Hack machine language specification**
- 16-bit machine
- CPU
- 2 memory modules (instruction memory ,data memory)
- 2 memory mapped I/O devices: screen and keyboard.

- **memory address spaces**
- 2 distinct address (instruction memory ,data memory)
- both 16 bit wide and 24 bit address space .
- CPU can run program that resides in instruction memory.
- instruction memory is read-only.


- **Registers**
- Two 16-bit registers called D & A.
- registers can be manipulated by arithmetic and logical instruct>
- D stores data values
- A doubles as both data register and an address register.



