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

#### MANUAL CALCULATION

<img width="1600" height="658" alt="WhatsApp Image 2026-05-11 at 9 41 26 AM" src="https://github.com/user-attachments/assets/a65e1e1c-61a8-4753-9273-173251635f96" />


#### OUTPUT TABLE

<img width="1600" height="1027" alt="WhatsApp Image 2026-05-11 at 9 41 44 AM" src="https://github.com/user-attachments/assets/bbb5e501-333a-46e6-875e-53881dc45158" />


---

## OUTPUT IMAGE FROM MASM SOFTWARE
<img width="1395" height="1044" alt="WhatsApp Image 2026-05-11 at 9 41 58 AM" src="https://github.com/user-attachments/assets/bef18331-d373-49c3-9afb-b6f8e5215dc1" />



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
<img width="1537" height="1044" alt="WhatsApp Image 2026-05-11 at 9 43 48 AM" src="https://github.com/user-attachments/assets/4706d60f-a0b1-4be4-8f70-5e6f1b377f40" />




#### Manual Calculations

<img width="1600" height="900" alt="WhatsApp Image 2026-05-11 at 9 43 28 AM" src="https://github.com/user-attachments/assets/5a73a6e9-db1a-4a17-9c82-1a61449af663" />


---


## OUTPUT SCREEN FROM MASM SOFTWARE
<img width="1600" height="1027" alt="WhatsApp Image 2026-05-11 at 9 44 03 AM" src="https://github.com/user-attachments/assets/5d1ab6ff-a2bf-43d0-be88-28d8cce3f67f" />


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
<img width="1600" height="958" alt="WhatsApp Image 2026-05-11 at 9 44 38 AM" src="https://github.com/user-attachments/assets/71b7d16d-95f8-4628-adb9-390a6ab2898d" />


#### Manual Calculations
<img width="1600" height="900" alt="WhatsApp Image 2026-05-11 at 9 44 21 AM" src="https://github.com/user-attachments/assets/7be59147-9d2e-42a8-8c98-28957a662bc7" />




---

## OUTPUT SCREEN FROM MASM SOFTWARE
<img width="1600" height="900" alt="WhatsApp Image 2026-05-11 at 9 44 54 AM" src="https://github.com/user-attachments/assets/89358966-3e70-48af-927e-a670ba37a7ca" />


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

<img width="1600" height="1003" alt="WhatsApp Image 2026-05-11 at 9 45 38 AM" src="https://github.com/user-attachments/assets/cc2b73cc-1ab5-4d0f-82bb-fd4e8b966931" />

#### Manual Calculations

<img width="1600" height="900" alt="WhatsApp Image 2026-05-11 at 9 45 51 AM" src="https://github.com/user-attachments/assets/32b48774-82b7-48a7-9250-661cb777550f" />


---
## OUTPUT FROM MASM SOFTWARE
<img width="1567" height="1044" alt="WhatsApp Image 2026-05-11 at 9 46 16 AM" src="https://github.com/user-attachments/assets/ad07b47f-60c3-4e71-9593-e77b3ef72ef2" />




## RESULT

Thus, the Assembly Language Programs for 8086 to perform arithmetic operations (Addition, Subtraction, Multiplication, and Division) using both direct and indirect methods were successfully written and executed using MASM.

