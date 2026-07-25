
# **Lab 1: Introduction to Digital Logic**

# Logisim Evolution Installation Process (Arch Linux)

## Installation

Open the terminal and install Logisim Evolution using the AUR helper (`yay`):

```bash
yay -S logisim-evolution
```

During installation:

- Press **Enter** to keep the default option (`None`) for **cleanBuild**.
- Press **Enter** to skip viewing **diffs**.
- Wait while the package is downloaded, compiled, and built.
- When prompted:

```text
:: Proceed with installation? [Y/n]
```

Type **Y** and press **Enter**.

If prompted for the administrator password, enter your **sudo password**.

After successful installation, launch the application using:

```bash
logisim-evolution
```

## Installation Output (Successful)

The following messages indicate that the installation completed successfully:

```text
==> Finished making: logisim-evolution 4.1.0-1
:: Processing package changes...
(1/1) reinstalling logisim-evolution
:: Running post-transaction hooks...
```
![alt text](image-32.png)
![alt text](image-33.png)
![alt text](image-34.png)

## Result

Logisim Evolution was successfully installed and is ready for use.

## **Experiment 1: Implementation of OR Gate using NOR Gates**

**Description:**\
In this experiment, we will implement an OR gate using only NOR gates. The OR gate is a fundamental digital logic gate that outputs true (1) when at least one of its inputs is true (1). The NOR gate, on the other hand, is a universal gate that can be used to create any other logic gate, including the OR gate.

**Procedure:**
1. **Understanding the NOR Gate:**
   - A NOR gate is a combination of an OR gate followed by a NOT gate. It outputs true (0) only when all its inputs are false (0).
   - The truth table for a 2-input NOR gate is as follows:

   | Input A | Input B | Output (A NOR B) |
   |---------|---------|------------------|
   |    0    |    0    |         1        |
   |    0    |    1    |         0        |
   |    1    |    0    |         0        |
   |    1    |    1    |         0        |

2. **Implementing the OR Gate using NOR Gates:**
   - To implement an OR gate using NOR gates, we can use the following logic:
   - The OR gate can be expressed in terms of NOR gates as follows:
   - OR(A, B) = NOT(NOR(A, B))
   - This means that we can first use a NOR gate to get the output of NOR(A , B), and then use another NOR gate to invert that output.  

3. **Circuit Design:**
   - Connect the inputs A and B to the first NOR gate.
   ![alt text](image.png)

   - Connect the output of the first NOR gate to both inputs of the second NOR gate to invert the output.
   ![alt text](image-1.png)

4. **Testing the Circuit:**
   - Apply different combinations of inputs (A and B) to the circuit and observe the output.
   - Verify that the output matches the expected results of an OR gate.
   
   ![alt text](image-2.png)

   ![alt text](image-3.png)


**Conclusion:**
In this experiment, we successfully implemented an OR gate using only NOR gates. By understanding the properties of NOR gates and their ability to create other logic gates, we were able to demonstrate the versatility of digital logic design. This exercise reinforces the concept of universal gates and their applications in digital circuits.


## **Experiment 2: Implementation of OR Gate using NAND Gates**

**Description:**\
In this experiment, we will implement an OR gate using only NAND gates. The NAND gate is another universal gate that can be used to create any other logic gate, including the OR gate.

**Procedure:**
1. **Understanding the NAND Gate:**
   - A NAND gate is a combination of an AND gate followed by a NOT gate. It outputs false (0) only when all its inputs are true (1).
   - The truth table for a 2-input NAND gate is as follows:
   
   | Input A | Input B | Output (A NAND B) |
   |---------|---------|-------------------|
   |    0    |    0    |        1          |
   |    0    |    1    |        1          |
   |    1    |    0    |        1          |
   |    1    |    1    |        0          |

2. **Implementing the OR Gate using NAND Gates:**
   - To implement an OR gate using NAND gates, we can use the following logic:
   - OR(A, B) = NOT(NAND(NOT(A), NOT(B)))
   - This means that we can first use two NAND gates to invert the inputs A and B, and then use a third NAND gate to combine the inverted inputs.
3. **Circuit Design:**
   - Connect the inputs A and B to the first two NAND gates to invert them.
   ![alt text](image-4.png)

    - Connect the outputs of the first two NAND gates to the inputs of the third NAND gate to get the final output.
    ![alt text](image-5.png)

4. **Testing the Circuit:**
   - Apply different combinations of inputs (A and B) to the circuit and observe the output.
   - Verify that the output matches the expected results of an OR gate.

   ![alt text](image-6.png)
   ![alt text](image-7.png)


**Conclusion:**
   In this experiment, we successfully implemented an OR gate using only NAND gates. By understanding the properties of NAND gates and their ability to create other logic gates, we were able to demonstrate the versatility of digital logic design. This exercise reinforces the concept of universal gates and their applications in digital circuits.


## **Experiment 3: Implementation of AND Gate using NOR Gates**

**Description:**\
In this experiment, we will implement an AND gate using only NOR gates. The AND gate is a fundamental digital logic gate that outputs true (1) only when both of its inputs are true (1). The NOR gate, being a universal gate, can be used to create an AND gate as well.

**Procedure:**
1. **Understanding the AND Gate:**
   - An AND gate outputs true (1) only when both of its inputs are true (1). The truth table for a 2-input AND gate is as follows:

   | Input A | Input B | Output (A AND B) |
   |---------|---------|-------------------|
   |    0    |    0    |        0          |
   |    0    |    1    |        0          |
   |    1    |    0    |        0          |
   |    1    |    1    |        1          |

2. **Implementing the AND Gate using NOR Gates:**
   - To implement an AND gate using NOR gates, we can use the following logic:
   - AND(A, B) = NOT(NOR(NOT(A), NOT(B)))
   - This means that we can first use two NOR gates to invert the inputs A and B, and then use a third NOR gate to combine the inverted inputs.

3. **Circuit Design:**
   - Connect the inputs A and B to the first two NOR gates to invert them.
   ![alt text](image-8.png)
    - Connect the outputs of the first two NOR gates to the inputs of the third NOR gate to get the final output.
    ![alt text](image-9.png)

4. **Testing the Circuit:**
   - Apply different combinations of inputs (A and B) to the circuit and observe the output.
   - Verify that the output matches the expected results of an AND gate.
   ![alt text](image-10.png)
   ![alt text](image-11.png)

**Conclusion:**
In this experiment, we successfully implemented an AND gate using only NOR gates. By understanding the properties of NOR gates and their ability to create other logic gates, we were able to demonstrate the versatility of digital logic design. This exercise reinforces the concept of universal gates and their applications in digital circuits.

## **Experiment 4: Implementation of AND Gate using NAND Gates**

**Description:**\
In this experiment, we will implement an AND gate using only NAND gates. The NAND gate is a universal gate that can be used to create any other logic gate, including the AND gate.

**Procedure:**
1. **Understanding the AND Gate:**
   - An AND gate outputs true (1) only when both of its inputs are true (1). The truth table for a 2-input AND gate is as follows:

    | Input A | Input B | Output (A AND B) |
    |---------|---------|-------------------|
    |    0    |    0    |        0          |
    |    0    |    1    |        0          |
    |    1    |    0    |        0          |
    |    1    |    1    |        1          |


2. **Implementing the AND Gate using NAND Gates:**
   - To implement an AND gate using NAND gates, we can use the following logic:
   - AND(A, B) = NOT(NAND(A, B))
   - This means that we can first use a NAND gate to get the output of NAND(A, B), and then use another NAND gate to invert that output.

3. **Circuit Design:**
   - Connect the inputs A and B to the first NAND gate.
   ![alt text](image-12.png)
    - Connect the output of the first NAND gate to both inputs of the second NAND gate to invert the output.
    ![alt text](image-13.png)

4. **Testing the Circuit:**
   - Apply different combinations of inputs (A and B) to the circuit and observe the output.
   - Verify that the output matches the expected results of an AND gate.
   ![alt text](image-14.png)
   ![alt text](image-15.png)

**Conclusion:**
In this experiment, we successfully implemented an AND gate using only NAND gates. By understanding the properties of NAND gates and their ability to create other logic gates, we were able to demonstrate the versatility of digital logic design. This exercise reinforces the concept of universal gates and their applications in digital circuits.

## **Experiment 5: Implementation of NOT Gate using NOR Gates**


**Description:**\
In this experiment, we will implement a NOT gate using only NOR gates. The NOT gate is a fundamental digital logic gate that outputs the opposite value of its input. The NOR gate, being a universal gate, can be used to create a NOT gate as well.

**Procedure:**
1. **Understanding the NOT Gate:**
   - A NOT gate outputs true (1) when its input is false (0) and outputs false (0) when its input is true (1). The truth table for a NOT gate is as follows:

   | Input A | Output (NOT A) |
   |---------|----------------|
   |    0    |        1       |
   |    1    |        0       |

2. **Implementing the NOT Gate using NOR Gates:**
   - To implement a NOT gate using NOR gates, we can use the following logic:
   - NOT(A) = NOR(A, A)
   - This means that we can connect the input A to both inputs of a NOR gate to get the inverted output.

3. **Circuit Design:**
   - Connect the input A to both inputs of the NOR gate.
   ![alt text](image-16.png)

4. **Testing the Circuit:**
   - Apply different values of input A to the circuit and observe the output.
   - Verify that the output matches the expected results of a NOT gate.

   ![alt text](image-17.png)

**Conclusion:**
In this experiment, we successfully implemented a NOT gate using only NOR gates. By understanding the properties of NOR gates and their ability to create other logic gates, we were able to demonstrate the versatility of digital logic design. This exercise reinforces the concept of universal gates and their applications in digital circuits.


## **Experiment 6: Implementation of NOT Gate using NAND Gates**

**Description:**\
In this experiment, we will implement a NOT gate using only NAND gates. The NOT gate is a fundamental digital logic gate that outputs the opposite value of its input. The NAND gate, being a universal gate, can be used to create a NOT gate as well.

**Procedure:**
1. **Understanding the NOT Gate:**
   - A NOT gate outputs true (1) when its input is false (0) and outputs false (0) when its input is true (1). The truth table for a NOT gate is as follows:

   | Input A | Output (NOT A) |
   |---------|----------------|
   |    0    |        1       |
   |    1    |        0       |

2. **Implementing the NOT Gate using NAND Gates:**
   - To implement a NOT gate using NAND gates, we can use the following logic:
   - NOT(A) = NAND(A, A)
   - This means that we can connect the input A to both inputs of a NAND gate to get the inverted output.

3. **Circuit Design:**
   - Connect the input A to both inputs of the NAND gate.

   ![alt text](image-18.png)

4. **Testing the Circuit:**
   - Apply different values of input A to the circuit and observe the output.
   - Verify that the output matches the expected results of a NOT gate.

   ![alt text](image-19.png)

**Conclusion:**
In this experiment, we successfully implemented a NOT gate using only NAND gates. By understanding the properties of NAND gates and their ability to create other logic gates, we were able to demonstrate the versatility of digital logic design. This exercise reinforces the concept of universal gates and their applications in digital circuits.


## **Experiment 7: Implementation of Full Adder and testing it.**

**Description:**\
In this experiment, we will implement a Full Adder circuit using basic logic gates. A Full Adder is a digital circuit that performs the addition of three binary bits: two significant bits and a carry bit. The Full Adder produces a sum and a carry output.

**Procedure:**
1. **Understanding the Full Adder:**
   - A Full Adder takes three inputs: A, B, and Cin (carry input). It produces two outputs: Sum and Cout (carry output). The truth table for a Full Adder is as follows:

   | Input A | Input B | Cin | Sum | Cout |
   |---------|---------|-----|-----|------|
   |    0    |    0    |  0  |  0  |  0   |
   |    0    |    0    |  1  |  1  |  0   |
   |    0    |    1    |  0  |  1  |  0   |
   |    0    |    1    |  1  |  0  |  1   |
   |    1    |    0    |  0  |  1  |  0   |
   |    1    |    0    |  1  |  0  |  1   |
   |    1    |    1    |  0  |  0  |  1   |
   |    1    |    1    |  1  |  1  |  1   |

2. **Implementing the Full Adder Circuit:**
   - The Full Adder can be implemented using two Half Adders and an OR gate.
   - The first Half Adder takes inputs A and B and produces a sum (S1) and a carry (C1).
   - The second Half Adder takes the sum (S1) from the first Half Adder and the carry input (Cin) to produce the final sum (Sum) and a carry (C2).
   - The final carry output (Cout) is obtained by ORing the two carry outputs (C1 and C2) from the two Half Adders.

3. **Circuit Design:**
   - Connect the inputs A and B to the first Half Adder.
   ![alt text](image-20.png)
   - Connect the sum output (S1) from the first Half Adder and the carry input (Cin) to the second Half Adder.
   ![alt text](image-21.png)
   - Connect the carry outputs (C1 and C2) from both Half Adders to an OR gate to produce the final carry output (Cout).
   ![alt text](image-22.png)

4. **Testing the Circuit:**
   - Apply different combinations of inputs (A, B, and Cin) to the circuit and observe the outputs (Sum and Cout).
   - Verify that the outputs match the expected results of a Full Adder.
   ![alt text](image-23.png)
   ![alt text](image-24.png)
   ![alt text](image-25.png)
   For 8 bit the main full adder shows 10 in s and 0 in carry out. If we think about 1 bit the sum is 0 and carry out is 1 which is correct according to the circuit we have designed.
   ![alt text](image-26.png)
   Same as before for 8 bit the main full adder shows 11 in s and 0 in carry out. If we think about 1 bit the sum is 1 and carry out is 1 which is correct according to the circuit we have designed.

**Conclusion:**
In this experiment, we successfully implemented a Full Adder circuit using basic logic gates. By understanding the properties of Half Adders and their combination to form a Full Adder, we were able to demonstrate the addition of binary numbers. This exercise reinforces the concept of digital arithmetic and its applications in digital circuits. The Full Adder is a crucial component in the design of arithmetic logic units (ALUs) and other digital systems that require binary addition.


## **Experiment 8: Implementation of Binary to BCD Converter**

**Description:**\
In this experiment, we will implement a Binary to BCD (Binary-Coded Decimal) converter using basic logic gates. A Binary to BCD converter is a digital circuit that converts a binary number into its equivalent BCD representation. BCD is a form of decimal representation where each digit of a decimal number is represented by its binary equivalent.

**Procedure:**
1. **Understanding Binary to BCD Conversion:**
   - A Binary to BCD converter takes a binary input and produces a BCD output.
   - For example, the binary number 1010 (which is 10 in decimal) can be represented in BCD as 0001 0000 (1 and 0 in BCD).
   - The truth table for a 4-bit binary input and its corresponding BCD output is as follows:

| Binary Code |   |   |   | BCD Code |   |   |   |
|:-----------:|:-:|:-:|:-:|:--------:|:-:|:-:|:-:|
| B₃ | B₂ | B₁ | B₀ | D₄ | D₃ | D₂ | D₁ |
| 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 |
| 0 | 0 | 0 | 1 | 0 | 0 | 0 | 1 |
| 0 | 0 | 1 | 0 | 0 | 0 | 1 | 0 |
| 0 | 0 | 1 | 1 | 0 | 0 | 1 | 1 |
| 0 | 1 | 0 | 0 | 0 | 1 | 0 | 0 |
| 0 | 1 | 0 | 1 | 0 | 1 | 0 | 1 |
| 0 | 1 | 1 | 0 | 0 | 1 | 1 | 0 |
| 0 | 1 | 1 | 1 | 0 | 1 | 1 | 1 |
| 1 | 0 | 0 | 0 | 1 | 0 | 0 | 0 |
| 1 | 0 | 0 | 1 | 1 | 0 | 0 | 1 |
| 1 | 0 | 1 | 0 | 1 | 0 | 1 | 0 |
| 1 | 0 | 1 | 1 | 1 | 0 | 1 | 1 |
| 1 | 1 | 0 | 0 | 1 | 1 | 0 | 0 |
| 1 | 1 | 0 | 1 | 1 | 1 | 0 | 1 |
| 1 | 1 | 1 | 0 | 1 | 1 | 1 | 0 |
| 1 | 1 | 1 | 1 | 1 | 1 | 1 | 1 |

2. **Implementing the Binary to BCD Converter Circuit:**
   - The Binary to BCD converter can be implemented using a combination of logic gates to map the binary inputs to their corresponding BCD outputs.
   - The circuit design will involve creating logic expressions for each BCD output bit (D₄, D₃, D₂, D₁) which will be displayed on the BCD to seven-segment display based on the binary input bits (B₃, B₂, B₁, B₀).

3. **Circuit Design:**
   - Connect the binary input bits (B₃, B₂, B₁, B₀) to the Binary to BCD converter circuit.
   ![alt text](image-27.png)
   - The circuit will produce the corresponding BCD output bits (D₄, D₃, D₂, D₁) based on the input binary number which will be displayed on the BCD to seven-segment display.
   ![alt text](image-28.png)
4. **Testing the Circuit:**
   - Apply different combinations of binary inputs (B₃, B₂, B₁, B₀) to the circuit and observe the BCD outputs (D₄, D₃, D₂, D₁).
   - Verify that the outputs match the expected results of the Binary to BCD conversion.
   ![alt text](image-29.png)
   ![alt text](image-30.png)
   ![alt text](image-31.png)

**Conclusion:**
In this experiment, we successfully implemented a Binary to BCD converter using basic logic gates. By understanding the properties of binary numbers and their corresponding BCD representations, we were able to demonstrate the conversion process. This exercise reinforces the concept of digital number systems and their applications in digital circuits, particularly in systems that require decimal representation of binary numbers, such as digital displays and calculators.


## <h1 align='center'>  End of Lab 1 Report  </h1>