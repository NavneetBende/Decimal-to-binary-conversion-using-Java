# Decimal-to-binary-conversion-using-Java

Decimal to Binary conversion using Java
In this article we will create program for decimal to binary conversion using java. For this purpose we need to ask a decimal number from user and convert that decimal number to its binary equivalent form and then print the converted number on to the screen.
Decimal to binary
Working
For conversion, we divide the decimal number by 2 and get the quotient 
for the next iteration and continuously store the remainder value in an 
array in reverse order till the decimal number is greater than 0. For better understanding with an example just have a look towards the diagram 
shown at the right.

Example : Decimal number 5 = 101 in binary representation.
Decimal to binary conversion using java
Related Pages
Octal to Decimal conversion

Hexadecimal to Decimal conversion

Decimal to Binary conversion

Decimal to Octal Conversion

Decimal to Hexadecimal Conversion

Binary to Octal conversion

Algorithm
Initialize a empty array name binary
While decimal is greater then zero
If decimal is even r equals to 0 and else set 1
Append r to binary
Set decimal as half of its value
Java Code
Run
//Java program to convert decimal number to binary number
public class Main
{
	public static void main(String args[])
	{   
		//Decimal Number
		int decimal = 12;
		//integer array for storing binary digits 
		int binary[] = new int[20];
		int i = 0; 
		//writing logic for the conversion 
		while(decimal > 0)
		{       
			int r = decimal % 2;
			binary[i++] = r;
			decimal = decimal/2;
		}
		//printing result
		System.out.print("Binary number : ");
		for(int j = i-1 ; j >= 0 ; j--)
		System.out.print(binary[j]+"");
	}
}
Output
Binary number : 1100
