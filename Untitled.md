
# <a name="home"></a>***Welcome to Power Trade :***
***

## PowerTrade Documentation:
>+ **[About PowerTrade](#about)**
>+ **[Dashboard](#dashboard)**
>+ **[F8 Matching](#f8)**
>+ **[Clean MIS](#cleanmis)**
>+ **[MIS Report](#misreport)**
>+ **[Cyclical Report](#cycreport)**
>+ **[Analytics](#analytics)**
>+ **[Export](#export)**

***
## <a name="about"></a>What’s special in PowerTrade 2.0.0:
***

#### It’s a next generation’s Trading Support system.
Yes! It is just an accounting software. But yet it is different from its breed in so many ways.
It share its genes from accounting, but it evolve in so many folds that no other accounting system reach at peak of **PowerTrade**.

It supports not only backoffice accounting, but also take your co-pilot seat in trading operations. And gives you a comfort that you are having reliable and sound support a related to trading operations.

![](https://raw.githubusercontent.com/vsrathore/hostimgfile/master/PowerTradeDoc.png)

***
## <a name="dashboard"></a>Dashboard:
***

It is part of **QuickNDirty MIS Module**. Here we can check all open positions as per QuickNDirty method.

### Page Layout: 
> + [Load/Refresh](#dashboard1)
> + [Simple Filter](#dashboard2)

###  <a name="dashboard1"></a>Load/Refresh: 
	Fetch Open Positions from database as per QuickNDirty method. Data loaded from server contain following columns:
> + Client Code
> + Script ID
> + Particular
> + Quantity
> + Buy Price
> + Sell Price
> + Trade Date
> + RollOverPrice
> + RollOver Details
> + Trade ID

###  <a name="dashboard2"></a>Simple Filter:
	Open Position fetched from server from Load/Refresh is filterable by using this button. Following columns are filterable:
> + Client Code
> + Script ID
> + Particular
> + Trade Date


   

***
## <a name="f8"></a>F8 Matching:
***
This is part of **QuickNDirty MIS Module**. All the reports which are available related to QuickNDirty will generate here. Also all raw data (direct from Trading Terminal / ODIN) is feed here.

### Page Layout: 
> + [Raw F8 File](#f81)
> + [Upload Processed F8 file](#f82)
> + [Filter](#f83)
> + [Open Position from Server](#f84)
> + [Push to Server](#f85)

### <a name="f81"></a>Raw F8 File: 
This is used to process raw F8 file which generated from trading terminal.
> + **Input:**	 Raw ODIN’s F8 trade file in CSV format
> + **Output:** Processed F8 file in CSV format

**Note:** Please check date in processed F8 file. Because that will always Current Date. So if we are uploading Raw F8 file of old date/ back date, then we need to manually change that in processed F8 file. This date will be the TradeDate in data. 

###  <a name="f82"></a>Upload Processed F8 file: 
This is used for upload processed F8 file into database. 
> + **Input:**	 Processed F8 file in CSV format
> + **Output:** Nothing. Data uploaded into Database successfully.

### <a name="f84"></a>Open Position from Server:
Fetch Inventory Positions from database as per QuickNDirty method. Data loaded from server contain following columns:
> + Client Code
> + Script ID
> + Particular
> + Quantity
> + Buy Price
> + Sell Price
> + Trade Date
> + RollOverPrice
> + RollOver Details
> + Flag 2
> + Trade ID

### <a name="f83"></a>Simple Filter:
Inventory Position fetched from server from **Open Position from Server** is filterable by using this button. Following columns are filterable:
> + Client Code
> + Script ID
> + Particular
> + Trade Date

### <a name="matching"></a>Matching Operations: 
> + Ctrl-Q : [Match trade](#f8q)
> + Ctrl-X : [Remove selected trade](#f8x)
> + Ctrl-B : [Break trade](#f8b)
> + Ctrl-C : [Consolidate trade](#f8c)
> + Ctrl-I : [RollOver trade](#f8i)
> + Ctrl-E : [Edit trade](#f8e)
> + Ctrl-H : [Show help](#f8h)


### <a name="f8q"></a>Matching trade:
Select two trades by clicking on them. And pass **Ctrl-Q**. If trades are match able they will removed from current table, and added to a new table named ReadyToPushDatabase. And relevant SuccessMessage will show. And if any error occurs, it will show ErrorMessage. And reset all selected trade entries.

## <a name="f85"></a>Push to Server:
Push all closed trades from table named ReadyToPushDatabase to server. And relevant SuccessMessage will show. And if any error occurs, it will show ErrorMessage.

**Note:** Always perform this action before any other Delete, Break, Consolidate or RollOverTrade action. Because these actions will reset any pending ready to push trades.

### <a name="f8x"></a>Delete trade:
Select all trades which we want to delete by clicking on them. And pass **Ctrl-X**. They will removed from current table and Database. And relevant SuccessMessage will show. And if any error occurs, it will show ErrorMessage. And reset all selected trade entries.

### <a name="f8b"></a>Break trade:
Select single trade which we want to break by clicking on them. And pass **Ctrl-B**. A new popup box will open, submit Quantity which we want to break this trade. On clicking **Send** data will refresh with new trades entries. And relevant SuccessMessage will show. And if any error occurs, it will show ErrorMessage. And reset all selected trade entries.

### <a name="f8c"></a>Consolidate trade:
Select all trades which we want to consolidate/merge by clicking on them. And pass **Ctrl-C**. On passing keys data will refresh with new trades entries. And relevant SuccessMessage will show. And if any error occurs, it will show ErrorMessage. And reset all selected trade entries.

### <a name="f8i"></a>RollOver trade:
Select all trades which we want to rollover by clicking on them. And pass ** Ctrl-I**. A new popup box will open, submit New RollOver Particular and RollOver Cost for these trades. On clicking **Send** data will refresh with new trades entries. And relevant SuccessMessage will show. And if any error occurs, it will show ErrorMessage. And reset all selected trade entries.

### <a name="f8e"></a>Edit trade:
Select single trade entry which we want to edit by clicking on them. And pass **Ctrl-E**. A new popup box will open, modify details which we want to update for this trade. On clicking **Send** data will refresh with new trades entries. And relevant SuccessMessage will show. And if any error occurs, it will show ErrorMessage. And reset all selected trade entries.

### <a name="f8h"></a>Show Help:
There is no need to memorize these shortcut commands related to matching/updating trades. Just pass **Ctrl-H**. A new popup box will open and show all help commands. But it will always easy to work with memorized commands.


***
## <a name="cleanmis"></a>Clean MIS:
***
It is part of **Clean MIS Module**. All the reports which are available, related to Clean MIS will generate here. All data is feed here.

### Page Layout: 
> + [Zipped CN](#cleanmis1)
> + [Filter](#cleanmis2)
> + [NSE Open Position](#cleanmis3)
> + [RMC Open Position](#cleanmis4)
> + [Push to Server](#cleanmis5)
> + [Open Position for CMP](#cleanmis6)

### <a name="cleanmis1"></a>Zipped CN: 
This is used to process raw CN files.
> + **Input :** All CN in single zipped file in .ZIP format
> + **Output:** Nothing. Data uploaded into Database successfully

**Note:** Please upload CN in small set for better performance. 


### <a name="cleanmis3"></a>NSE Open Position:
Fetch Inventory Positions from database as per NSE method.

### <a name="cleanmis4"></a>RMC Open Position:
Fetch Inventory Positions from database as per RMC method. Data loaded from server contain following columns:
> + Client Code
> + Script ID
> + Particular
> + Quantity
> + Buy Price
> + Sell Price
> + Trade Date
> + RollOverPrice
> + RollOver Details
> + Flag 2
> + Trade ID

### <a name="cleanmis2"></a>Simple Filter:
Inventory Position fetched from server from NSE/RMC Open Position is filterable by using this button. Following columns are filterable:
> + Client Code
> + Script ID
> + Particular
> + Trade Date

### [Matching Operations](#matching):
Same as F8 Matching operations. [Link](#matching)

### <a name="cleanmis5"></a>[Push to Server](#f85):
Same as F8 PushToServer operations. [Link](#f85)

### <a name="cleanmis6"></a>Open Position for CMP:
It is used for fetching unique particulars from both type of inventory (NSE/RMC). This will open popup box with list of all unique particulars. After entering CMP (Current Market Price) of all particular click on **Send**.  If all CMP filled successfully, another popup box will open. And if any error occurs, it will show ErrorMessage. In next popup box, fill all required details:
> + **Report Date :** M / D / YYYY
> + **Report Type :** NSE / RMC / Leave Blank for All ..
> + **Client Code :** Code1,Code2 / Leave Blank for All ..
> + **Comment     :** If any …


***
## <a name="misreport"></a>MIS Report:
***
It is part of **Clean MIS Module**. Here we can get latest MIS report of clients.

### Page Layout:
> + Client Code
> + RMC / NSE Segment
> + Get Report
> + Report: Summary Report, Equity, FO and Currency Report

### Working:
Toggle segment by clicking on **RMC/NSE**. Then submit **ClientCode**. Then click on **Get Report**. If client code present in database and its report was created in previous step (Link:[CleanMIS](#cleanmis) [OpenPositionforCMP](#cleanmis6)) , it will show report of requested client with SuccessMessage. And if any error occurs, it will show ErrorMessage.

### Report:
Reports will show as **Summary Report**. And also show separate report for each Cash, FO and Currency segment. Click on relevant tab for particular segment’s report. Reports will hold following details:
> + **Particular :** Detail of particular
> + **Inventory :** Open position
> + **CMP :** Current Market price (as of Report Created date)
> + **Net P/L :** Net Profit/Loss  (MTM + Booked P/L)
> + **Adj_Price :** Booked Profit/Loss adjusted price 
> + **Actual_Price :** Actual Inventory price on which trade done
> + **MTM :** Mark to Market
> + **Booked P/L :** Booked Profit/Loss (Dehadi in case of RMC report)


***
## <a name="cycreport"></a>Cyclical Report:
***
It is part of **Advance Reporting Module**. Here we can get latest Cyclical MIS report of clients.

### Page Layout:
> + [General Report](#cycreport1)
> + [Cyclical Report](#cycreport2)

### <a name="cycreport1"></a>General Report:
> + Client Code
> + Script ID
> + Particular
> + Get Report

#### Working:
Submit **ClientCode** and click on **Get Report**. If client code present in database, it will show report of requested client with SuccessMessage. And if any error occurs, it will show ErrorMessage. General Report is calculated with assumption of whole trading time period as single cycle.

#### Report Output:
Reports will show a General Cyclical Report. This fetched report is filterable with following columns:
> + Client Code
> + Script ID
> + Particular

#### Reports will hold following details:
> + **Client Code :** Client Code
> + **Script ID :** Particular segment
> + **Particular :** Detail of particular
> + **Closed Trades :** Number of total closed trades
> + **Profit Trades :** Number of trades with profit
> + **Profit Trades (%) :** Percentage of profitable trades
> + **Holding Period :** Holding period of trades in days
> + **Total Margin Utilized :** Total Margin Utilized
> + **Average Margin :** Average margin utilized
> + **Cost of funds :** Cost of funds
> + **Dehadi :** Profit/Loss on closed trades
> + **Net IRR :** Net IRR

### <a name="cycreport2"></a>Cyclical Report:
> + Client Code
> + Script ID
> + Particular
> + Cycle
> + Get Report

#### Working:
The only difference between [GeneralReport](#cycreport1) and this is, here we have flexibility of defining cycles. So first define cycle. Submit ClientCode and defined Cycle. Then click on Get Report. If client code present in database, it will show report of requested client with SuccessMessage. And if any error occurs, it will show ErrorMessage. Cyclical Report is calculated with referance to user defined cycle.

#### How to define cycle:
Suppose user want to define 2 cycles as following:

Cycle Name | Start Date | End Date 
-----------  | ---------------- | ---------- 
1stCycle  | 1st Jan 2014 | 31st Dec 2014  
2ndCycle | 1st Jan 2015 | 31st Dec 2015


**Define:**  1stCycle,2ndCycle#2014-01-01,2014-12-31,2015-12-31

    Syntext : Cycle1,Cycle2,….,CycleN#Date(yyyy-mm-dd)………

#### Report Output:
Reports will show a Cyclical Report. This fetched report is filterable with following columns:
> + Client Code
> + Script ID
> + Particular
> + Cycle

#### Reports will hold following details:
> + **Client Code :** Client Code
> + **Script ID :** Particular segment
> + **Particular :** Detail of particular
> + **Cycle :** Cycle Name
> + **Closed Trades :** Number of total closed trades
> + **Profit Trades :** Number of trades with profit
> + **Profit Trades (%) :** Percentage of profitable trades
> + **Holding Period :** Holding period of trades in days
> + **Total Margin Utilized :** Total Margin Utilized
> + **Average Margin :** Average margin utilized
> + **Cost of funds :** Cost of funds
> + **Dehadi :** Profit/Loss on closed trades
> + **Net IRR :** Net IRR


#### [Back link to top](#home)

### Welcome to [PowerTrade](http://testtrade.herokuapp.com/login)
