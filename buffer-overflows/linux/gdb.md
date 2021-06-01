# GDB

## Getting started 

### disas \[function name\]

Shows a disassembly of a function.

### break \[function\] or break 0xaddress

Puts a breakpoint at the entry of a function or at a certain address. 

### print \[name\]

Displays content of an object. 

### info \[name\]

Displays information. for example info registers prints the certents of all registers 

### step 

Step in teh program untill it reaches the next source line \(Step Over\) 

### stepi

Step into exactly one instruction 

### x 

Displays various memory locations in various formats. 

The syntax is: x/\[number of units\]\[data type\]\[location name\]

#### Example:

Displays 20 words starting from where esi points to

```text
x/20w $esi
```

