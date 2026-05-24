# JAVA

**How println and scanner works**
```java
package myFirstProject;
import java.util.Scanner; // This module or library is needed for scanner to work


public class Main {

	public static void main(String[] args) {
		// TODO Auto-generated method stub
		System.out.println("I am king of the world");

		Scanner scanner = new Scanner(System.in);
		
		System.out.println("who are you");
		
		String intro = scanner.nextLine();
		
		
		System.out.println("what is your age ?");
		
		int age = scanner.nextInt(); /* here new line problem arise 
		if used next line after this, To clear that we should use next line */
		
		scanner.nextLine(); // to clear empty read error
		
		
		System.out.println("What is your favourite dish ?");
		String food = scanner.nextLine();


		System.out.println("Welcome, "+ intro);
		if (age >= 18) System.out.println("Enjoy, You got access");
		else System.out.println("Sorry, Not today");
		System.out.println("you like "+ food);
	}

}

```

**GUI**(Graphical user Interface)
Javax.swing.JOptionPane

```java
package myFirstProject;
import javax.swing.JOptionPane;

public class Main {

	public static void main(String[] args) {
		String name = JOptionPane.showInputDialog("what is your name");
		// default read to string, even from a number input
		// to counter that, we use Integer.parseInt()
		int age = Integer.parseInt(JOptionPane.showInputDialog("what is your age"));
				

		JOptionPane.showMessageDialog(null, "Hello " + name + ". You are " + age);
	}
}
```

**Math library in Java**
All functions and finding hyoptenuse
```java
package myFirstProject;
import javax.swing.JOptionPane;

public class Main {
	public static void main(String[] args) {
		double x = 9.3, y = 27.8;
		
		double maxi = Math.max(x, y);
		// all sorts of functions are present, .min(x,y)
		// .round(), .sqrt, .ceil, .floor, .abs(x)
		
		System.out.print("maximum valeu is " + maxi);
		
		double hyp = Math.sqrt(x*x + y*y);
		
		JOptionPane.showMessageDialog(null, "The valeu of longest side is " + hyp);
	}
}
```

**Gaming tasks uses Random**
```java
package myFirstProject;
import java.util.Random;

import javax.swing.JOptionPane;

public class Main {
	public static void main(String[] args) {
		Random random = new Random();
		
		int val = random.nextInt(10); // range from 0 to 9, else all possible numbers
		// have nextBoolean(), nextDouble() too
		
		JOptionPane.showMessageDialog(null, val);
	}
}
```

For to compare two string equal or not

```java
x.equals(y)
```

### How strings work
```java
public class Main {
	public static void main(String[] args) {
		String[] cars = new String[4];
		
		cars[0] = "volvo";
		cars[1] = "bmw";
		cars[2] = "bugatti";
		cars[3] = "mercedes";
		
		for (int i = 0; i <= 3; i++) System.out.println(cars[i]);
	}
}
```

Same with 2D arrays
String[][] cars = new String[5][8];
same with 3d lists

### All imp functions of String
```java
package myFirstProject;
import java.util.Random;
import java.util.Scanner;

import javax.swing.JOptionPane;

public class Main {
	public static void main(String[] args) {
		String name = "Vishnu";
		
		int len = name.length();
		System.out.println("Length of name is " + len);
		boolean isSame = name.equals("vishnu");
		System.out.println("Case sensitive, is it equal ? " + isSame);
		
		isSame = name.equalsIgnoreCase("vishnu");
		System.out.println("Case insensitive, is it equal ? " + isSame);
		
		char pointer = name.charAt(2);
		System.out.println("Pointer at letter "+pointer);
		
		// name.indexOf(), name.isEmpty(), name.toUpperCase(), name.toLowerCase()
		// name.trim() this will remove leading and ending empty space
	}
}

```

**Wrapper Class**
Wrapper class is Reference datatype, not a simple datatype, whoch incorparates many useful functions
		
String is already wrapper, often start with capital first letter
Integer, Boolean, Character, Double, String
int, boolean, char, double, String

```java
Integer a = 70; 
// on using a. ex: a.byteValue(), you can see how many types you do
		
int primitiveNum = 10;
Integer wrapperObj = primitiveNum; // Autoboxing happens here

Integer wrapperObj = 20;
int primitiveNum = wrapperObj; // Unboxing happens here
```

**ArrayList**(Not camel case)
This is pretty similar to vector in Cpp STL, A type of resizable array
even, .size() function is similar between both.

```java
package myFirstProject;
import java.util.ArrayList;

public class Main {
	public static void main(String[] args) {
		ArrayList<String> cities = new ArrayList();
		
		cities.add("New York");
		cities.add("Delhi");
		cities.add("Hyderabad");
		cities.add("Banglore");
		
		cities.set(0, "Mumbai");
		
		for (int i = 0; i < cities.size(); i++) {
			System.out.println(cities.get(i));
		}
		
		cities.remove(1);
		
		System.out.println(cities); // can print a whole list at one go
		
		// .remove() at index, and .clear() completey also works
	}
}
```

Can create 2D array.
ArrayList<ArrayList<String>> cities = new ArrayList();

can use .add(1d array) for 2d array

**Functions**
You can write additional function outside *static public void main()*
but inside *public class main*

```java
package myFirstProject;

public class Main {
	public static void main(String[] args) {
		call();
		call();
		call();
	}
	
	static void call() {
		System.out.println("This function was called.");
	}
}
```

**printf is format specifier** 
int val = scanner.nextInt();
System.out.printf("The value %d is entered", val)
<img width="850" height="331" alt="image" src="https://github.com/user-attachments/assets/4e7a23aa-bff2-48df-a2ca-666d14edfa86" />
