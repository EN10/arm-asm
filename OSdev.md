#ARM Assembly#

Install (Only Once):    
-
Open Terminal:  
Click "+" -> New Teminal OR Alt + T     

    sudo apt install binutils-arm-none-eabi 
    sudo apt install qemu-system-arm    

Assemble:    
-
    arm-none-eabi-as add.s

Run:    
-
    qemu-system-arm -M sx1 -kernel a.out -nographic -monitor stdio  
    info registers

For detailed debugging see GDB:     
https://github.com/EN10/arm-as/blob/master/GDB.md   

Notes on Source
-
@ is an arm as single line comment like ' in VB.NET     
/*  */ is used for multiline comments like in C

Source must end with newline otherwise:  
Assembler end of file Warning  

Infinite loop needed at the end otherwise:  
qemu: fatal: Trying to execute code outside RAM

-o flag can be used to specify output name  

    arm-none-eabi-as -o add.o add.s

**AQA ARM:**     
http://filestore.aqa.org.uk/resources/computing/AQA-75162-75172-ALI.PDF 

Instructions Examples:  
*   ADD 
*   SUB
*   AND 
*   LSL
*   CMP