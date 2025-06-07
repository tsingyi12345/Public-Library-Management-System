# Library Management System 
Database Project
This project is a Library Management System that provides both a librarian interface for managing the library inventory and a user interface for searching, checking in and checking out books.

Features:

Librarian Interface: Add, remove, and search for books in the library inventory. Generate reports of books borrowed and books available in the inventory.

User Interface: Search for books based on title, author, genre, release year, or other criteria. Check-in and check-out books if they are available in the inventory.

Database Management: All data is stored in a local MySQL server for efficient data management and retrieval. (CRUD) Optional Additional Features:

User profiles for tracking individual preferences and borrowing history. Book recommendation system based on user preferences and borrowing patterns. Enhanced book search capabilities allowing users to find books by various criteria such as author, genre, release year, etc. How to Run:

Clone this repository. Set up a local MySQL server and configure the database connection in the code. Run python main.py to start the Library Management System.

---

## 📘 Additional README: Differences Between Notebook Versions

This section explains the differences between the two versions of the notebook `PublicLibraryProject_With_Pandas.ipynb` used in the **Library Management System** project.

### 🔄 Comparison Overview

| Feature/Section | Old Version | New Version |
|----------------|-------------|-------------|
| **Data Handling** | Basic data loading and display via `pandas.read_csv` | Improved data validation and cleanup (e.g., handling ISBN as `str`, removing decimal artifacts) |
| **Book Issue Logic** | Simple ISBN lookup and decrement logic | Enhanced with error handling, `try-except`, and better logging for failed transactions |
| **ISBN Formatting** | ISBNs were handled as raw numbers (leading to float conversion) | ISBNs now explicitly converted to string with decimal removed using `.astype(str).str.replace()` |
| **Function Modularity** | Mixed logic and database operations in single block | Functions broken down (e.g., `issue_book`, `return_book`) for better clarity and reuse |
| **Error Logging** | Minimal logging (`print`) | Added descriptive `print` outputs and exception captures for easier debugging |
| **UI Prompting (if any)** | Static query/test cases | Conditional prompts using input cells for interactivity or validation testing |

---

### 📁 Notebook Structure Enhancements

The new version is more modular and production-ready. Notable additions:
- **`database_init()`** with connection setup in one place.
- Improved **SQL parameter handling** using parameterized queries (`%s`) to prevent SQL injection.
- All ISBNs are treated as strings to maintain consistency across systems that may interpret them differently.

---

### ✅ Recommendation

Use the **new version** of the notebook for:
- Better data hygiene (especially ISBN handling)
- More stable and readable issue/return logic
- Enhanced error handling for production/test cases
