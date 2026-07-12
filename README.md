# Employee Data Processor (Java Streams)

![Java](https://img.shields.io/badge/java-%23ED8B00.svg?style=for-the-badge&logo=openjdk&logoColor=white)
![Stream API](https://img.shields.io/badge/Stream_API-Functional_Programming-blue?style=for-the-badge)

A pure Java application focused on **Functional Programming**, **Lambda Expressions**, and the **Stream API**. This project reads employee data from a CSV file and dynamically processes the information to extract specific insights using modern Java declarative programming techniques.

> This project was developed as a practice exercise for the "Java and Object-Oriented Programming" course by DevSuperior (Prof. Dr. Nelio Alves), aiming to consolidate knowledge on functional paradigms introduced in Java 8.

---

## Technologies & Concepts

* **Java 8+:** Core language.
* **Stream API:** Extensive use of data pipelines (`stream()`, `filter()`, `map()`, `sorted()`, `reduce()`, `toList()`).
* **Lambda Expressions:** Arrow functions (`->`) for concise anonymous method implementations.
* **File Handling:** Robust reading of `.csv` or `.txt` files using `BufferedReader` and `FileReader` with `try-with-resources`.
* **Exception Handling:** Graceful handling of `IOException` for file reading failures.

---

## Business Rules (Pipeline Logic)

The system performs the following operations sequentially based on a user-defined salary threshold:

1. **Filtering & Sorting:** Filters employees whose salary is greater than the provided input, extracts only their emails, sorts them in alphabetical order, and collects them into a new `List`.
2. **Mapping & Reducing:** Filters employees whose names start with the letter 'M', extracts only their salaries, and reduces (sums) them into a single total value.

---

## Execution Example

Here is a practical example of how the application behaves in the console:

### Input File (`in.txt`):
```csv
Maria,maria@gmail.com,3200.00
Alex,alex@gmail.com,1900.00
Marco,marco@gmail.com,1700.00
Bob,bob@gmail.com,3500.00
Anna,anna@gmail.com,2800.00
```

## Console Output:
```csv
Enter file full path: c:\temp\in.txt
Enter salary: 2000.00
Email of people whose salary is more than 2000.00:
anna@gmail.com
bob@gmail.com
maria@gmail.com
Sum of salary of people whose name starts with 'M': 4900.00
