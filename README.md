easy db checker
=============
As we know, a typical workflow of manual test  is: 
Click a button or link in our system page.
check change in DB via Sequel Pro or MysqlWorkBench.
However,  It’s hard for QA to find all the data change in all the tables, so he/she may neglect some changes due to dev’s bug. It is dangerous for our product. With this tool, it's easy for QA to find all the data changes instantly,so we can find critical bugs easily.

## Installation
please visit http://git.dev.fwmrm.net/hackathon/easy_db_checker/blob/master/easy_db_checker.jar and click download link, then you can download a file named easy_db_checker.jar.  Then double click this jar and the application will be shown in you right bottom screen. JRE must be installed at first.

## Usage
1) main frame

2)db setting
Local mode is based on mysql binlog, so you should add the databases to binlog-do-db list in my.cnf at first.

3) filter setting
If you don’t want to see data changes of some tables, e.g. change_history. You can put the table to ignored list, then data changes of change history table won’t be shown in main frame.

4) STG/PROD mode
STG/PROD mode is based on change history, so we need to filter out the data changes due to others' actions. Please copy the session id in cookies and then paste the session id into input dialog before you see the data changes.

5) clear button
You can click clear button to clear the changes list.  Shortcut keys is Command + shift + c.

6) on top checkbox
If you select  on top checkbox, the main frame will be above other windows, and the main frame will move to other side when your cursor move to the text output area. This feature is useful when the size of your screen is not very big.


4. reference

1.mysql-binlog-connector-java:https://github.com/shyiko/mysql-binlog-connector-java
2. mysql-connector-java:http://dev.mysql.com/downloads/connector/j/
3.jkeymaster: https://github.com/tulskiy/jkeymaster


If you have any problem when you are using it, please let me know.
