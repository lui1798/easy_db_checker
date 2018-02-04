easy db checker
=============
As we know, a typical workflow of manual test  is: 

1. Click a button or link in our system page.
2. Check change in DB via Sequel Pro or MysqlWorkBench.

However,  It’s hard for QA to find all the data change in all the tables, so he/she may neglect some changes due to dev’s bug. It is dangerous for our product. With this tool, it's easy for QA to find all the data changes instantly,so we can find critical bugs easily.

## Installation
please click easy_db_checker.jar, then you can download a file named easy_db_checker.jar.  Then double click this jar and the application will be shown in you right bottom screen. 

Note:
1. JRE must be installed at first.
2. Row based mysql binary log must be opened. You can edit it in my.cnf of mysql server.
```
    #sql_mode=NO_ENGINE_SUBSTITUTION,STRICT_TRANS_TABLES
    log_bin = mysql-bin
    log-slave-updates
    binlog_format = ROW
    server-id = 1
    binlog-do-db = database_name1
    binlog-do-db = database_name2
    binlog-do-db = database_name3
```

## Usage
* main frame

    ![Alt text](/assets/main_frame.png)
* db setting

    ![Alt text](/assets/db_setting.png)
    Local mode is based on mysql binlog, so you should add the databases to binlog-do-db list in my.cnf at first.
* filter setting

    ![Alt text](/assets/setting.png)
    If you don’t want to see data changes of some tables, e.g. change_history. You can put the table to ignored list, then data changes of change history table won’t be shown in main frame.

* clear button

    You can click clear button to clear the changes list.  Shortcut keys is Command + shift + c.
* on top checkbox

    If you select  on top checkbox, the main frame will be above other windows, and the main frame will move to other side when your cursor move to the text output area. This feature is useful when the size of your screen is not very big.


## reference

1. mysql-binlog-connector-java:https://github.com/shyiko/mysql-binlog-connector-java
2. mysql-connector-java:http://dev.mysql.com/downloads/connector/j/
3. jkeymaster: https://github.com/tulskiy/jkeymaster


If you have any problem when you are using it, please let me know.
