# Calculator
import java.util.Scanner;

//class calculator implementing basic functionality
class Calculator
{

//add method
public int add (int num1, int num2)
{

return num1 + num2;
}
//subtract method
public int subtract (int num1, int num2)
{
return num1 - num2;

}
//multiply method
public int multiply (int num1, int num2)
{
return num1 * num2;
}
//divide method
public int divide (int num1, int num2)
{

if (num2 == 0)
{
System.out.println ("num2 cannot be zero");
return 0;
}
else
return num1 / num2;
}

//square method
public int square (int num1)
{
return num1 * num1;
}}

//MagicCalculator class extending calculator class
class MagicCalculator extends Calculator
{
//factorial method
public static int factorial (int n)
{
return (n == 1 || n == 0) ? 1 : n * factorial (n - 1);
}
//main functionality
public static void main (String[]args)
{
//object of calculator class
Calculator calculator = new Calculator ();
//scanner class to take input
Scanner sc = new Scanner (System.in);

System.out.print("Enter Number: ");

int num = sc.nextInt ();
//calling square method
int sq = calculator.square (num);

System.out.println ("The Square Root of " + num + " is: " + sq);
//Enter in degrees then converting to radians
System.out.println ("Enter angle in degrees :");

double degree = sc.nextDouble ();

double radians = Math.toRadians (degree);

System.out.println ("Sin is: " + Math.sin (radians));
System.out.println ("Cosine is: " + Math.cos (radians));
System.out.println ("Tangent is: " + Math.tan (radians));
System.out.println ("Factorial of "+ num + " is: " + factorial (num));
}
} 
