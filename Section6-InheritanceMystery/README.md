# Section 6 - Inheritance Mystery 

## Introduction 
The goal of today's section is to become more familiar with inheritance. 
The task is to work through a series of method calls on objects that are 
created from classes using inheritance. Additionally, you will answer 
several theoretical questions at the end to check your understanding of 
inheritance. If you get stuck, work with a neighbor, refer to the class 
slides from the Inheritance lectures or talk with your SL. 

## Assignment
You will be stepping through function calls on objects from the Classes 
One, Two, Three, and Four. Do NOT assume they inherit from one another in 
numerical order. Look at what objects are created and what methods exist 
in those classes to answer the method call questions. You can write your 
answers to the questions in a basic text file in Eclipse or any text editor 
of your choice or you can write the answers down on a sheet of paper. Once
you have completed all questions, show them to your SL.  

Look over the following classes and answer the questions below. 

```
public class One extends Two {
	
	public void name() {
		super.name();
		System.out.println("Cero");
	}
	
	public void twice() {
		super.twice();
		name(); 
	}

}

```
```

public class Two extends Four {
	
	public void twice() {
		super.twice(); 
		System.out.println("Two Two");
	}
	
	public void thrice() {
		System.out.println("Tres Tres");
	}
}

```
```


public class Three extends Two {

	public void thrice() {
		super.twice(); 
		System.out.println("Trois Tres Three");
	}
	
	public void once() {
		super.once();
		System.out.println("Once");
		super.once();
	}

}

```
```

public class Four {
	public void once() {
		System.out.println("Uno");
	}
	public void twice() {
		once(); 
		System.out.println("Deux Deux");
	}
	public void name() {
		System.out.println("Quatre");
	}
}

```
### Method Call Questions: 

#### Q1 
Create a Two object and call twice. 

```

		Two two = new Two(); 
		two.twice(); 

```

#### Q2
Create a One object and call twice. 

```

		Two two = new One(); 
		two.twice(); 

```

#### Q3 
Create a Three object and call name. 

```
		Three three = new Three(); 
		three.name();
```

#### Q4 
On the same Three object call thrice. 

```
		three.thrice();
```


### Review Questions:

#### Q5 

```
Which class is at the top of the inheritance hierarchy? 
```

#### Q6 

```
Imagine the twice method in the One class did not call name() and appeared as the code below. 

	public void twice() {
		super.twice();
		name(); 
	}

Why would this version of twice() be poor decomposition? 
```

#### Q7 

```
7) Can Two's thrice method call super.thrice()? Why or why not? 
```


