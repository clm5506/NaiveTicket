# NaiveTicket

The second Objects lab, from the BlueJ book's second chapter.

Look for the [Chapter 2 file](./doc/BlueJ-objects-first-ch2.pdf) you need in the [doc](./doc) folder.
There is 35 pages of reading and exercises in the chapter.

Work through all these exercises. You edit this file with your answers for these exercises.

### Exercise 2.1
* Create a TicketMachine object on the object bench. 
	CM - Created my TicketMachine with price of tickets = 10
* Upon viewing its methods, `getBalance`, `getPrice`, `insertMoney`, `printTicket`.
* Use `getPrice` method to view the value of the price of the tickets that was set when this object was created. 
	CM - Price is = to 10
* Use `insertMoney` method to simulate inserting an amount of money into the machine.
	CM - Inserted money with amount of 20
* Use `getBalance` to check that the machine has a record of the amount inserted.
	CM - getBalance returns 20
	* You can insert several separate amounts of money into the machine, just like you might insert multiple coins or notes into a real machine. Try inserting the exact amount required for a ticket. As this is a simple machine, a ticket will not be issued automatically, so once you have inserted enough money, call the `printTicket` method. A facsimile ticket should be printed in the BlueJ terminal window.
	CM -Called printTicket() and the below output was returned:
	
##################
# The BlueJ Line
# Ticket
# 10 cents.
##################

### Exercise 2.2
* What value is returned if you check the machine’s balance after it has printed a ticket?
	CM - getBalance() returns 0

### Exercise 2.3
* Experiment with inserting different amounts of money before printing tickets.
	* Do you notice anything strange about the machine’s behavior?
		CM - Yes...
	* What happens if you insert too much money into the machine – do you receive any refund?
		CM - NO balance sets to zero even if the amount you inserted is greater than the price of tickets
	* What happens if you do not insert enough and then try to print a ticket?
		CM - Ticket still prints if you have not inserted enough money
		

### Exercise 2.4
* Try to obtain a good understanding of a ticket machine’s behavior by interacting with it on the object bench before we start looking at how the `TicketMachine` class is implemented in the next section.

### Exercise 2.5
* Create another ticket machine for tickets of a different price.
		CM - Price is set to 33
	* Buy a ticket from that machine.
	* Does the printed ticket look different?
		CM - Yes output below is returned
		
##################
# The BlueJ Line
# Ticket
# 33 cents.
##################

### Exercise 2.6
* Write out what you think the outer wrappers of the `Student` and `LabClass` classes might look like – do not worry about the inner part.
	CM - 
	     public class Student {
	}
	     public class LabClass {
	}     

### Exercise 2.7
Does it matter whether we write<br>
`public class TicketMachine`<br>
or<br>
`class public TicketMachine`<br>
in the outer wrapper of a class?

* Edit the source of the `TicketMachine` class to make the change and then close the editor window.
	* Do you notice a change in the class diagram? CM - Yes
	* What error message do you get when you now press the compile button? CM - invalid method declaration; return type 		expected
	* Do you think this message clearly explains what is wrong? CM - Nope

### Exercise 2.8
* Check whether or not it is possible to leave out the word `public` from the outer wrapper of the `TicketMachine` class.
	CM - Yes it's possible

### Exercise 2.9
* From your earlier experimentation with the ticket machine objects within BlueJ you can probably remember the names of some of the methods – `printTicket`, for instance.
	* Look at the class definition in Code 2.1 and use this knowledge, along with the additional information about ordering we have given you, to try to make a list of the names of the fields, constructors, and methods in the `TicketMachine` class. CM - Fields: price, balance, total
	  - Constructor:
	
	public TicketMachine(int ticketCost)
   	 {
        price = ticketCost;
        balance = 0;
        total = 0;
   	 }
    	Methods: getPrice(), getBalance(), insertMoney(), printTicket(), 
	 
	* Hint: There is only one constructor in the class.

### Exercise 2.10
* Do you notice any features of the constructor that make it significantly different from the other methods of the class?
	CM - First letter of the contructor is capitalized and doesn't specify whether or not something should be returned by 	      the method

### Exercise 2.11
* What do you think is the type of each of the following fields?

```java
private int count; CM - the type is int
private Student representative; CM - the type is Student
private Server host; CM - the type is Server
```

### Exercise 2.12
* What are the names of the following fields?

```java
private boolean alive; CM - the name is alive
private Person tutor; CM - the name is tutor
private Game game; CM - the name is game
```
### Exercise 2.13

In the following field declaration from the TicketMachine class<br>

```java
private int price;
```
does it matter which order the three words appear in? CM - YES
* Edit the `TicketMachine` class to try different orderings. After each change, close the editor.
	* Does the appearance of the class diagram after each change give you a clue as to whether or not other orderings are
possible? CM - Yes 
	* Check by pressing the compile button to see if there is an error message. CM - <identifier> expected, illegal start of type error is received
	* Make sure that you reinstantiate the original version after your experiments!

### Exercise 2.14
* Is it always necessary to have a semicolon at the end of a field declaration? CM - YES, '; expected' error 
* Once again, experiment via the editor.
* The rule you will learn here is an important one, so be sure to remember it.


### Exercise 2.15
* Write in full the declaration for a field of type `int` whose name is `status`. CM - declared private int status; in editor

### Exercise 2.16
* To what class does the following constructor belong? CM - Student
```
public Student(String name)
```

### Exercise 2.17
* How many parameters does the following constructor have and what are their types?
```
public Book(String title, double price) CM - 2 parameters of types String and double respectively
```

### Exercise 2.18
* Can you guess what types some of the `Book` class’s fields might be? CM - int, object, String
* Can you assume anything about the names of its fields? CM - no

Work all Exercises from 2.19 to 2.58 that are **NOT** marked *Challenge exercise*.
READ upto and INCLUDING section 2.15 of this chapter.

### Exercise 2.19
public Pet(String petsName) {
	String myPetsName = petsName;
}

### Exercise 2.21 Compare the getBalance method with the getPrice method. What are the differences between them?
	      They return different values
### Exercise 2.22 If a call to getPrice can be characterized as ‘What do tickets cost?’, how would you characterize a call to getBalance? 
	      The amount of money already inserted for the next ticket
	      
### Exercise 2.23 If the name of getBalance is changed to getAmount, does the return statement in the body of the method need to be changed, too? Try it out within BlueJ.
		NO it doesn't need to be changed, but it should be to be clear to people reading the code
		
### Exercise 2.24 Define an accessor method, getTotal, that returns the value of the total field.
		    public int getTotal()
    {
        return total;
    }
    
### Exercise 2.25 Try removing the return statement from the body of getPrice. What error message do you see now when you try compiling the class?
	Error states "missing return type"
	
### Exercise 2.26 Compare the method signatures of getPrice and printTicket in Code 2.1. Apart from their names, what is the main difference between them?
	getPrice expects a int return value and printTicket doesn't return anything;
	
### Exercise 2.27 Do the insertMoney and printTicket methods have return statements? Why do you think this might be? Do you notice anything about their headers that might suggest why they do not require return statements?
	No they do not return anything because they are not called to retrieve data from the class like accessor methods. They are mutator methods. They change state. They both have void in their method signatures.
	
### Exercise 2.28 Create a ticket machine with a ticket price of your choosing. Before doing anything else, call the getBalance method on it. Now call the insertMoney method (Code 2.6) and give a non-zero positive amount of money as the actual parameter. Now call getBalance again. The two calls to getBalance should show different output because the call to insertMoney had the effect of changing the machine’s state via its balance field. 
	Balance started out at zero that increased to the amount I sent when I called the insertMoney method.

### Exercise 2.29 How can we tell from just its header that setPrice is a method and not a constructor?
public void setPrice(int ticketCost)
	The method specifies void return type, setPrice is lower case.
		
### Exercise 2.30 Complete the body of the setPrice method so that it assigns the
value of its parameter to the price field.

	public void setPrice(int ticketCost){
		this.price = ticketCost;
	}

### Exercise 2.31 Complete the body of the following method, whose purpose is to
add the value of its parameter to a field named score.
  /**
   * Increase score by the given number of points.
   */
  public void increase(int points)
  {
  	score = score + points;
... }

### Exercise 2.32 Can you complete the following method, whose purpose is to sub- tract the value of its parameter from a field named price?
  /**
   * Reduce price by the given amount.
   */
  public void discount(int amount)
  {
  price = price - amount;
... }

### Exercise 2.33 Add a method called prompt to the TicketMachine class. This should have a void return type and take no parameters. The body of the method should print something like:
  Please insert the correct amount of money.
  
    public void prompt() {
    System.out.println("Please input the correct amount of money");
    }
    
### Exercise 2.34 Add a showPrice method to the TicketMachine class. This should have a void return type and take no parameters. The body of the method should print something like:
The price of a ticket is xyz cents.
where xyz should be replaced by the value held in the price field when the method
is called.

    public void showPrice() {
     System.out.println("The price of a ticket is " + price + " cents");   
    }
    
### Exercise 2.35 Create two ticket machines with differently priced tickets. Do calls to their showPrice methods show the same output, or different? How do you explain this effect?
	The out put is different because we defined different prices when constructing our objects.
	
### Exercise 2.36 What do you think would be printed if you altered the fourth state- ment of printTicket so that price also has quotes around it, as follows?
  System.out.println("# " + "price" + " cents.");
  	It would concatenate the 3 strings in the output instead of printing the value of price.
		
### Exercise 2.37 What about the following version? System.out.println("# price cents.");
	It would print # price cents. all on one line\\Exercise 2.38 Could either of the previous two versions be used to show the price of tickets in different ticket machines? Explain your answer.
	No because we aren't using the variable price in the output we're just printing the word price.

### Exercise 2.39 Modify the constructor of TicketMachine so that it no longer has a parameter. Instead, the price of tickets should be fixed at 1000 cents. What effect does this have when you construct ticket machine objects within BlueJ?

    public TicketMachine()
    {
        price = 1000;
        balance = 0;
        total = 0;
    }
    
    You are no longer prompted to provide the price of tickets within BlueJ when creating a new instance of TicketMachine.
    
### Exercise 2.40 Implement a method, empty, that simulates the effect of removing all money from the machine. This method should have a void return type, and its body should simply set the total field to zero. Does this method need to take any parameters? Test your method by creating a machine, inserting some money, printing some tickets, checking the total, and then emptying the machine. Is this method a mutator or an accessor?
 
     public void empty() {
        total = 0;
    }
    
    No it doesn't need to take any parameters because you want the value to be 0 not a value that is passed in. It is a mutator method.
    
### Exercise 2.41 Implement a method, setPrice, that is able to set the price of tickets to a new value. The new price is passed in as a parameter value to the method. Test your method by creating a machine, showing the price of tickets, changing the price, and then showing the new price. Is this method a mutator?
    
        public void setPrice(int ticketCost){
		this.price = ticketCost;
    }
    This is a mutator method
    
### Exercise 2.42 Give the class two constructors. One should take a single parame- ter that specifies the price, and the other should take no parameter and set the price to be a default value of your choosing. Test your implementation by creating machines via the two different constructors.

    public TicketMachine()
    {
        price = 1000;
        balance = 0;
        total = 0;
    }
    
    public TicketMachine(int priceSentInMethodCall) {
        this.price = priceSentInMethodCall;
    }
    
### Exercise 2.43 Check that the behavior we have discussed here is accurate by creating a TicketMachine instance and calling insertMoney with various actual parameter values. Check the balance both before and after calling insertMoney. Does the balance ever change in the cases when an error message is printed? Try to predict what will happen if you enter the value zero as the parameter, and then see if you are right.
    
	If I insert zero dollars, then I receive the error prompting me to use a positive number. The balance is not updated when calling insertMoney with a value < 0.
	
### Exercise 2.44 Predict what you think will happen if you change the test in insertMoney to use the greater-than or equal-to operator:
  if(amount >= 0)
Check your predictions by running some tests. What difference does it make to the behavior of the method?

	I predict that change the = to >= will allow the insertMoney method to be called with 0 as the amount and no error will be displayed to the user.
	
	The results match my prediction
	
### Exercise 2.45 In the shapes project we looked at in Chapter 1 we used a boolean field to control a feature of the circle objects. What was that feature? Was it well suited to being controlled by a type with only two different values?

	The boolean field was isVisible. Boolean was acceptable because there are only 2 options: visible and invisible.
	

### Exercise 2.46 In this version of printTicket we also do something slightly different with the total and balance fields. Compare the implementation of the method in Code 2.1 with that in Code 2.8 to see whether you can tell what those differences are. Then check your understanding by experimenting within BlueJ.


	2.1 code sets balance to 0 after printTicket is called and balance is added to total.
	2.8 code sets balance = to balance - price and price, instead of balance, is added to total.
	
Exercise 2.47 After a ticket has been printed, could the value in the balance field ever be set to a negative value by subtracting price from it? Justify your answer.
	
	No, because balance has to be > or = to price before entering the loop that reduces balance by price.
	
### Exercise 2.48 Sofarwehaveintroducedyoutotwoarithmeticoperators,+and–, that can be used in arithmetic expressions in Java. Take a look at Appendix D to find out what other operators are available.

### Exercise 2.49 Write an assignment statement that will store the result of multiply- ing two variables, price and discount, into a third variable, saving.

	int saving = price * discount;

Exercise 2.50 Write an assignment statement that will divide the value in total by the value in count and store the result in mean. 

	int mean = total / count;


### Exercise 2.51 Write an if statement that will compare the value in price against the value in budget. If price is greater than budget then print the message ‘Too expensive’, otherwise print the message ‘Just right’.
	
	if( price > budget) {
		System.out.println("Too expensive");
	} else {
		System.out.println("Just right");
	}

### Exercise 2.52 Modify your answer to the previous exercise so that the message if the price is too high includes the value of your budget.

	if( price > budget) {
		System.out.println( price + "is Too expensive");
	} else {
		System.out.println("Just right");
	}
	
### Exercise 2.53 Why does the following version of refundBalance not give the same results as the original?
  public int refundBalance()
  {
balance = 0;
      return balance;
  }
  
  The original refundBalance returns amountToRefund.
  
What tests can you run to demonstrate that it does not? Test what balance value is returned when balance is greater than price.

### Exercise 2.54 What happens if you try to compile the Ticket Machine class with the following version of refundBalance?
  public int refundBalance()
  {
      return balance;
balance = 0; }

You will get an error

What do you know about return statements that helps to explain why this version does not compile?

Return statement needs to be the last line in the method bc it will be the last to be executed and so any line of code beneath the return statement will be considered unreachable.

### Exercise 2.55 Add a new method, emptyMachine, that is designed to simulate emptying the machine of money. It should both return the value in total and reset total to be zero.

    public int emptyMachine() {
        total = 0;
        return total;
    }
    
### Exercise 2.56 Is emptyMachine an accessor, a mutator, or both?
 
 	emptyMachine is a mutator method because change the state of a variable.
	
### Exercise 2.57 Rewrite the printTicket method so that it declares a local variable, amountLeftToPay. This should then be initialized to contain the difference between price and balance. Rewrite the test in the conditional statement to check the value of amountLeftToPay. If its value is less than or equal to zero, a ticket should be printed, otherwise an error message should be printed stating the amount still required. Test your version to ensure that it behaves in exactly the same way as the original version.

    public void printTicket()
    {
        
        int amountLeftToPay = price - balance;
        
        if(amountLeftToPay <= 0) {
            // Simulate the printing of a ticket.
            System.out.println("##################");
            System.out.println("# The BlueJ Line");
            System.out.println("# Ticket");
            System.out.println("# " + price + " cents.");
            System.out.println("##################");
            System.out.println();

            // Update the total collected with the price.
            total = total + price;
            // Reduce the balance by the prince.
            balance = balance - price;
        }
        else {
            System.out.println("You must insert at least: " +
                               (price - balance) + " more cents.");
                    
        }
    }
