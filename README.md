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
MOV SI,2000H
MOV CL,00H
MOV AX,[SI]
MOV BX,[SI+02H]
ADD AX,BX
JNC L1
INC CL
L1:
MOV [SI+04H],AX
MOV [SI+06H],CL
MOV AH,4CH
INT 21H
CODE ENDS
END
```

#### Output Table

| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| 1200:12----------------------- | 1200:24------------------------ |
|  1201:34                       | 1205:68 1202:12 1206:00 1203:34                        |

#### Manual Calculations

(Add your calculation here)
<img width="665" height="722" alt="image" src="https://github.com/user-attachments/assets/a5943379-5937-4f23-b111-9ef0205d619b" />

---

## OUTPUT IMAGE FROM MASM SOFTWARE
<img width="640" height="480" alt="Screenshot (3201)" src="https://github.com/user-attachments/assets/089c832e-da66-481a-8da7-4069c75e2b3a" />
<img width="640" height="480" alt="Screenshot (3203)" src="https://github.com/user-attachments/assets/216ba082-b5a1-4977-883a-9297a41c4dcb" />


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
MOV SI,2000H
MOV CL,00H
MOV AX,[SI]
MOV BX,[SI+02H]
SUB AX,BX
JNC L1
INC CL
L1:
MOV [SI+04H],AX
MOV [SI+06H],CL
MOV AH,4CH
INT 21H
CODE ENDS
END
```



#### Output Table

| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
|1200:12 ----------------------- | 1200:00------------------------ |
| 1201:34                         | 1205:00 1202:12 1206:00 1203:34                          |

#### Manual Calculations

(Add your calculation here)
<img width="613" height="557" alt="image" src="https://github.com/user-attachments/assets/5feeb081-0bad-41d0-800e-d956bfedd05f" />

---


## OUTPUT SCREEN FROM MASM SOFTWARE
<img width="640" height="480" alt="Screenshot (3189)" src="https://github.com/user-attachments/assets/8c6e7494-269b-404c-b695-3c73e9629614" />
<img width="640" height="480" alt="Screenshot (3190)" src="https://github.com/user-attachments/assets/6c111013-5b35-4ca2-b7ef-4bef98e669a5" />


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
MOV SI,2000H
MOV DX,0000H
MOV AX,[SI]
MOV BX,[SI+02H]
MUL BX
MOV [SI+04H],AX
MOV [SI+06H],DX
MOV AH,4CH
INT 21H
CODE ENDS
END
```

#### Output Table

| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| 1200:12----------------------- | 1200:44----------------------- |
| 1201:34                        | 1205:51 1202:12 1206:97 1203:34-------- 1207:0A-----------|-----------                         |

#### Manual Calculations

(Add your calculation here)
<img width="613" height="434" alt="image" src="https://github.com/user-attachments/assets/cbec3c0f-1d7a-4698-b8d1-240c058d45ff" />


---

## OUTPUT SCREEN FROM MASM SOFTWARE
<img width="640" height="480" alt="Screenshot (3195)" src="https://github.com/user-attachments/assets/902af171-565c-4e72-8198-10a73b409dc2" />
<img width="640" height="480" alt="Screenshot (3196)" src="https://github.com/user-attachments/assets/6c8bf4d6-f92e-46d1-a5da-01e65470e584" />


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
ASSUME CS: CODE, DS: CODE
ORG 1000H
MOV SI,2000H
MOV DX,0000H
MOV AX,[SI]
MOV BX,[SI+02H]
DIV BX
MOV [SI+04H],AX
MOV [SI+06H],DX
MOV AH,4CH
INT 21H
CODE ENDS
END
```

#### Output Table

| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| 1200:12----------------------- | 1200:01------------------------ |1201:34
| 1205:00 1202:12 1206:00 1203:34----------1207:00-------                         |   -------------                       |

#### Manual Calculations

(Add your calculation here)
<img width="1104" height="715" alt="image" src="https://github.com/user-attachments/assets/dd617aaa-7907-4845-9643-b8c5829f5b62" />

---
## OUTPUT FROM MASM SOFTWARE
<img width="640" height="480" alt="Screenshot (3198)" src="https://github.com/user-attachments/assets/f3c9a890-98e9-433d-8e8c-1db1712f2fcf" />
<img width="640" height="480" alt="Screenshot (3199)" src="https://github.com/user-attachments/assets/a88a9462-cc75-4fca-b0e1-2dbe60cb171d" />



## RESULT

Thus, the Assembly Language Programs for 8086 to perform arithmetic operations (Addition, Subtraction, Multiplication, and Division) using both direct and indirect methods were successfully written and executed using MASM.
