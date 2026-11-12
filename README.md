# OOP-MINI-PROJECT
Library Management System (C++ Mini Project)

A console-based Library Management System built in C++ for Practical 12 (Option A). This project demonstrates core Object-Oriented Programming (OOP) principles, Standard Template Library (STL) containers, custom exception handling, and persistent CSV file storage.

Problem Statement & Users

Target Users: Librarians and library staff.

Problem Solved: Automates manual book tracking by providing a persistent, error-safe system to add books, search the catalog, and track book availability (issued vs. available).

Key Features

Object-Oriented Design: Encapsulates book properties in a Book class and library management operations in a Library class, utilizing function overloading for searching by ID or keyword.

STL Integration: Uses std::vector and <algorithm> (std::find_if) for efficient in-memory record management.

Persistent Storage (File I/O): Automatically loads records from books.csv at startup and saves updates immediately using std::ifstream and std::ofstream.

Exception Handling: Implements a custom LibraryException class (derived from std::runtime_error) to safely handle duplicate IDs, non-existent books, unavailable books, and file errors.

UML Class Diagram

+-------------------------------------------------------+
|                         Book                          |
+-------------------------------------------------------+
| - bookID : int                                        |
| - title : std::string                                 |
| - author : std::string                                |
| - isAvailable : bool                                  |
+-------------------------------------------------------+
| + Book(id: int, t: string, a: string, avail: bool)    |
| + getBookID() : int                                   |
| + getTitle() : std::string                            |
| + getAuthor() : std::string                           |
| + getAvailability() : bool                            |
| + setAvailability(status: bool) : void                |
| + display() : void                                    |
| + toCSV() : std::string                               |
| + fromCSV(csvLine: std::string) : Book (static)       |
+-------------------------------------------------------+
                           | 1
                           | manages *
                           v
+-------------------------------------------------------+
|                        Library                        |
+-------------------------------------------------------+
| - books : std::vector<Book>                           |
| - filename : std::string                              |
+-------------------------------------------------------+
| + Library(csvFilename: std::string)                   |
| + addBook(id: int, title: string, author: string)     |
| + searchBook(id: int) : void                          |
| + searchBook(keyword: std::string) : void             |
| + displayAllBooks() : void                            |
| + issueBook(id: int) : void                           |
| + returnBook(id: int) : void                          |
| + loadFromFile() : void                               |
| + saveToFile() : void                                 |
+-------------------------------------------------------+
                           | throws
                           v
+-------------------------------------------------------+
|                   LibraryException                    |
|             (extends std::runtime_error)              |
+-------------------------------------------------------+
| + LibraryException(message: std::string)              |
+-------------------------------------------------------+


Compilation & Execution

Compile the code using a C++11 (or newer) compiler:

g++ -std=c++11 library_management.cpp -o library_system


Run the executable:

On Linux/macOS:

./library_system


On Windows:

library_system.exe
