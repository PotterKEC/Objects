# Java Objects Introduction

This repository contains a practice activity for learning about Object-Oriented Programming in Java.

## What Are Objects?

In Java, objects are instances of classes. Think of a class as a blueprint for creating objects:
- A **class** defines the properties (attributes) and behaviors (methods) that objects of that type will have
- An **object** is a specific instance of a class with its own unique data

## How to Create a Class

```java
public class Book {
    // Properties (attributes)
    private String title;
    private String author;
    private int pageCount;
    
    // Constructor
    public Book(String title, String author, int pageCount) {
        this.title = title;
        this.author = author;
        this.pageCount = pageCount;
    }
    
    // Methods
    public void displayInfo() {
        System.out.println("Book: " + this.title + " by " + this.author + ", " + this.pageCount + " pages");
    }
    
    // Getters and Setters
    public String getTitle() {
        return this.title;
    }
    
    public void setTitle(String title) {
        this.title = title;
    }
    
    public String getAuthor() {
        return this.author;
    }
    
    public void setAuthor(String author) {
        this.author = author;
    }
    
    public int getPageCount() {
        return this.pageCount;
    }
    
    public void setPageCount(int pageCount) {
        this.pageCount = pageCount;
    }
}
```

## How to Create an Object

Once you have defined a class, you can create objects of that class:

```java
public class Main {
    public static void main(String[] args) {
        // Create a new Book object
        Book harryPotter = new Book("Harry Potter", "J.K. Rowling", 400);
        
        // Use the object's methods
        harryPotter.displayInfo();
        
        // Access properties using getters
        System.out.println("Title: " + harryPotter.getTitle());
        
        // Modify properties using setters
        harryPotter.setPageCount(423);
        System.out.println("Updated page count: " + harryPotter.getPageCount());
    }
}
```

## Your Assignment: Create an Enemy Class

For this assignment, you will create an `Enemy` class for a video game.

### Requirements:

1. Create an `Enemy` class with the following private properties:
   - `name` (String)
   - `health` (int)
   - `damage` (int)
   - `speed` (double)

2. Create a constructor that accepts values for all properties

3. Create getter and setter methods for all properties

4. Add the following methods:
   - `displayInfo()` - prints all enemy information
   - `attack()` - returns the damage value and prints a message about attacking
   - `takeDamage(int amount)` - reduces health by the amount and returns remaining health
   - `isDefeated()` - returns true if health <= 0, false otherwise

5. In your `Main` class, create at least two different Enemy objects and demonstrate using all of their methods

### Example Output:

```
Enemy: Goblin
Health: 50
Damage: 10
Speed: 2.5
The Goblin attacks for 10 damage!
Goblin took 20 damage, 30 health remaining.

Enemy: Dragon
Health: 200
Damage: 40
Speed: 1.0
The Dragon attacks for 40 damage!
Dragon took 50 damage, 150 health remaining.
```

## Folder Structure

```
project-root/
├── src/
│   ├── Book.java
│   ├── Enemy.java
│   └── Main.java
└── README.md
```


Good luck!