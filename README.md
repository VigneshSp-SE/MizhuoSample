# MizhuoSample
Mizhuo Sample
Sample application for trading.
1. Load the csv file with correct template (Click the Export Template button, save the valid template and use the template to load orders).
2. Click Submit button to send to Exchange.
    The Price (greater than zero), Quantity (greater than zero) and Lot size (maxmimum of 100,000 for each instrument) is validated.
    Validation failed orders are not sent to Exchange (check the red alert on the UI controls and message is provided with a tooltip).
    Update the failed orders and click submit button (Errors on the orders will be removed if it succeeds the validation).
3. Click Export Csv button to export the orders to csv file.
