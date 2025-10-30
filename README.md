# FIBONACCI-SERIES

## FIBONACCI SERIES(KEIL)
## AIM
To write and execute an Assembly language program to perform the fibonacci series using 8051 Keil.
---

## APPARATUS REQUIRED
- Personal computer with Keil software
---

## ALGORITHM
1. **Start**
2. **Input**: Read the number `n`.
4. **Initialize**:
   - Set factorial to `1`.
   - Set `i` to `1`.
5. **Loop**: While `i` is less than or equal to `n`:
   - Multiply factorial by `i`.
   - Increment `i` by `1`.
6. **Output**: Store or print the value of factorial.
7. **End**

## PROGRAM
```
ORG 0000H         
MOV R7, #08H      
MOV R0, #30H    
MOV A, #00H        
MOV @R0, A     
INC R0
MOV A, #01H       
MOV @R0, A        
INC R0
MOV A, R7
CLR C
SUBB A, #02H
MOV R7, A
MOV A, #00H        
MOV B, #01H       
NEXT_TERM:
ADD A, B       
MOV @R0, A       
INC R0
MOV R5, A        
MOV A, B          
MOV B, R5          
DJNZ R7, NEXT_TERM
HERE: SJMP HERE     
END

```
## OUTPUT
<img width="997" height="288" alt="Screenshot 2025-10-23 141527" src="https://github.com/user-attachments/assets/874704b5-706c-4891-ae40-0355d825ca37" />

## RESULT
Thus, the fibonacci series is executed successfully using 8051 Keil.
