# Bank Management System (C)

A console-based banking system written in C. It has two modes: customer record management and a simulated ATM protected by a PIN.

## Features

When the program starts, choose a mode:

### 1. Transactions (ATM)
Enter your PIN, then choose:

| Option | Action |
|---|---|
| 1. Balance Enquiry | Show the current balance |
| 2. Withdraw Cash | Withdraw a custom amount (up to Rs 25,000 per transaction) |
| 3. Deposit Cash | Add funds to the balance |
| 4. Fast Cash | One-tap withdrawals of Rs 5,000 – 25,000 |
| 5. Quit | Exit the ATM |

### 2. Customer Records (CRUD)
Manage up to 20 customers:

| Option | Action |
|---|---|
| 1. Insert Record | Add a customer (account number, name, balance, age) |
| 2. Delete Record | Remove a customer by account number |
| 3. Update Record | Edit a customer's details |
| 4. Display Records | List all customers |
| 5. Save Records to File | Write all records to `bank_records.txt` |
| 6. Exit | Close the program |

## Data Model

```c
struct Customer {
    int   accountNumber;
    char  name[50];
    float balance;
    int   age;
};
```

## Build and Run

```bash
gcc Bank.c -o bank
./bank
```

On Windows, run `bank.exe` instead. The demo PIN is defined in `Bank.c`.

## Concepts Practised

Structs · arrays · CRUD operations · file I/O · nested menus
