# Expense Tracker  

## Introduction  
This project is designed to assess object-oriented programming (OOP) concepts in Python by implementing an expense tracking system. It includes two main classes:  

- **Expense**: Represents an individual financial expense.  
- **ExpenseDB**: Manages a collection of expenses.  

The program allows users to add, update, retrieve, and remove expenses while maintaining timestamps for accurate record-keeping.  

## Features  
1. Add new expenses with a unique ID  
2. Update expense title or amount  
3. Retrieve expenses by ID or title  
4. Remove an expense from the database  
5. View all stored expenses  

## Technologies Used  
- Python 3  
- `uuid` for unique expense IDs  
- `datetime` for timestamp handling  

## Installation  

### Prerequisites  
Ensure you have **Python 3** installed. You can check your version with:  
```bash
python --version
```
or  
```bash
python3 --version
```

### Clone the Repository  
```bash
git clone https://github.com/your-username/test-expense_tracker.git
cd test-expense_tracker
```

## How to Run the Code  
Execute the script using:  
```bash
python test-expense_tracker.py
```
or (if using Python 3):  
```bash
python3 test-expense_tracker.py
```

## Example Usage  

### Adding an Expense  
```python
from expense_tracker import Expense, ExpenseDB

db = ExpenseDB()
expense1 = Expense("Groceries", 50.00)
db.add_expense(expense1)
print(db.to_dict())
```

### Updating an Expense  
```python
expense1.update(amount=60.00)
print(expense1.to_dict())
```

### Retrieving an Expense by ID  
```python
found_expense = db.get_expense_by_id(expense1.id)
print(found_expense.to_dict() if found_expense else "Expense not found")
```

### Deleting an Expense  
```python
db.remove_expense(expense1.id)
print(db.to_dict())
```

## Contributing  
You can fix this repository, create a branch, and submit a pull request with improvements.  

## License  
This project is open-source and available under the **MIT License**.  

## Author  
**Taiwo Ajabi**  
[GitHub Profile]((https://github.com/AjabiTaiwo))  
