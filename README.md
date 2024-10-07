# unit-2-6-assignment

## API and Documentation
Documentation for the shape classes can be found [here](https://coderunner.projectstem.org/docs/shapes/index.html).

## Git Config
```
git config user.name "user"
git config user.email "email"
```

## Compiling and Running Java Programs
Note that since the shape classes are separate classes, you will need to compile ALL the files (at least one time).  You can do this by running
```
javac *.java
```
The star means to compile every file that is a Java file type.

Run your code by running
```
java Main.java
```

After you compile the shape classes, you only need to compile and run `Main.java` as usual.

## Problem 1
Write code that takes input from the user for the radius (double) of a circle, and create a circle with that radius. The program should then print a sentence with the circumference and area of the circle. You should use the appropriate `Circle` methods to obtain the circumference and area of the circle rather than calculating these values yourself.

Sample run:
```
Enter the radius of the circle:
> 3
A circle with a radius of 3.0 has a circumference of 18.84955592153876 and an area of 28.274333882308138
```
Hint: You can approach this problem by saving the double (radius) as a variable and then creating the Circle, or you can create the Circle and use methods from the Circle class to set the radius.

## Problem 2
Write code that takes an integer input and a double input from the user, and creates a `RegularPolygon` object where the integer is the number of sides and the double is the side length. The code should calculate the area of the `RegularPolygon`, print the area, then increment the number of sides of the `RegularPolygon` by two and print the new area.

Sample run:
```
Enter number of sides:
> 4
Enter the side length:
> 5.6
Area with 4 sides: 31.36
Incrementing the number of sides by two
Area with 6 sides: 81.47566998803998
```
Hint: You can use either the `addSides` or `setNumSides` methods from the `RegularPolygon` class to increment the number of sides by 2.

## Sample Solutions
```java
import java.util.Scanner;

public class Main
{
	public static void main(String[] args)
	{
		// Problem 2
		Scanner sc = new Scanner(System.in);
		int numSide;
		double sideLength;
		RegularPolygon rp;

		System.out.println("Enter number of sides:");
		numSide = sc.nextInt();

		System.out.println("Enter the side length:");
		sideLength = sc.nextDouble();

		rp = new RegularPolygon(numSide, sideLength);

		System.out.println("Area with " + rp.getNumSides() + " sides: " + rp.getArea());
		
		rp.addSides(2);
		System.out.println("Incrementing the number of sides by two");
		
		System.out.println("Area with " + rp.getNumSides() + " sides: " + rp.getArea());
	}
}
```
