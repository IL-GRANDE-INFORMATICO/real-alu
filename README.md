# RealALU
**Input**
inA (7:0)
inB (7:0)
aluOp (3:0)

**Output**
aluOut (0:7)
V _overflow, 1 se C != aluOut[7]_
C _carry, = aluOut[8]_
Z _zero, 1 se out == 00000000_

**Comandi**
```
0 | 0000 | inA and inB | Logica
1 | 0001 | inA or inB  | Logica
2 | 0010 | NOT inB     | Logica
3 | 0011 | LSL inB (0) | Logica
4 | 0100 | LSR inB (0) | Logica
5 | 0101 | inA add inB | Aritmetica
6 | 0110 | inA sub inB | Aritmetica
7 | 0111 | inc inB     | Aritmetica
8 | 1000 | dec inB     | Aritmetica
9 | 1001 | inA         | Aritmetica
```