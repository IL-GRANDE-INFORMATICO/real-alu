# RealALU
### Input

- **inA** (7:0) _primo operando_
- **inB** (7:0) _secondo operando_
- **aluOp** (3:0) _selettore dell'operazione da eseguire_

### Output

- **aluOut** (0:7) _risultato dell'operazione_
- **V** _overflow, 1 se C != aluOut[7]_
- **C** _carry, = aluOut[8]_
- **Z** _zero, 1 se out == 00000000_
- **N** _segno, = aluOut[7]_

### Comandi

```
N | BIN  | ISTRUZIONE  | TIPOOPERAZ | FLAG
0 | 0000 | inA and inB | Logica     | ---Z
1 | 0001 | inA or inB  | Logica     | ---Z
2 | 0010 | NOT inB     | Logica     | ---Z
3 | 0011 | LSL inB (0) | Logica     | -NCZ
4 | 0100 | LSR inB (0) | Logica     | -NCZ
5 | 0101 | inA add inB | Aritmetica | VNCZ
6 | 0110 | inA sub inB | Aritmetica | VNCZ
7 | 0111 | inc inB     | Aritmetica | VNCZ
8 | 1000 | dec inB     | Aritmetica | VNCZ
9 | 1001 | inA         | Aritmetica | -N-Z
```

## Da fare
- [x] inA AND inB
- [x] inA OR inB
- [x] NOT inB
- [x] LSL (0) _shift a sinistra_
- [x] LSR inB (0) _shift a destra_
- [ ] inA ADD inB _somma tra byte_
- [ ] inA SUB inB _sottrazione tra byte_
- [ ] inc inB _aumenta di 1 l'ingresso B_
- [ ] dec inB _decrementa di 1 l'ingresso B_
- [ ] inA
