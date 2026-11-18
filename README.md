# OOP-MINI-PROJECT
# 📚 Library Management System

A simple, console-based **Library Management System** implemented in C++ as an Object-Oriented Programming (OOP) mini-project. This application allows users to manage a collection of books, track availability, and handle issuing and returning operations efficiently.

## 👤 Student Details
* **Name:** Husain Kaizar Husain Dadawala
* **URN:** E25B002817
* **Course:** Object-Oriented Programming (OOP) Mini-Project

---

## 👨🏻‍🏫 Faculty Details
* **Name:** Mr Dattatray Dudhamogre
* **Submitted on:** 19 November 2026
* **Rate my Project😀:** https://forms.gle/kPvz1WYPx7yH5iRF9

---

## ✨ Features
* **Add Books:** Register new books into the library system with unique IDs, titles, and authors (includes duplicate ID validation).
* **Display Catalog:** View a complete list of all available and issued books currently stored in the system.
* **Search Books:** Quickly find specific books using their unique Book ID.
* **Issue Books:** Check out available books by updating their status to "Issued".
* **Return Books:** Process book returns to restore their status back to "Available".
* **Interactive Menu:** Clean command-line user interface with loop-based navigation.

---

## 🛠️ OOP Concepts Demonstrated
This project applies core Object-Oriented Programming principles:
1. **Encapsulation:** Data hiding is implemented in both the `Book` and `Library` classes by keeping member variables (`id`, `title`, `author`, `isAvailable`, `books`) `private` and exposing controlled access via `public` getter and setter methods.
2. **Classes and Objects:** The system models real-world entities cleanly using distinct classes (`Book` as an individual item, and `Library` as the manager of the collection).
3. **Composition:** The `Library` class contains a `std::vector<Book>`, demonstrating a "has-a" relationship where the library manages multiple book instances.

---

## 🚀 Getting Started

### Prerequisites
You need a C++ compiler supporting C++11 or later (such as programiz).

### Compilation and Execution

1. **Copy Source Code From:**
   https://github.com/HussainKaizarHussain/OOP-MINI-PROJECT

2. **Paste it in compiler**

   https://www.programiz.com/cpp-programming/online-compiler/
