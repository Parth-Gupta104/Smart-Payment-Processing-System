Design and implement a Smart Payment Processing System using Object-Oriented 
Programming concepts in Python. 
The system should allow a user to make payments using 
different payment methods such as Credit Card, UPI, PayPal, and Digital Wallet. Each 
payment method must follow a common interface but implement different business logic
for computing the final payable amount.
Create an abstract base class named Payment that stores the user name and declares an 
abstract method pay(amount) which must be implemented by all child classes. The base 
class should also contain a concrete method generate_receipt() that prints the user name, 
original amount, and final amount paid after processing.

Implement the following payment types by inheriting from the Payment class:

> CreditCardPayment: Apply a 2% gateway fee on the transaction amount and then 
apply 18% GST on the gateway fee. The final amount should be computed by 
adding the original amount, gateway fee, and GST. 

> UPIPayment: Provide a cashback of ₹50 if the payment amount is greater than 1000. 
Otherwise, no cashback is applied. The final payable amount should be calculated 
after subtracting cashback. 

> PayPalPayment: Apply a 3% international transaction fee and an additional fixed 
currency conversion fee of ₹20. These charges should be added to the original 
amount to compute the final payment.

> WalletPayment: This payment method should maintain a wallet balance. If the 
payment amount exceeds the available balance, the transaction should fail. Otherwise, 
deduct the amount from the wallet and update the remaining balance.
