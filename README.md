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

final is similar to const in cpp

once fixed, can't be changed.

**OOPS IN Java**
Classes and object.
Obcject, An instance of class that may contain attributes and methods.

Constructor is special method, that's get called when object is initialised, and it have same name as class.

Demo code I wrote

Main.java
```java
package firstStepsOfJava;

import java.util.ArrayList;

public class Main {

	public static void main(String[] args) {
		// TODO Auto-generated method stub
		ArrayList<Student> names = new ArrayList<>();
		
		names.add(new Student(101, "Arjun", "CSE", 6.94, 22));
		names.add(new Student(102, "Rahul", "EE", 7.82, 24));
		names.add(new Student(103, "Sneha", "ECE", 8.15, 21));
		names.add(new Student(104, "Priya", "CSE", 6.18, 22));
		names.add(new Student(105, "Kiran", "CSE", 7.72, 23));
		
		names.get(2).updateCGPA(8.42);
		
		for (int i = 0; i < names.size(); i++) {
			names.get(i).displayDetails();
		}
		
		for (int i = 0; i < 5; i++) {
			if (names.get(i).isPlacementEligible()) 
				System.out.println(names.get(i).getName() + " is eligible for placement drive");
		}
		
		double tCgpa = 0.0;
		
		for (int i = 0; i < 5; i++) {
			tCgpa = Math.max(tCgpa, names.get(i).getCgpa());
		}
		
		System.out.println("Highest cgpa is scored is " + tCgpa);
		
		
	}
}

```

Student.java
```java
package firstStepsOfJava;

public class Student {
	int id;
	String name, branch;
	double cgpa;
	int age;
	
	Student(int id, String name, String branch, double cgpa, int age) {
		this.id = id;
		this.name = name;
		this.branch = branch;
		this.cgpa = cgpa;
		this.age = age;
	}
	
	void displayDetails() {
		System.out.println("ID: "+id);
		System.out.println("Name: "+name);
		System.out.println("Branch: "+branch);
		System.out.println("CGPA: "+cgpa);
		System.out.println("Age: "+age);
		System.out.println();
	}
	
	boolean isPlacementEligible() {
		return cgpa >= 7;
	}
	
	void updateCGPA(double newcgpa) {
		cgpa = newcgpa;
	}
	
	String getName() {
		return name;
	}
	
	double getCgpa() {
		return cgpa;
	}
}
```

Output
```
ID: 101
Name: Arjun
Branch: CSE
CGPA: 6.94
Age: 22

ID: 102
Name: Rahul
Branch: EE
CGPA: 7.82
Age: 24

ID: 103
Name: Sneha
Branch: ECE
CGPA: 8.42
Age: 21

ID: 104
Name: Priya
Branch: CSE
CGPA: 6.18
Age: 22

ID: 105
Name: Kiran
Branch: CSE
CGPA: 7.72
Age: 23

Rahul is eligible for placement drive
Sneha is eligible for placement drive
Kiran is eligible for placement drive
Highest cgpa is scored is 8.42
```

**Overload Constructors**
name + arguments = New Signature

the function with same name and many different arguments is different.

toString() method is combinations of all values in it.
Can create a function toString implicitly
car.toString() or explicitly car
<img width="774" height="410" alt="image" src="https://github.com/user-attachments/assets/080035e7-a343-49ae-a72f-5842cddddb91" />
<img width="997" height="446" alt="image" src="https://github.com/user-attachments/assets/c342fdbc-b5ad-405f-974d-e9da565a5609" />

```
ArrayList<Student> names = new ArrayList<>(); // this is Dynamic array

Student[] names = new Student[3]; // 3 items of Student is used.
```

It is the reperesentation of arraylist of objects where Student is class.

We don't need a getName and getCgpa, those are trivial can be writen neatly as obj1.name or obj1.cgpa as these are basic data initialised.

### Static Modifier
When used static modifier in datatypes in class, these are inheritly shared through all objects that get created.
ex: static int noOfFriends;

_Bonus point_: You can use Class not only object to call this static part, either incorparated in function that uses static variables or direct .static datatype

### Inheritance in Java
Inheriting variables and methods from parent class and also creating new inside the chold class.
The values of car in first line is child and right side is parent
```java
public class car extends vehicle {}
public class ford extends car {}
```

Creating a function of same name in chld class get superior priority in executing.
Which is called Method Overriding.

You can use _@override_ keyword for best practice, but it execute anyway.

### super keyword
The way to call the parent function. Where inherited variables and methods from it.
Most relatable case is using this.name = name, Instance of name is initialised in parent class, we need to call super(name) and add this.name = name there itself.

**Abstract Class**
An abstract class can't be used to create objects out of it.

But can initialize the abstract methods without completing implemntation, which can be used by subclasses of it.
where you can create a object of subclass

It is mandatory to fill the abstract methods of parent class, otherwise you will get error.

```java
public abstract class Vehicle {
	void tagline() {
		System.out.println("Made with love");
	}
	
	abstract void go(); // abstract methods are not implemented
}
```

```java
public class Car extends Vehicle{
	void go() {
		System.out.println("This car is moving!!");
	}
}
```

```java
public class Truck extends Vehicle {
	void go() {
		System.out.println("This Truck is moving!!");
	}
}

```

**Packages in Java?**

A package is just a way to organize related Java classes together — like folders.

```java
package animals;

public class Dog {
}
```

Here, Dog belongs to package animals.

You usually create packages to:
- organize code
- avoid name conflicts
- control access between classes

**Modifiers** comparision
| Modifier | Same Class | Same Package | Subclass (Different Package) | Different Package Non-Subclass |
|---|---|---|---|---|
| `private` | ✅ | ❌ | ❌ | ❌ |
| no modifier (default) | ✅ | ✅ | ❌ | ❌ |
| `protected` | ✅ | ✅ | ✅ | ❌ |
| `public` | ✅ | ✅ | ✅ | ✅ |

**_Imp:_** No modifier doesn't allow sub/child class from another package to access variable.

## Encapsulation
Attributes of class will be hidden or private. Can be accessed only through special methods like getter or setters ex: setAge(), getScore() etc
You should make attributes private if you don't have a good reason to make them public.

### Copy objects
car2 = car1, will assign same adress to car2

Instead create a method of car2.copy(car1) and put that menthod in Car() Overloaded constructor

Car car2 = new Car(car1);

It assigns the values of car1 to car2 completely.

### Interface vs abstract class
interface is hard coded rules with all methods with initialisation but no implemntation.

so every class inheritedf rom this must implemnt those methods.

abstract classcan have soem mehthod no abstract with implementation.

use _implements_ instead _extends_ for subclass of interface classes

### Polymorphism
The ability of object to identify as more than one type.

Finding that common class and use that to create Array and use common method go()

<img width="605" height="272" alt="image" src="https://github.com/user-attachments/assets/946a2c3b-7666-48da-8b26-ae0416f497c8" />

**Compile time polymorphism** is same as Overloading methods, same function name with different no of arguments.

**Run time Polymorphism** is overriding methods, also called **dynamic polymorphism.**
Ex: Use a scanner depends on user choice to select @Override method of child1 or child2, both which extends from parent class.
Where child1 and child2 has same function. speak() for dog is _Bark_ , speak() for car is _Meow_

It will create a Animal object that only trust in methods of only Animal, and the methods that Dog override and nothing else.

```java
public class Animal {
	void breathes() {
	}

	walks() {}
}
 public class dog extends Animal {
	// something
	void breathes() {
	}

	barks() {}
}
```
Animal a = new Dog();

walks(), breathes() of Dog class, barks() is not identified and won't work.

### Try Catch exception
```java
import java.util.InputMismatchException;
import java.util.Scanner;

public class Main {
	public static void main(String[] args) {
		
		try {
		Scanner scanner = new Scanner(System.in);
		
		System.out.println("Enter the number to divide: ");
		int a = scanner.nextInt();
		
		System.out.println("Enter the number to divide by: ");
		int b = scanner.nextInt();
		
		double z = (double)a/b;
		
		System.out.println("Your quotient is " + z); // If I write a string in place of number input i get, InputMismatchException
		}
		catch(InputMismatchException e) {
			System.out.println("Enter a number, you idiot");
		}
	}
}
```
```java
If you want to club all exceptions into single things.
catch(Exception e) { // This will take care of it
	System.out.println("Something went wrong";
}
finally {
	System.out.println("This will pront anyway");
	scanner.close(); // This is good practice
}
```

**Basic File handling**
```java
File file1 = new File("secret.txt"); // if file exists in same project folder, then relative directly si enough
File file2 = new File("C:Users/VARDHAN/OneDrive/Desktop/anj_id.pdf");
	
if (file1.exists()) System.out.println("File exists");
else System.out.println("Not exists");

System.out.println(file2.getAbsolutePath());
System.out.println(file2.getPath());
file1.delete();
```

**FileWriter() and FileReader()**
```java
try {
			FileWriter writer = new FileWriter("poem.txt");
			
			writer.write("Whta the hell is this \nWas said by a reader\n");
			writer.append("\nWritten by Vishnu");
			writer.close();
		} catch (IOException e) {
			// TODO Auto-generated catch block
			e.printStackTrace();
		}
		
		try {
			FileReader reader = new FileReader("art.txt");
			int data = reader.read(); // reads in ascii value, when it ends it will be -1
			
			while (data!= -1) {
				System.out.print((char)data);
				data = reader.read(); // type cast into char before printing
			}
		} catch (IOException e) {
			// TODO Auto-generated catch block
			e.printStackTrace();
		}
```

```
  ,_-~~~-,    _-~~-_
 /        ^-_/      \_    _-~-.
|      /\  ,          `-_/     \
|   /~^\ '/  /~\  /~\   / \_    \
 \_/    }/  /        \  \ ,_\    }
        Y  /  /~  /~  |  Y   \   |
       /   | {Q) {Q)  |  |    \_/
       |   \  _===_  /   |
       /  >--{     }--<  \
     /~       \_._/       ~\
    /    *  *   Y    *      \
    |      * .: | :.*  *    |
    \    )--__==#==__--     /
     \_      \  \  \      ,/
       '~_    | |  }   ,~'
          \   {___/   /
           \   ~~~   /
           /\._._._./\
          {    ^^^    }
           ~-_______-~
            /       \
```

**Audio Player using Java**
(To be filled)
How to play and much more

**JFrame**
(To be filled)
A Code of Java native, GUI(Graphical User Interface)
Which application run like a piant app, that we can change colors of it, size and behaviour on click.
Mainly event driven programming interface.


**JLabel**
(To be filled)
he text like string in JFrames

**JPanel**
A component that functions as a container to hold other components

**JButton**

# Leetcode using Java
Unordered Map(C++) is same as HashMap in Java

Two sum using _HashMap_ in Java
```java
class Solution {
    public int[] twoSum(int[] nums, int target) {
        HashMap<Integer, Integer> mpp = new HashMap<>();

        for (int i = 0; i < nums.length; i++) {
            if (mpp.containsKey(nums[i])) {
                return new int[]{i, mpp.get(nums[i])};
            } else {
                mpp.put(target-nums[i], i);
            }
        }
        return new int[]{};
    }
}
```

## Java Collection Framework
Same as stl in c++
