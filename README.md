# Student Record Management System

## Overview
This program is a **Student Record Management System** implemented in C. It allows users to perform various operations on a linked list of student records, such as adding, deleting, modifying, and sorting records. The program is menu-driven and provides a simple text-based interface for interaction.

---

## Features
1. **Add New Record**:
   - Add a new student record with name, marks, and an auto-generated roll number.

2. **Delete Record**:
   - Delete a record by roll number or name.

3. **View Records**:
   - Display the entire list of student records in a tabular format.

4. **Modify Record**:
   - Update student details (name, roll number, or both).

5. **Save Records**:
   - Save the current list of records to a file named `student.dat`.

6. **Exit**:
   - Exit the program with an option to save the data.

7. **Sort Records**:
   - Sort the records by name or marks.

8. **Delete All Records**:
   - Clear all student records from the system.

9. **Reverse List**:
   - Display the records in reverse order.

---

## How to Compile and Run
1. **Compile the Program**:
   ```bash
   gcc -o student_record_system Database_system.c
   ```

2. **Run the Program**:
   ```bash
   ./student_record_system
   ```

---

## Menu Options
| Option | Functionality                        |
|--------|-------------------------------------|
| `a/A`  | Add new record                      |
| `d/D`  | Delete a record                     |
| `s/S`  | Show all records                    |
| `m/M`  | Modify a record                     |
| `v/V`  | Save the records to a file          |
| `e/E`  | Exit the program                    |
| `t/T`  | Sort the records                    |
| `l/L`  | Delete all records                  |
| `r/R`  | Reverse the list                    |

---

## Code Highlights
### Data Structure
```c
typedef struct student {
    int roll;
    char name[30];
    float mark;
    struct student* next;
} ST;
```
This structure represents a student record containing:
- **roll**: Unique roll number (auto-incremented).
- **name**: Name of the student.
- **mark**: Marks obtained by the student.
- **next**: Pointer to the next student record (used for the linked list).

### Important Functions
1. **Adding Records**:
   ```c
   int add_end(ST **ptr, int rn);
   ```
   Prompts the user to input name and marks for a new student and appends the record to the list.

2. **Deleting Records**:
   ```c
   void delete(ST **ptr);
   ```
   Deletes a record based on the roll number or name.

3. **Sorting Records**:
   ```c
   void sort(ST *ptr);
   ```
   Sorts the records by name or marks using bubble sort.

4. **Saving Records**:
   ```c
   void save(ST *ptr);
   ```
   Saves all records to a file `student.dat` in plain text format.

5. **Reversing Records**:
   ```c
   void reverse(ST *ptr);
   ```
   Displays the records in reverse order.

---

## File Operations
- Records are saved to `student.dat` using the `save()` function.
- The file format is:
  ```
  RollNo   Name   Marks
  1        Alice  85.5
  2        Bob    78.0
  ```

---

## Future Improvements
1. Add functionality to load records from a file at startup.
2. Implement error handling for file operations.
3. Enhance the sorting algorithm for scalability.
4. Add a graphical user interface (GUI).

---

## Contribution
Feel free to fork the repository, raise issues, or submit pull requests to improve this project.

---

