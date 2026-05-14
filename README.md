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
<img width="400" height="664" alt="image" src="https://github.com/user-attachments/assets/b5a7062d-e294-47cd-9683-a40de25e82de" />


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

| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
|       1200   :  12       |            1204 : 24   |
|                          |                         |
|         1200  : 34        |       1205 :68         |
|                          |                           |
|          1202 :12         |                          |
|                           |                           |
|          1203: 34          |                           |
----------------------------------------------------------
#### Manual Calculations\
<img width="600" height="300" alt="image" src="https://github.com/user-attachments/assets/1b425415-8809-4e60-bf3e-4a8a95e66119" />

(Add your calculation here)

---<img width="85" height="168" alt="Screenshot 2026-05-14 120859" src="https://github.com/user-attachments/assets/54275ce8-43ed-467a-9eee-a55762447f71" />


## OUTPUT IMAGE FROM MASM SOFTWARE

## 2. SUBTRACTION

#### Algorithm

1. Initialize memory and store 1st data.
2. Increment to get 2nd data.
3. Move 2nd data to accumulator.
4. Subtract memory content.
5. Store result.

## FLOWCHART

<img width="378" height="497" alt="image" src="https://github.com/user-attachments/assets/564c3c7a-33ce-4a1c-8920-beb5c24b9b47" />


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
| ----------------------- | ------------------------ |
|       1200   :  12       |            1204 : 00   |
|                          |                         |
|         1200  : 34        |       1205 :00         |
|                          |                           |
|          1202 :12         |                          |
|                           |                           |
|          1203: 34          |                           |
----------------------------------------------------------

#### Manual Calculations

<img width="600" height="300" alt="image" src="https://github.com/user-attachments/assets/1accdd8f-afbf-4cbb-b7c0-99cbad2e5176" />
<img width="83" height="180" alt="Screenshot 2026-05-14 120928" src="https://github.com/user-attachments/assets/7611e904-a35b-4376-93b9-f7e8d845a608" />

(Add your calculation here)

---


## OUTPUT SCREEN FROM MASM SOFTWARE

## 3. MULTIPLICATION

#### Algorithm

1. Initialize memory and store operands.
2. Move operands to registers.
3. Multiply.
4. Store result.

##FLOWCHART


<img width="569" height="506" alt="image" src="https://github.com/user-attachments/assets/88be88ff-2896-4a88-b73d-84ccffd2fcf9" />



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
| ----------------------- | ------------------------ |
|       1200   :  12       |            1204 : 44   |
|                          |                         |
|         1200  : 34        |       1205 :51        |
|                          |                           |
|          1202 :12         |      1206 :97             |
|                           |                           |
|          1203: 34          |       1207  :0A           |
----------------------------------------------------------
#### Manual Calculations

(Add your calculation here)
<img width="600" height="300" alt="image" src="https://github.com/user-attachments/assets/30807205-5dc7-47eb-a46f-52c77ecac463" />

<img width="90" height="222" alt="Screenshot 2026-05-14 121022" src="https://github.com/user-attachments/assets/33da474d-5ae0-4e61-b456-7c8c516ed30f" />

---

## OUTPUT SCREEN FROM MASM SOFTWARE

## 4. DIVISION

#### Algorithm

1. Load memory location of operands.
2. Perform division.
3. Store result.

   ## FLOWCHART


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
| ----------------------- | ------------------------ |
|       1200   :  12       |            1204 : 01   |
|                          |                         |
|         1200  : 34        |       1205 : 00        |
|                          |                           |
|          1202 :12         |       1206 :00 |
|                           |                           |
|          1203: 34          |                           |
----------------------------------------------------------

#### Manual Calculations
<img width="600" height="300" alt="image" src="https://github.com/user-attachments/assets/feece72d-b207-4a83-a928-495c0c81951b" />


(Add your calculation here)

---<img width="89" height="237" alt="Screenshot 2026-05-14 121008" src="https://github.com/user-attachments/assets/a7b3e360-0c4d-4b2c-a2fc-8354910841d7" />

## OUTPUT FROM MASM SOFTWARE



## RESULT

Thus, the Assembly Language Programs for 8086 to perform arithmetic operations (Addition, Subtraction, Multiplication, and Division) using both direct and indirect methods were successfully written and executed using MASM.

