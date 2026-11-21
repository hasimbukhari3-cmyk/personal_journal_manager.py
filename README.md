# personal_journal_manager.py

# File Operator – Personal Journal Manager

## Description
A Python console application that demonstrates file handling operations and exception handling through a Personal Journal Manager. It uses OOP principles including class design, encapsulation, and instance methods.

## Features
- Add new journal entries with timestamps.
- View all journal entries from the file.
- Search for entries by keyword or date.
- Delete all entries with confirmation.
- Handle `FileNotFoundError`, `PermissionError`, and other exceptions gracefully.
- Menu-driven interface with input validation.

## Assumptions
- Journal entries are stored in `journal.txt` in the current directory.
- Each entry is prefixed with a timestamp in `[YYYY-MM-DD HH:MM:SS]` format.
- Entries are separated by a blank line.
- Search is case-insensitive and matches both timestamp and entry text.
- Data persists between program runs.

## File Handling Modes Used
| Mode | Operation | Method |
|------|-----------|--------|
| `'a'` | Append entries | `add_entry()` |
| `'r'` | Read entries | `view_entries()`, `search_entries()` |
| `os.remove()` | Delete file | `delete_entries()` |

## Class Structure
JournalManager
├── __init__(filename)
├── add_entry()
├── view_entries()
├── search_entries()
└── delete_entries()

## How to Run
1. Ensure Python 3.x is installed.
2. Clone the repository.
3. Run: `python personal_journal_manager.py`

## Sample Output
(============================================================
Welcome to Personal Journal Manager!
============================================================
This program demonstrates file handling, exception handling,
and OOP principles including class design and encapsulation.

JournalManager initialized with file: journal.txt

==================================================
--- Personal Journal Manager ---
==================================================
Please select an option:
1. Add a New Entry
2. View All Entries
3. Search for an Entry
4. Delete All Entries
5. Exit
==================================================
Enter your choice: 1

--- Add a New Entry ---
Enter your journal entry:
Today was a productive day. I learned about file handling in Python.

Entry added successfully!

Press Enter to continue...

==================================================
--- Personal Journal Manager ---
==================================================
Please select an option:
1. Add a New Entry
2. View All Entries
3. Search for an Entry
4. Delete All Entries
5. Exit
==================================================
Enter your choice: 1

--- Add a New Entry ---
Enter your journal entry:
Had a great session on OOP concepts!

Entry added successfully!

Press Enter to continue...

==================================================
--- Personal Journal Manager ---
==================================================
Please select an option:
1. Add a New Entry
2. View All Entries
3. Search for an Entry
4. Delete All Entries
5. Exit
==================================================
Enter your choice: 2

--- View All Entries ---

Your Journal Entries:
==================================================
[2024-12-25 10:00:00]
Today was a productive day. I learned about file handling in Python.

[2024-12-24 18:00:00]
Had a great session on OOP concepts!

==================================================

Press Enter to continue...

==================================================
--- Personal Journal Manager ---
==================================================
Please select an option:
1. Add a New Entry
2. View All Entries
3. Search for an Entry
4. Delete All Entries
5. Exit
==================================================
Enter your choice: 3

--- Search for an Entry ---
Enter a keyword or date to search: productive

Matching Entries:
==================================================
[2024-12-25 10:00:00]
Today was a productive day. I learned about file handling in Python.
--------------------------------------------------

Press Enter to continue...

==================================================
--- Personal Journal Manager ---
==================================================
Please select an option:
1. Add a New Entry
2. View All Entries
3. Search for an Entry
4. Delete All Entries
5. Exit
==================================================
Enter your choice: 3

--- Search for an Entry ---
Enter a keyword or date to search: vacation

No entries were found for the keyword: vacation.

Press Enter to continue...

==================================================
--- Personal Journal Manager ---
==================================================
Please select an option:
1. Add a New Entry
2. View All Entries
3. Search for an Entry
4. Delete All Entries
5. Exit
==================================================
Enter your choice: 4

--- Delete All Entries ---
Are you sure you want to delete all entries? (yes/no): yes
All journal entries have been deleted.

Press Enter to continue...

==================================================
--- Personal Journal Manager ---
==================================================
Please select an option:
1. Add a New Entry
2. View All Entries
3. Search for an Entry
4. Delete All Entries
5. Exit
==================================================
Enter your choice: 2

--- View All Entries ---
Error: The journal file does not exist. Please add a new entry first.

Press Enter to continue...

==================================================
--- Personal Journal Manager ---
==================================================
Please select an option:
1. Add a New Entry
2. View All Entries
3. Search for an Entry
4. Delete All Entries
5. Exit
==================================================
Enter your choice: 6

Invalid option. Please select a valid option from the menu.

Press Enter to continue...

==================================================
--- Personal Journal Manager ---
==================================================
Please select an option:
1. Add a New Entry
2. View All Entries
3. Search for an Entry
4. Delete All Entries
5. Exit
==================================================
Enter your choice: 5

Thank you for using Personal Journal Manager. Goodbye!)

## Author
[Hasim Bukhari]
