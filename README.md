# FoodBridge 🍲
**An Expiry-Aware Surplus Food Donation Allocator**
Data Structures & Algorithms Project · BSCS Semester 3 (C3B) · Fatima Business School, Salim Habib University

FoodBridge sends surplus food from restaurants, supermarkets and wedding halls to the shelters that need it most, **before it expires**.

## How it works
- **Min-Heap** (our own implementation): the food that expires first is always on top.
- **Priority Queue**: the most urgent shelter is served first (ties go to the larger need).
- **HashMap ×3**: find any donor, food item or organization by ID (D1, F1, O1) in O(1).
- Each delivery gives **min(food available, storage space, need)**, so food is never wasted and no shelter is overloaded.
- **SQLite database (JDBC)**: all data is saved after every change and loaded again on start.

## Files
| File | What it is |
|---|---|
| `code.zip` | Java program: `Main.java`, `Database.java`, `MainTest.java` (11 JUnit tests) and the SQLite driver. Unzip it to run. |
| `FoodBridge-GUI (3).html` | Web GUI (open in any browser) |
| `FoodBridge-Project-Report (1).docx` | Project report |
| `FoodBridge-Presentation (1).pptx` | Presentation slides |
| `FoodBridge-SRS (2).pdf` | Software Requirements Specification |
| `FoodBridge-Poster (1).pdf` | Project poster |
| `FoodBridge-Intro-Video.mp4` | 1:20 intro film |

## Run the Java program
1. Download `code.zip` and unzip it.
2. Open a terminal inside the `code` folder and run:

```
javac -cp lib/sqlite-jdbc-3.41.2.2.jar *.java
java -cp ".;lib/sqlite-jdbc-3.41.2.2.jar" Main
```

On Mac/Linux use `:` instead of `;`. Quick demo: choose `7` → `2`, then `4`, `5`, `11`.

## Author
**Ayesha Shafiq** · F25CSC068
Supervisor: Miss Saadia Karim · Lab: Sir Salman Khan
