Mult-threaded java project with cooks, customers, foods and machines.This project aims to keep track of multiple cooks, multiple customers, multiple foods, and simulate the operations of the restaurant.


--------COOKS---------------------\
 Cooks are simulation actors that have at least one field, a name.\
  When running, a cook attempts to retrieve outstanding orders placed\
  by Customer and process them.
 

The cook tries to retrieve orders placed by Customers. For each order, a List<Food>, the  cook submits each Food item in the List to an appropriate Machine type, by calling makeFood(). Once all machines have produced the desired Food, the order is complete, and the Customer is notified. The cook can then go to process the next order. If during its execution the cook is interrupted (i.e., some other thread calls the interrupt() method on it, which could raise InterruptedException if the cook is blocking), then it terminates.
 
-----------------------CUSTOMER----------------------------\
  Customers are simulation actors that have two fields: a name, and a list
  of Food items that constitute the Customer's order. When running, an
  customer attempts to enter the Ratsie's (only successful if the
  Ratsie's has a free table), place its order, and then leave the
  Ratsie's when the order is complete.

---------------Machines-----------------\
  Machines are used to make different kinds of Food. Each Machine type makes
  just one kind of Food. Each machine type has a count: the set of machines of
  that type can make that many food items in parallel. If the machines are
  asked to produce a food item beyond its count, the requester blocks. Each
  food item takes at least item.cookTime10S seconds to produce. In this
  simulation, use Thread.sleep(item.cookTime10S) to simulate the actual cooking
  time.

---RAT class----\
The Rat class is used to tie all these classes together, and simulate the functions of the restaurant.


--Validate Class---\
The validate class is used to validate the operations of the Resturaunt, and simulate it appropriately. 
