---
title: Service interfaces for Expense Reporting App using MongoDB
description: Service interfaces for Expense Reporting App using MongoDB
---
```java
package com.springsource.html5expense.services;

import java.util.List;

import com.springsource.html5expense.model.ExpenseType;

public interface ExpenseTypeService {
    List<ExpenseType> getAllExpenseType();

    ExpenseType getExpenseTypeById(Long id);
}

```
```java
package com.springsource.html5expense.services;

import java.util.List;

import org.springframework.data.mongodb.core.query.Update;

import com.springsource.html5expense.model.Expense;

public interface ExpenseService {
    Long save(Expense expense);

    Expense getExpense(Long expenseId);

    List<Expense> getAllExpenses();

    List<Expense> getPendingExpensesList();

    Expense changeExpenseStatus(Long expenseId, String state);

    void deleteExpense(Long expenseId);

    void updateExpense(Long expenseId, Update update);
}
```