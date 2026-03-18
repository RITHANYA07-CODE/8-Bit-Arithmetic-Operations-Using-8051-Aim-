# 8-Bit-Arithmetic-Operations-Using-8051

## Aim:
To perform 8-bit arithmetic operations such as addition, subtraction, multiplication, and division using the 8051 microcontroller.

## Apparatus Required:

•	Laptop with Keil uVision software

## Algorithm:

## For Addition:
1.	Load the first number from memory location 30H into register A.
2.	Load the second number from memory location 31H into register B.
3.	Add the contents of registers A and B.
4.	Store the result in memory location 40H.
5.	Store the carry (if any) in 41H.

## Program:
```
  MOV A,30H;
  ADD A,31H;
  MOV 40H,A;
  JNC NEXT ;
  MOV 41H,#01H;
  SJMP END_PROGRAM;
  NEXT:MOV 41H,#00H;
  END_PROGRAM:NOP;
  END
```

## Output:

<img width="952" height="329" alt="Screenshot 2026-03-13 161557" src="https://github.com/user-attachments/assets/8141ea1e-9aaf-4f9a-aba6-a71957ad1141" />

<img width="954" height="331" alt="Screenshot 2026-03-13 161746" src="https://github.com/user-attachments/assets/d09f36e4-4429-4150-b22e-ac8598282b76" />
   
## For Subtraction:
1.	Load the first number from memory location 30H into register A.
2.	Load the second number from memory location 31H into register B.
3.	Subtract B from A.
4.	Store the result in memory location 40H.

## Program:
```
  ORG 0000H
  MOV A,30H
  SUBB A,31H
  MOV 40H,A
  JNC NEXT 
  MOV 41H,#01H;
  SJMP END_PROGRAM;
  NEXT:MOV 41H,#00H;
  END_PROGRAM:NOP;
  END
```

## Output:

<img width="955" height="271" alt="Screenshot 2026-03-16 110404" src="https://github.com/user-attachments/assets/1cee95cf-13e1-4eb1-96ad-127ec4330f76" />

<img width="957" height="251" alt="Screenshot 2026-03-16 110347" src="https://github.com/user-attachments/assets/fe14b4b6-fc5c-42be-958f-9fc5de091c16" />


## For Multiplication:
1.	Load the first number from memory location 30H into register A.
2.	Load the second number from memory location 31H into register B.
3.	Multiply A and B.
4.	Store the lower byte of the result in memory location 40H.
5.	Store the higher byte of the result in memory location 41H.

## Program:
```
ORG 0000H
MOV A, 30H 
MOV B, 31H
MUL AB
MOV 40H, A 
MOV 41H, B
END
```

## Output:

<img width="519" height="198" alt="Screenshot 2026-03-16 110958" src="https://github.com/user-attachments/assets/8465231f-2ca3-49e6-850c-92b712470d78" />

<img width="521" height="200" alt="Screenshot 2026-03-16 111007" src="https://github.com/user-attachments/assets/33428f45-0ecb-400c-baae-f42de62e2f91" />


## For Division:
1.	Load the dividend from memory location 30H into register A.
2.	Load the divisor from memory location 31H into register B.
3.	Divide A by B.
4.	Store the quotient in memory location 40H.
5.	Store the remainder in memory location 41H.


## Program:
```
ORG 0000H
MOV A, 30H
MOV B, 31H
DIV AB
MOV 40H, A
MOV 41H, B 
END
```

## Output:

<img width="954" height="270" alt="Screenshot 2026-03-16 111400" src="https://github.com/user-attachments/assets/02947277-f913-44df-91da-6c33b6e9e69e" />

<img width="957" height="271" alt="Screenshot 2026-03-16 111416" src="https://github.com/user-attachments/assets/fe8a9279-53f5-47d7-bda8-ad37e2a57890" />

## Result:
The 8-bit arithmetic operations using the 8051 microcontroller have been successfully executed and verified using Keil software.

