# Arithmetic-operation-using-8086
# 8086 Assembly Language Programs for Arithmetic Operations

## AIM

To write and execute Assembly Language Programs to perform arithmetic operations for the 8086 microprocessor.

---

## APPARATUS REQUIRED

* Personal Computer with MASM Software

---

## 1. ADDITION

#### Algorithm

1. Initialize memory location in HL register.
2. Store 1st data.
3. Increment HL to enter 2nd data.
4. Move 2nd number to accumulator.
5. Decrement HL.
6. Add value in memory with accumulator.
7. Store result.
8. Stop.


## FLOW CHART
<img width="707" height="1024" alt="image" src="https://github.com/user-attachments/assets/b5a7062d-e294-47cd-9683-a40de25e82de" />


#### Program

```asm
CODE SEGMENT
ASSUME CS: CODE, DS: CODE
ORG 1000H
MOV CL,00H
MOV AX,1234H
MOV BX,124H
ADD AX,BX
JNC L1
INC CL
L1:MOV SI,1200H
MOV [SI], AX
MOV [SI+2], CL
MOV AH,4CH
INT 21H
CODE ENDS
END
```

#### Output Table

| MEMORY LOCATION (OUTPUT) |
| 1200      01|
| 58        13|



#### Manual Calculations

AX  1234H
BX  0124H
-------------
   5813
## OUTPUT IMAGE FROM MASM SOFTWARE
<img width="1128" height="752" alt="image" src="https://github.com/user-attachments/assets/d76f1387-2da4-4d83-a1e6-b01b056ce62c" />


## 2. SUBTRACTION

#### Algorithm

1. Initialize memory and store 1st data.
2. Increment to get 2nd data.
3. Move 2nd data to accumulator.
4. Subtract memory content.
5. Store result.

## FLOWCHART

<img width="578" height="797" alt="image" src="https://github.com/user-attachments/assets/564c3c7a-33ce-4a1c-8920-beb5c24b9b47" />


#### Program
```asm
CODE SEGMENT
ASSUME CS: CODE, DS: CODE
ORG 1000H
MOV CL,00H
MOV AX,1234H
MOV BX,124H
SUB AX,BX
JNC L1
INC CL
L1:MOV SI,1200H
MOV [SI], AX
MOV [SI+2], CL
MOV AH,4CH
INT 21H
CODE ENDS
END
```


#### Output Table

| MEMORY LOCATION (OUTPUT) |
| 1200    01 |
|  10     11 |                          

#### Manual Calculations

AX   1234H
BX   0124H
--------------
     1011


## OUTPUT SCREEN FROM MASM SOFTWARE
<img width="1121" height="751" alt="image" src="https://github.com/user-attachments/assets/1b5dc01b-e7df-4f99-a94f-69c4b5f49ad3" />



## 3. MULTIPLICATION

#### Algorithm

1. Initialize memory and store operands.
2. Move operands to registers.
3. Multiply.
4. Store result.

##FLOWCHART

<img width="569" height="906" alt="image" src="https://github.com/user-attachments/assets/88be88ff-2896-4a88-b73d-84ccffd2fcf9" />



#### Program

```asm
CODE SEGMENT
ASSUME CS: CODE, DS: CODE
ORG 1000H
MOV DX,0000H
MOV AX,1234H
MOV BX,124H
MUL BX
MOV SI,1200H
MOV [SI],AX
MOV [SI+02H],DX
MOV AH,4CH
INT 21H
CODE ENDS
END
```

#### Output Table

| MEMORY LOCATION (OUTPUT) |
| 1200   01   02   03 |
| 58     13   00   EB |                          

#### Manual Calculations

AX   1234H
BX   124H
----------------
    581300EB

## OUTPUT SCREEN FROM MASM SOFTWARE
<img width="1148" height="751" alt="image" src="https://github.com/user-attachments/assets/3047d813-0649-40ba-8cf1-6f8037f8becc" />


## 4. DIVISION

#### Algorithm

1. Load memory location of operands.
2. Perform division.
3. Store result.

   ## FLOWCHART
<img width="1065" height="802" alt="image" src="https://github.com/user-attachments/assets/25b4a483-0d42-494b-8639-1af3ea17191b" />


#### Program

```asm
CODE SEGMENT 
ASSUME CS:CODE,DS:CODE
ORG 1000H
MOV DX,0000H
MOV AX,1234H
MOV BX,124H
DIV BX
MOV SI,1200H
MOV[SI],AX
MOV[SI+02H],DX
MOV AH,4CH
INT 21H
CODE ENDS
END
```

#### Output Table

| MEMORY LOCATION (OUTPUT) |
|1200   01   02   03 |
|01     00   00   E8 |                          

#### Manual Calculations

AX   1234H
BX   124H
--------------
   010000E8

## OUTPUT FROM MASM SOFTWARE
<img width="1132" height="751" alt="image" src="https://github.com/user-attachments/assets/e9bed875-ff94-4fdf-bd08-9e637f3fbb86" />




## RESULT

Thus, the Assembly Language Programs for 8086 to perform arithmetic operations (Addition, Subtraction, Multiplication, and Division) using both direct and indirect methods were successfully written and executed using MASM.

