still todo
# VICERA Documentation

## Opcode reference

description description description

### Table of Contents

 - table
 - of
 - contents

### Reference

| Instruction | Opcode | Length | Description | Notes |
|----|----|----|----|----|
| HALT | 0x00 | 1 | Halt | |
| NOP | 0x01 | 1 | No Operation | |
| PUSH HL | 0x02 | 1 | Push | |
| PUSH BC | 0x03 | 1 | | |
| PUSH DE | 0x04 | 1 | | |
| PUSHA | 0x05 | 1 | Push All | |
| POP HL | 0x06 | 1 | Pop
| POP BC | 0x07 | 1 | | |
| POP DE | 0x08 | 1 | | |
| POPA | 0x09 | 1 | Pop All | |
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
| ADD A, A | 0x5D | 1 | Add | destination += source |
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
