# Library-System
# Generic Library System (Java CLI)

This is a simple, console-based Java application that simulates a library catalog system. The system allows users to add, remove, and view library items such as books, DVDs, or magazines. It uses Java generics to make the system reusable for any type of item ID (e.g., `Integer`, `String`, `UUID`, etc.).

## Features

- Add new library items
- Remove items by ID
- View the full catalog
- Uses Java Generics to support multiple item ID types
- Console-based interactive menu

## Class Overview

### LibraryItem<T>
A generic class that represents a library item.

**Attributes:**
- `String title`
- `String author`
- `T itemID` – the unique identifier for the item (can be any type)

**Methods:**
- Constructor to initialize all fields
- Getters: `getTitle()`, `getAuthor()`, `getItemID()`
- `toString()` – returns a human-readable description of the item

### LibraryCatalog<T>
A generic class that manages a list of `LibraryItem<T>`.

**Methods:**
- `void addItem(LibraryItem<T> item)` – adds an item to the catalog
- `void removeItem(T itemID)` – removes an item by matching its ID
- `void displayCatalog()` – prints all items in the catalog

### LibrarySystem (Main Class)
Contains the `main()` method and provides a command-line interface for interacting with the system.

**Features:**
- Menu-driven interface with options:
  1. Add item  
  2. Remove item  
  3. View catalog  
  4. Exit  
- Uses `Scanner` for user input
- Demonstrates use of generics with `Integer` item IDs

## How to Run

1. Ensure you have Java 8 or higher installed.
2. Compile all classes in the `librarysystem` package:

   ```bash
   javac librarysystem/LibrarySystem.java

