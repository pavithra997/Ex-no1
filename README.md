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
ASSUME CS:CODE, DS:CODE
ORG 1000H
MOV CL,00H
MOV AX,1234H
MOV BX,1234H
ADD AX,BX
JNC L1
INC CL
L1:MOV SI,1200H
MOV [SI],AX
MOV [SI+2],CL
MOV AH,4CH
INT 21H
CODE ENDS
END
```

#### Output Table

| MEMORY LOCATION (OUTPUT) |
| 1200  01 |
| 58    13 |

#### Manual Calculations

AX  1234H
BX  124H
------------
    5813
    
## OUTPUT IMAGE FROM MASM SOFTWARE
<img width="1087" height="755" alt="image" src="https://github.com/user-attachments/assets/91c3c120-e1a8-4461-8ceb-1e5087120373" />


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
| 1200      01 |
|  10       11 |                          

#### Manual Calculations

AX 1234H
BX 124H
-------------
   1011

## OUTPUT SCREEN FROM MASM SOFTWARE
<img width="1125" height="747" alt="image" src="https://github.com/user-attachments/assets/b3c5c811-75d8-49fa-bf52-5bbe405f621a" />


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
| 1200  01  02  03 |
|  58   13  00  EB |                          

#### Manual Calculations

AX  1234H
BX  124H
--------------
   581300EB
   
## OUTPUT SCREEN FROM MASM SOFTWARE
<img width="1156" height="751" alt="image" src="https://github.com/user-attachments/assets/fc4c4bd4-f375-4e3f-8406-1392be9693d2" />


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
| 1200   01   02    03 |
|  01    00   00    E8 |                          

#### Manual Calculations

AX  1234H
BX  124H
---------------
    010000E8
    
## OUTPUT FROM MASM SOFTWARE
<img width="1132" height="750" alt="image" src="https://github.com/user-attachments/assets/f98b42a0-044b-4616-ac9a-3965f284d987" />




## RESULT

Thus, the Assembly Language Programs for 8086 to perform arithmetic operations (Addition, Subtraction, Multiplication, and Division) using both direct and indirect methods were successfully written and executed using MASM.

