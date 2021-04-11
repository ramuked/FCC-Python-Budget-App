## Python Budget App for FCC Scientific Computing with Python Course


The category class instantiates objects based on different budget categories like *food*, *clothing*, and *entertainment*. When objects are created, they are passed in the name of the category. The class has an instance variable called `ledger` that is a list. The class also contains the following methods:

* A `deposit` method that accepts an amount and description. If no description is given, it defaults to an empty string. The method  appends an object to the ledger list in the form of `{"amount": amount, "description": description}`.

* A `withdraw` method that is similar to the `deposit` method, but the amount passed in should be stored in the ledger as a negative number. If there are not enough funds, nothing should be added to the ledger. This method returns`True` if the withdrawal took place, and `False` otherwise.

* A `get_balance` method that returns the current balance of the budget category based on the deposits and withdrawals that have occurred.

* A `transfer` method that accepts an amount and another budget category as arguments. The method adds a withdrawal with the amount and the description "Transfer to [Destination Budget Category]". The method then adds a deposit to the other budget category with the amount and the description "Transfer from [Source Budget Category]". If there are not enough funds, nothing should be added to either ledgers. This method should return `True` if the transfer took place, and `False` otherwise.

* A `check_funds` method that accepts an amount as an argument. It returns `False` if the amount is greater than the balance of the budget category and returns `True` otherwise. This method should be used by both the `withdraw` method and `transfer` method.

When the budget object is printed it displayx:
* A title line of 30 characters where the name of the category is centered in a line of `*` characters.
* A list of the items in the ledger.
* A line displaying the category total.

Here is an example of the output:
```
*************Food*************
initial deposit        1000.00
groceries               -10.15
restaurant and more foo -15.89
Transfer to Clothing    -50.00
Total: 923.96
```

Besides the `Category` class, a function (outside of the class) called `create_spend_chart` that takes a list of categories as an argument. It should return a string that is a bar chart.

The chart will show the percentage spent in each category passed in to the function. The percentage spent should be calculated only with withdrawals and not with deposits. 


```
Percentage spent by category
100|          
 90|          
 80|          
 70|          
 60| o        
 50| o        
 40| o        
 30| o        
 20| o  o     
 10| o  o  o  
  0| o  o  o  
    ----------
     F  C  A  
     o  l  u  
     o  o  t  
     d  t  o  
        h     
        i     
        n     
        g     
```

The unit tests for this project are in `test_module.py`.


