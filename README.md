** Note: this a very early development draft and is therefore unstable **

# Registers
R0..R31 general purpose registers
COND register
RIP register
RSP register
RBP register

Bit fields
[0..31] IMM
[32..36] RS2
[37..41] RS1
[42..46] RD
[47..56] OPCODE
[57..60] OPCODE_GROUP
[61..63] FIELD

# Set memory
SET RD IMM ; Set lower bit, erases higher bit
SETH RD IMM ; Set higher bit

# Memory Accesses
LDx RD RS
SRx RD RS
LDx RD IMM
SRx RD IMM
where x is 1,2,4,8

# Arithmetic
ADD RD RS1 RS2
SUB RD RS1 RS2
MUL RD RS1 RS2
DIV RD RS1 RS2

ADD RD RS1 IMM
SUB RD RS1 IMM
MUL RD RS1 IMM
DIV RD RS1 IMM

# Conditionals set the COND register
GEQ RS1 RS2
GRE RS1 RS2
EQU RS1 RS2
LEQ RS1 RS2
LES RS1 RS2

# Branching
J IMM
J RS1

## Function calls
CALL
RET

# ABI
R0 the return value
R1..R32 for arguments

# Addressing modes
Only absolute and indirect addressin is used
