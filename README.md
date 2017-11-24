# use-sqlserver-from-macos
Hate to use SSMS (GUI Client) of SQL Server, and try to run a command line on MacOs, and simulate Oracle Commands 

# What you can get here

- run sqlcmd on MacOS, as 'Oracle SQLPLUS' 
- run scripts in command line via sqlcmd
- run some scripts like export, import, plus DESC, TAB in SQLPLUS

# Why not using SSMS or Sqlcmd on Windows

- Do not like SSMS GUI, and prefer command line and scripts (can reuse scripts)
- Using MacOS, rather than Windows (My new i5 windows notebook is quit slow running huge SSMS)
- As a Oracle DBA, I can not find the right command in sqlcmd, such as `describe table_x`


# Have a SQL Server Client on MacOS

_**NO offical SQL Server Client is availabe for MacOS (as 2017/10/01)**_. An alternative choice is some payed GUI client by third party, which you can search in Mac App Store.

Many thanks to Docker. There is [SQL Server docker image](https://hub.docker.com/r/microsoft/mssql-server-linux/), which contains Sqlserver DB Server and Client.

```bash
docker pull microsoft/mssql-server-linux:2017-latest
```


# Run Sqlcmd in bash of the docker

Run the client command line inner the docker. Either connect to a local Sqlserver DB or a remote one

```bash
run_docker.sh        # run a docker and use bash of the container 

cd /work

/opt/mssql-tools/bin/sqlcmd -?
```

# Source envs for remote/local DB and run scripts

## desc.sh - show a table's fields

## tab.sh - show a tables

## export.sh - export a query's result as csv file with default field spliter "|"

## import_via_insert.sh - use insert instead of bulk
https://docs.microsoft.com/en-us/sql/t-sql/statements/bulk-insert-transact-sql


# Reference

## sqlcmd command line parameters

```bash
/opt/mssql-tools/bin/sqlcmd -?
```

## Commands in sqlcmd

```
-- use help to know more
:help
:quit
```

## T-SQL Examples

### use/list a database

```
use mydb;
go
```

TODO

### backup/recover a database

TODO

### read/create/insert/delete/drop a table

TODO

### import/export a table

TODO

### list/describe tables/views

TODO

### clone a table

```
select * into cloned_mytab from mytab;
go
```

### read/create/insert/delete/drop a view

TODO

### define/use a variable

TODO

### try, catch, and exception

TODO

### with

TODO
