# MizhuoSample
Mizhuo Sample
Sample application for trading.
1. Load the csv file with correct template (Click the Export Template button, save the valid template and use the template to load orders).
2. Click Submit button to send to Exchange.
    The Price (greater than zero), Quantity (greater than zero) and Lot size (maximum of 100,000 for each instrument) is validated.
    Validation failed orders are not sent to Exchange (check the red alert on the UI controls and message is provided with a tooltip).
    Update the failed orders and click submit button (Errors on the orders will be removed if it succeeds the validation).
3. Click Export Csv button to export the orders to csv file.
4. Delete All button deletes all the orders.
5. Delete button deletes only the current order.
6. User can not edit/delete the order when the order is submitted.
7. Legends - Displays the order status.



Sample CSV Load data (used for testing).

TradingAccount	UserId	InstrumentCode	Side	Price	Quantity
c123	        Rav123	C123		            0	    10000
d123	        Raj123	D123		            2000	100000
f123	        Rag123	F123	                123		100000
e123	        Ram123	E123		            10	    1
g123	        Ran123	G123	         abc	2000	100000
h123	        Rah123	H123		            10	    100000
e123	        Raj123	E123		            10	    100000


OrderStatus Flow
Status                      New             ->  Submitted           ->   Approved           ->    Rejected
Validation Failed           Csv upload order.
New Order                   Csv upload order.
Waiting for Exchange        Csv upload order-> Submitted To Exchange.
Approved by Exchange        Csv upload order-> Submitted To Exchange-> Approved by Exchange.
Rejected by Exchange        Csv upload order-> Submitted To Exchange--------------------------> Rejected By Exchange.
