# Quiz

```
Part 1 - Quiz. Can't use internet for these questions. Or visual studio or ChatGpt. The main purpose for me is to work out the gaps in your knowledge so we can cover them.
1. What is SOLID. List all 5
	SOLID is an acronym detailing the five princliples one should follow when programming in an object oriented programming to ensure robust, maintainable, and understandable classes.
	S - Single responsiblity principle. A class should be responsible for one thing and one thing only. If a waiter class performs the responsibilities for a waiter but also for a chef, porter, police officer then that's a violation of the sinlge responsibility principle. 
	O - Open and closed principle. A class should be open for extention but closed for modification. Any extentions added to a class should not involve changing the base code.
	L - Liskovs's substitution principle. A parent class should be able yo be substituted by its child classes and expected to work.
	I - Interface segregation principle. A class shouldn't have to implement methods from interfaces that it will not be using. Multiple smaller, niche interfaces are better than one large interface. 
	D - Dependancy inversion principle. A class should extend only interfaces or abstract classes, not from concrete classes.
2. What is the difference between struct and class
	- A  struct is a lightweight class, it cannot extend other classes and it cannot have null fields.
3. List Data structures in c# e.g. List, 
	- ArrayList, Dictionary, Array,  
4. What is sealed, abstract and virtual keywords
	- An abstract class can contain both method signatures and have method implementations.  
5. What are the different access modifiers in c# (e.g. private). And what do they do 
		- Internal: Only accessible by things in the same file as it.
		- Private: Only accessible by things within the same class, children cannot access
		- Public: Accessible by things outside the class aswell as within.
		- Protected: Like private, but children can also access
6. What is the difference between "const", "static" and "static readonly" keywords
		- Const: once the variable has been initialised, its value cannot change. It is immutable
		- Static: is accessible by referencing the class itself and not an instance of the class (do not have to create an instance of the class and reference the instance). A static value is also shared throughout all the instances of the class.
		- Static readonly: Like static, but is immutable, like const
7. Write a line of code that throws an exception
		- throw new Exception("An error has occurred!");
8. When should you use stringbuilder 
9. What is the CLR - Common Language Runtime
10. Why are strings immutable
	 - For security reasons, we don't want passwords to be mutated before it reaches its destination. 
11. What is diff between GetType(), is and typeof()
		- Get type is a method that the class has to implement
		- typeof is a built-in C# method
12. How is a dictionary implemented
		- A dictionary stores its data using a key-pair value. A basic dictionary is made up of an array, a hashing function, and functions to add, retrieve, and delete an item. The hashing funciton takes an object (the key) and performs an operation on the key that returns an almost unique number that is within range of the array length. This number is used as the index of the array to perform an operation in. For example, the add method will take a key and value,    call the hashing function passing the key, and use the int returned as the index to store the value in.  
13. What is the Equals/hashcode contract. Aka why are the equals() and hashcode() important on every class and important in dictionary. 
	-  The equals method compares the hashcode, obtained from the hashcode method,  between the two compring objects to check if they are the same object. Changing the equals or hashcode implementation would break the contract. 
14. What happens when there is a collision in a dictionary
	- The dictionary would store an array in the index that has the collision and in there the collided key value pairs will be stored. The contents in the array will be searched using the standard loop, looking for the index that has the matching key.
15. What is a constructor. Write code for an example
	- A contructor is the method that is called when a class is instanciated. Code that setups up the class is run here (setting fields, properties). 
	- public MyClass(type arg 1, type arg2){ Console.WriteLine($"I have been constructed with {arg1} and {arg2} as my parameters")}
16. What is the difference between method overloading and overriding. Give an example of each 
	 - Overloading is having the same method name but different number or types of parameters
		 - public void DoSomething(type arg1, type arg2)
		 - public void DoSomething(type arg1, type arg2, type arg3)
	- Overriding is replacing the implementation of a method, typically inherited from a parent class
		- public void override DoSomething(type arg1, type arg2)
17. What is the main entry point of a c# application 
	- Through the public static void main(string[] args) method 
18. What is TDD? Explain the 3 steps in it. 
	- Test driven development is the methodology of first writing out tests before implementing. The steps to TDD is to write a test, write code that is meant to fail, then write code that passes the task, and then refactor.
	- It is easier to find the cause of bugs or to see if changes to the code caused anything to fail. 
19. Explain difference between ref and out keywords in C#
20. What is the output for executing the following code?
public class TestClass
{
    private string a = "Unchanged";
    
    private void TestMethod(string b)
    {
        var newString = "Changed in TestMethod";
        b = newString;
        Console.WriteLine(b);
    }
    
    public void RunTest()
    {
        TestMethod(a);
        Console.WriteLine(a);
    }
}
var test = new TestClass();
test.RunTest();

Output: 
"Changed in TestMethod
Unchanged"


```
