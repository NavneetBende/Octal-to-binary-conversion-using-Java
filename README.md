# Octal-to-binary-conversion-using-Java

Octal to Binary Conversion using Java
Here, on this page, we will discuss octal to binary conversion using java. For this purpose, we need to ask for an octal number from user and convert that octal number to its binary equivalent form and then print the converted number onto the screen.

For conversion, we first convert the octal number into decimal form and then convert the decimal number to a binary number.

Octal to binary conversion using java
Method 1:-
Accept octal number
Convert it into decimal Equivalent
Convert this decimal value into Binary
Make sure you have visited these two pages before moving ahead with the code –

Octal to Decimal conversion
Decimal to Binary Conversion
Method 1 Code in Java
Run
//Java program to convert octal number to binary number
class Main
{
    public static void main(String args[])
    {
        int octal = 12;

        //Declaring variable to store decimal number
        int decimal = 0;
        //Declaring variable to use in power
        int n = 0;

        //writing logic for the octal to decimal conversion
        while(octal > 0)
        {
            int temp = octal % 10;
            decimal += temp * Math.pow(8, n);
            octal = octal/10;
            n++;
        }

        int binary[] = new int[20];
        int i = 0;

        //writing logic for the decimal to binary conversion
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
Enter a octal number : 12
Binary number : 1010
Related Pages
Decimal to Binary conversion

Decimal to Octal Conversion

Decimal to Hexadecimal Conversion

Permutations in which n people can occupy r seats in a classroom 

Octal to Binary conversion

Quadrants in which a given coordinate lies

Method 2
Each digit of an octal number can be converted into its binary Equivalent (see image)

Binary Representation for Octal digit:
0 => 000
1 => 001
2 => 010
3 => 011
4 => 100
5 => 101
6 => 110
7 => 111
Octal to binary conversion using java
Octal to Binary in Java
Method 2 Code in Java:
Run
import java.util.HashMap;
class Main
{
    public static void main(String[] args)
    {
        HashMap b =new HashMap();
        b.put(0,"000");
        b.put(1,"001");
        b.put(2,"010");
        b.put(3,"011");
        b.put(4,"100");
        b.put(5,"101");
        b.put(6,"110");
        b.put(7,"111");

        String result =" ";
        long num = 347;
        long n=num;
        while(n !=0)
        {
            int rem=0;
            rem=(int)n%10;
            if(n!=0)
            {
                result = b.get(rem)+result;

            }
            n=n/10;

        }
        System.out.println(result);
    }
}
Output
Enter a octal number : 347
Binary number : 011100111
