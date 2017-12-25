This file contains materials for one instance of the attacklab.

Files:

    ctarget

Linux binary with code-injection vulnerability.  To be used for phases
1-3 of the assignment.

    rtarget

Linux binary with return-oriented programming vulnerability.  To be
used for phases 4-5 of the assignment.

     cookie.txt

Text file containing 4-byte signature required for this lab instance.

     farm.c

Source code for gadget farm present in this instance of rtarget.  You
can compile (use flag -Og) and disassemble it to look for gadgets.

     hex2raw

Utility program to generate byte sequences.  See documentation in lab
handout.

#### Solution
exploit.txt
exploit2.txt
exploit3.txt
exploit2r.txt

run ./ctarget -i exploit-raw.txt -q 

1. get exploit.txt using
  ./hex2raw < exploit.txt > exploit-raw.txt 
2. get touch.o using
  gcc -c touch.s
3. get touch.d using (disassemble)
  objdump -d touch.o > touch.s