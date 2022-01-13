# core-code
Core Code Bootcamp
1. video viewed. 
Compilation is faster and keeps the source private, however it is not crossplatform and requires the extra compiling step.
Interpretation is cross platform, esier debugging, however slower and has public source.
2.Java can be considered both a compiled and an interpreted language because its source code is first compiled into a binary byte-code. This byte-code runs on the Java Virtual Machine (JVM), which is usually a software-based interpreter.
3. 
import java.util.Scanner;
public class Main {
 public static void main(String[] args) {
  Scanner in = new Scanner(System.in);
    System.out.print("Input in quetzales: ");
      int num1 = in.nextInt();
  System.out.println(num1 / 7.8);
 }}
 4. Read about pseudocode and took a look at the examples.
 5. Pseudocode helps us get an idea of what variables, structure and conditions we might want to consider in our actual code.
 6. 
 Get the year user was born
 Set current year
 Subtract that year from current year
 Result equals approximate age of user
 7. Read about flowcharts and how they help us get an idea of how to build the structure of our projects. 
 8. Flow charts are helpful to us developers, because they give us an idea of how to structure our projects. For instance in java, we would be able to define classes before hand, and that helps us have a better idea of how the whole system works.
 9.  Watched the video Lenguajes de alto y bajo nivel. Lenguajes de bajo nivel como C se utilizan mucho para la programación en la electrónica, sin embargo no es tan utilizado hoy en día. Hoy en día está la tecnología de assembly que le permite a los navegadores entender código de bajo nivel e interpretarlo. 

Day 2

1. los numeros binarios tienen una base de 2, los decimales de 10 y los hexadecimales de 16. Información adquirida en http://www.eecs.umich.edu/courses/eecs270/270lab/270_docs/HexNumSys.pdf
2. 1987 - binary 111 11000011 / hexadecimal (7C3)₁₆ = (7 × 16²) + (12 × 16¹) + (3 × 16⁰) = (1987)₁₀ / decimal 1987
3. 51966 - binary 11001010 11111110 / hexadecimal (CAFE)₁₆ = (12 × 16³) + (10 × 16²) + (15 × 16¹) + (14 × 16⁰) = (51966)₁₀ 
4. Done
5. 5.1  
.data
	number1: .asciiz "\nIngrese el primer numero: "
	number2: .asciiz "\nIngrese el segundo numero: "
	result_message: .asciiz "\nEl resultado es: "
.text
	main:
		li $v0, 4
		la $a0, number1
		syscall

		li $v0, 5
		syscall

		move $t0, $v0

		li $v0, 4
		la $a0, number2
		syscall

		li $v0, 5
		syscall

		move $t1, $v0

		li $v0, 1
		move $a0, $t0

		add $t2, $t0, $t1

		li $v0, 4
		la $a0 result_message
		syscall

		li $v0, 1
		move $a0, $t2
		syscall
  
  5.2 
  .data
	Myname: .asciiz "\nJorge"
.text
	main:
		li $v0, 4
		la $a0, Myname
		syscall

		li $v0, 5
		syscall
