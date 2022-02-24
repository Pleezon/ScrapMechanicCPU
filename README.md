# ScrapMechanicCPU
ScrapMechanic 4hz 8bit programmable CPU made from over 6000 logic-gates.  
Comes with pre-programmed fibonacci and a 7-segment display hooked up to it.

## Usage
1. press the button closest to the display to reset the program counter.  
2. enable every switch, the last one being the closest to the display.  
3. watch it do it's thing until it overflows (it will keep on going, though)  

## Programming  
The program memory is the largest component. It has 256 12-Bit rows, colored yellow and green.    
Programming is done by changing logic-gates to NOR / OR, so that their default state (without inputs) changes.    
To start programming, disable the switch located on the front of the program memory to enter human-readable-mode.    

| Binary |	Opcode | Description |  
| ------ | ------- | ----------- |
| 00000000 | HLT	| Halt |  
| 00000001 	| LDA	| Load from instruction to A
| 00000010	| LDB	| Load from instruction to B
| 00000011	| STA	| Store from A to memory adress
| 00000100	| STB	| Store from B to memory adress
| 00000101	| STC	| Store from C to memory adress
| 00000110	| MEA	| Load from memory to A
| 00000111	| MEB	| Load from memory to B
| 00001000	| ADD	| A+B=C
| 00001001	| SUB	| A-B=C
| 00001010	| CMP	| Compare A and B into C, if true c=00000001 else c=00000000. Adress 01 for >, adress 00 for <, adress 10 for ==
| 00001011	| JMP	| Jumps to adress in program memory
| 00001100	| JIF	| Jumps to adress if C = 00000001
| 00001101	| OUT	| Outputs memory adress to screen
| 00001110		
| 00001111		

## Features  
#### 256Bit ROM for programming (4bit opcode, 8bit parameter)  
#### 16Bit adressable RAM  
#### 4hz (which is actually pretty fast for Scrap Mechanic)
#### ALU  
- CLR adder  
- comparisons  
- multiplication  
