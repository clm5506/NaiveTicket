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
public Book(String title, double price)
```

### Exercise 2.18
* Can you guess what types some of the `Book` class’s fields might be?
* Can you assume anything about the names of its fields?

Work all Exercises from 2.19 to 2.58 that are **NOT** marked *Challenge exercise*.
READ upto and INCLUDING section 2.15 of this chapter.
