The Kite PnL Problem Statement
The client has given us the " orders " file in CSV format. This file contains data on all trades made by an intraday trader in
different stocks.
The column fields are:
1. Time: It is a timestamp (date with time)
2. Type: It explains the type of trade (Buy or Sell)
3. Instrument: This is the name of a stock
4. Product: "MIS" means it is an intraday trade meaning we have to buy and sell on the same day. "CNC" orders are
held for longer than 1 day. We are interested in “MIS” products.
5. Qty.: This contains the number of shares bought or sold. The format is:
number_of_shares_executed/total_number_of_shares_placed_by_trader
6. Avg. Price: This is the price at which trade took place (can be either buy or sell).
7. Status: It contains three fieldsa. Cancelled: This means the order is cancelled by the trader.
• It might be possible that a trader cancels an order before it is completely executed or partially
executed.
• A trader can't cancel an order if it is fully executed.
b. Rejected: It means the order is rejected by the stock exchange.
• The reasons could be incorrect price, insufficient funds etc.
• We can ignore this type of trade in calculations.
c. Completed: It means the order is completed.
CLIENT REQUIREMENT:
Create a summary file in Excel that should contain three tables in different Excel sheets:
1) Different types of charges for Individual trade
Type Stock Product Qty. Avg.
price
Status Turnover Brokerage STT/CTT ETC SEBI GST Stamp
charges
Total
charges
2) Stock wise and Type wise analysis with weighted Avg. price & calculated charges
Instrument Type Qty. Avg.
price
Turnover Brokerage STT/CTT ETC SEBI GST Stamp
charges
Total
charges
3) Overall Summary of each Stocks
Instrument Gross PnL Total charges Net PnL % Charges on Gross PnL
YOUR TASK:
• You have to write a Python program which will calculate the above-mentioned charges and write them into an Excel file.
NOTE:
To calculate transaction charges, refer to this: https://zerodha.com/charges#tab-equities, in given link check for
Equity Intraday section. Use NSE values for calculations.
