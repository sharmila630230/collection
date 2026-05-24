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
