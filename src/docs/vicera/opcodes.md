still todo
# VICERA Documentation

## Opcode reference

This page lists the usage of opcodes from the VIC-8P CPU.

### HALT

Stops everything and closes the VICERA.

### NOP

Does nothing.

### PUSH / PUSHA

Sets the high byte of the source to the memory address SP - 1, and the low byte of the source to the memory address SP. Then, SP gets decremented by 2.

```
mov sp, 0x9004
mov hl, 0xBEEF
push hl

;                    vv SP
; 0x9000 00 00 00 be ef 00 00 00 00 00 00 00 00 00 00 00
;                 ^H ^L
```

PUSHA pushes HL, BC, DE in one instruction. It is the equivalent of:

```
push hl
push bc
push de
```

### POP / POPA

todo (including the rest of instructions)

### Full Reference

| Instruction | Opcode | Length | Description | Notes |
|----|----|----|----|----|
| HALT | 0x00 | 1 | Halt | |
| NOP | 0x01 | 1 | No Operation | |
| PUSH HL | 0x02 | 1 | Push | (sp) = source; sp -= 2|
| PUSH BC | 0x03 | 1 | | |
| PUSH DE | 0x04 | 1 | | |
| PUSHA | 0x05 | 1 | Push All | push hl, bc, de |
| POP HL | 0x06 | 1 | Pop | sp += 2; destination = (sp) |
| POP BC | 0x07 | 1 | | |
| POP DE | 0x08 | 1 | | |
| POPA | 0x09 | 1 | Pop All | pop de, bc, hl |
| MOV A, A | 0x0A | 1 | Move | destination = source |
| MOV A, B | 0x0B | 1 | | |
| MOV A, C | 0x0C | 1 | | |
| MOV A, D | 0x0D | 1 | | |
| MOV A, E | 0x0E | 1 | | |
| MOV A, H | 0x0F | 1 | | |
| MOV A, L | 0x10 | 1 | | |
| MOV B, A | 0x11 | 1 | | |
| MOV B, B | 0x12 | 1 | | |
| MOV B, C | 0x13 | 1 | | |
| MOV B, D | 0x14 | 1 | | |
| MOV B, E | 0x15 | 1 | | |
| MOV B, H | 0x16 | 1 | | |
| MOV B, L | 0x17 | 1 | | |
| MOV C, A | 0x18 | 1 | | |
| MOV C, B | 0x19 | 1 | | |
| MOV C, C | 0x1A | 1 | | |
| MOV C, D | 0x1B | 1 | | |
| MOV C, E | 0x1C | 1 | | |
| MOV C, H | 0x1D | 1 | | |
| MOV C, L | 0x1E | 1 | | |
| MOV D, A | 0x1F | 1 | | |
| MOV D, B | 0x20 | 1 | | |
| MOV D, C | 0x21 | 1 | | |
| MOV D, D | 0x22 | 1 | | |
| MOV D, E | 0x23 | 1 | | |
| MOV D, H | 0x24 | 1 | | |
| MOV D, L | 0x25 | 1 | | |
| MOV E, A | 0x26 | 1 | | |
| MOV E, B | 0x27 | 1 | | |
| MOV E, C | 0x28 | 1 | | |
| MOV E, D | 0x29 | 1 | | |
| MOV E, E | 0x2A | 1 | | |
| MOV E, H | 0x2B | 1 | | |
| MOV E, L | 0x2C | 1 | | |
| MOV H, A | 0x2D | 1 | | |
| MOV H, B | 0x2E | 1 | | |
| MOV H, C | 0x2F | 1 | | |
| MOV H, D | 0x30 | 1 | | |
| MOV H, E | 0x31 | 1 | | |
| MOV H, H | 0x32 | 1 | | |
| MOV H, L | 0x33 | 1 | | |
| MOV L, A | 0x34 | 1 | | |
| MOV L, B | 0x35 | 1 | | |
| MOV L, C | 0x36 | 1 | | |
| MOV L, D | 0x37 | 1 | | |
| MOV L, E | 0x38 | 1 | | |
| MOV L, H | 0x39 | 1 | | |
| MOV L, L | 0x3A | 1 | | |
| MOV (HL), A | 0x3B | 1 | | |
| MOV (HL), B | 0x3C | 1 | | |
| MOV (HL), C | 0x3D | 1 | | |
| MOV (HL), D | 0x3E | 1 | | |
| MOV (HL), E | 0x3F | 1 | | |
| MOV (HL), H | 0x40 | 1 | | |
| MOV (HL), L | 0x41 | 1 | | |
| MOV A, NN | 0x42 0xNN | 2 | | |
| MOV B, NN | 0x43 0xNN | 2 | | |
| MOV C, NN | 0x44 0xNN | 2 | | |
| MOV D, NN | 0x45 0xNN | 2 | | |
| MOV E, NN | 0x46 0xNN | 2 | | |
| MOV H, NN | 0x47 0xNN | 2 | | |
| MOV L, NN | 0x48 0xNN | 2 | | |
| MOV (HL), NN | 0x49 0xNN | 2 | | |
| MOV A, (HL) | 0x4A | 1 | | |
| MOV B, (HL) | 0x4B | 1 | | |
| MOV C, (HL) | 0x4C | 1 | | |
| MOV D, (HL) | 0x4D | 1 | | |
| MOV E, (HL) | 0x4E | 1 | | |
| MOV H, (HL) | 0x4F | 1 | | |
| MOV L, (HL) | 0x50 | 1 | | |
| MOV SP, NNNN | 0x51 0xNN 0xNN | 3 | | |
| MOV SP, HL | 0x52 | 1 | | |
| MOV HL, SP | 0x53 | 1 | | |
| MOV A, (BC) | 0x54 | 1 | | |
| MOV A, (DE) | 0x55 | 1 | | |
| MOV A, (NNNN) | 0x56 0xNN 0xNN | 3 | | |
| MOV (BC), A | 0x57 | 1 | | |
| MOV (DE), A | 0x58 | 1 | | |
| MOV (NNNN), A | 0x59 0xNN 0xNN | 3 | | |
| MOV HL, NNNN | 0x5A 0xNN 0xNN | 3 | | |
| MOV BC, NNNN | 0x5B 0xNN 0xNN | 3 | | |
| MOV DE, NNNN | 0x5C 0xNN 0xNN | 3 | | |
| ADD A, A | 0x5D | 1 | Add | destination += source; if result == 0 then zero; if overflow then carry |
| ADD A, B | 0x5E | 1 | | |
| ADD A, C | 0x5F | 1 | | |
| ADD A, D | 0x60 | 1 | | |
| ADD A, E | 0x61 | 1 | | |
| ADD A, H | 0x62 | 1 | | |
| ADD A, L | 0x63 | 1 | | |
| ADD A, NN | 0x64 0xNN | 2 | | |
| ADD A, (HL) | 0x65 | 1 | | |
| ADD HL, HL | 0x66 | 1 | | |
| ADD HL, BC | 0x67 | 1 | | |
| ADD HL, DE | 0x68 | 1 | | |
| ADD HL, NNNN | 0x69 0xNN 0xNN | 3 | | |
| SUB A, A | 0x6A | 1 | Subtract | destination -= source; if result == 0 then zero; if overflow then carry |
| SUB A, B | 0x6B | 1 | | |
| SUB A, C | 0x6C | 1 | | |
| SUB A, D | 0x6D | 1 | | |
| SUB A, E | 0x6E | 1 | | |
| SUB A, H | 0x6F | 1 | | |
| SUB A, L | 0x70 | 1 | | |
| SUB A, NN | 0x71 0xNN | 2 | | |
| SUB A, (HL) | 0x72 | 1 | | |
| SUB HL, HL | 0x73 | 1 | | |
| SUB HL, BC | 0x74 | 1 | | |
| SUB HL, DE | 0x75 | 1 | | |
| SUB HL, NNNN | 0x76 0xNN 0xNN | 3 | | |
| AND A, A | 0x77 | 1 | Bitwise And | destination &= source |
| AND A, B | 0x78 | 1 | | |
| AND A, C | 0x79 | 1 | | |
| AND A, D | 0x7A | 1 | | |
| AND A, E | 0x7B | 1 | | |
| AND A, H | 0x7C | 1 | | |
| AND A, L | 0x7D | 1 | | |
| AND A, NN | 0x7E 0xNN | 2 | | |
| AND A, (HL) | 0x7F | 1 | | |
| OR A, A | 0x80 | 1 | Bitwise Or | destination \|= source |
| OR A, B | 0x81 | 1 | | |
| OR A, C | 0x82 | 1 | | |
| OR A, D | 0x83 | 1 | | |
| OR A, E | 0x84 | 1 | | |
| OR A, H | 0x85 | 1 | | |
| OR A, L | 0x86 | 1 | | |
| OR A, NN | 0x87 0xNN | 2 | | |
| OR A, (HL) | 0x88 | 1 | | |
| XOR A, A | 0x89 | 1 | Bitwise Exclusive Or | destination ^= source |
| XOR A, B | 0x8A | 1 | | |
| XOR A, C | 0x8B | 1 | | |
| XOR A, D | 0x8C | 1 | | |
| XOR A, E | 0x8D | 1 | | |
| XOR A, H | 0x8E | 1 | | |
| XOR A, L | 0x8F | 1 | | |
| XOR A, NN | 0x90 0xNN | 2 | | |
| XOR A, (HL) | 0x91 | 1 | | |
| INC A | 0x92 | 1 | Increment | destination++ |
| INC B | 0x93 | 1 | | |
| INC C | 0x94 | 1 | | |
| INC D | 0x95 | 1 | | |
| INC E | 0x96 | 1 | | |
| INC H | 0x97 | 1 | | |
| INC L | 0x98 | 1 | | |
| INC HL | 0x99 | 1 | | |
| INC BC | 0x9A | 1 | | |
| INC DE | 0x9B | 1 | | |
| DEC A | 0x9C | 1 | Decrement | destination-- |
| DEC B | 0x9D | 1 | | |
| DEC C | 0x9E | 1 | | |
| DEC D | 0x9F | 1 | | |
| DEC E | 0xA0 | 1 | | |
| DEC H | 0xA1 | 1 | | |
| DEC L | 0xA2 | 1 | | |
| DEC HL | 0xA3 | 1 | | |
| DEC BC | 0xA4 | 1 | | |
| DEC DE | 0xA5 | 1 | | |
| SL A | 0xA6 | 1 | Bitwise Shift Left | destination <<= 1 |
| SL B | 0xA7 | 1 | | |
| SL C | 0xA8 | 1 | | |
| SL D | 0xA9 | 1 | | |
| SL E | 0xAA | 1 | | |
| SL H | 0xAB | 1 | | |
| SL L | 0xAC | 1 | | |
| SR A | 0xAD | 1 | Bitwise Shift Right | destination >>= 1 |
| SR B | 0xAE | 1 | | |
| SR C | 0xAF | 1 | | |
| SR D | 0xB0 | 1 | | |
| SR E | 0xB1 | 1 | | |
| SR H | 0xB2 | 1 | | |
| SR L | 0xB3 | 1 | | |
| CP A | 0xB4 | 1 | Compare | if a == source then zero; if a < source then carry |
| CP B | 0xB5 | 1 | | |
| CP C | 0xB6 | 1 | | |
| CP D | 0xB7 | 1 | | |
| CP E | 0xB8 | 1 | | |
| CP H | 0xB9 | 1 | | |
| CP L | 0xBA | 1 | | |
| CP NN | 0xBB 0xNN | 2 | | |
| CP (HL) | 0xBC | 1 | | |
| JP NNNN | 0xBD 0xNN 0xNN | 3 | Jump | pc = source |
| JP HL | 0xBE | 1 | | |
| JC NNNN | 0xBF 0xNN 0xNN | 3 | Jump if Carry | if carry then pc = source |
| JC HL | 0xC0 | 1 | | |
| JZ NNNN | 0xC1 0xNN 0xNN | 3 | Jump if Zero | if zero then pc = source |
| JZ HL | 0xC2 | 1 | | |
| JN NNNN | 0xC3 0xNN 0xNN | 3 | Jump if Not Zero | if not zero then pc = source |
| JN HL | 0xC4 | 1 | | |
| CALL NNNN | 0xC5 0xNN 0xNN | 3 | Call | push pc; pc = source |
| CALL HL | 0xC6 | 1 | | |
| RET | 0xC7 | 1 | Return | pop pc |
| DUMPR | 0xC8 | 1 | Dump Registers | |
| DUMPM NNNN | 0xC9 0xNN 0xNN | 3 | Dump Memory | |
| SLP | 0xCA | 1 | Sleep | |
| SWAP A | 0xCB | 1 | Swap | A = destination; destination = A |
| SWAP B | 0xCC | 1 | | |
| SWAP C | 0xCD | 1 | | |
| SWAP D | 0xCE | 1 | | |
| SWAP E | 0xCF | 1 | | |
| SWAP H | 0xD0 | 1 | | |
| SWAP L | 0xD1 | 1 | | |
| SWAP (HL) | 0xD2 | 1 | | |
| SWAP HL | 0xD3 | 1 | Swap (16-bit) | HL = destination; destination = HL |
| SWAP BC | 0xD4 | 1 | | |
| SWAP DE | 0xD5 | 1 | | |
| DBG | 0xD6 | 1 | Debug | |
