# 📚 Library Management System (Console-Based)

This is a console-based Library Management System built with Python. It allows administrators and members to manage books, members, and borrowing records. All data is stored in CSV files.

## 📁 Project Structure

```
├── main.py             # Main program with all features and menu logic
├── raw_input.py        # Script to auto-generate example CSV files
├── books.csv           # Stores book records
├── members.csv         # Stores member records
├── borrows.csv         # Stores borrowing records
```

## 🔧 Features

### 👨‍💼 Admin
- Add, update, delete, and search books
- Register, update, view, and delete members
- Record and manage book borrowing/returns
- View borrowed/overdue books and generate reports

### 👤 Member
- Log in using Member ID
- View available books
- Borrow and return books
- View their own active borrowed books

## 🔐 Login Credentials

- **Admin Username**: `admin`
- **Admin Password**: `admin123`

## 🏁 Getting Started

1. **Install Python 3** if you haven’t already.
2. Run the following script to generate sample data:

```bash
python raw_input.py
```

3. Then run the main program:

```bash
python main.py
```

4. Follow the console instructions to interact with the system.

## 📦 Dependencies

None. This project uses only Python’s built-in libraries:
- `csv`
- `os`
- `datetime`

## 📝 Example Data

**Books**

| book_id | title                   | author              | genre     | publication_year | available | times_borrowed |
|---------|-------------------------|---------------------|-----------|------------------|-----------|----------------|
| B001    | 1984                    | George Orwell       | Dystopian | 1949             | True      | 5              |

**Members**

| member_id | name       | contact_info           |
|-----------|------------|------------------------|
| M001      | John Doe   | johndoe@example.com    |

**Borrows**

| borrow_id         | book_id | member_id | borrow_date | return_date | late_fee |
|-------------------|---------|-----------|-------------|-------------|----------|
| BR20250219101010… | B002    | M001      | 2025-02-01  | 2025-02-15  | 0        |

## 📌 Notes
- Late fee is calculated after 14 days of borrowing.
- Borrowed books cannot be deleted.
- Members with active borrows cannot be deleted.

## 📃 License

MIT License
