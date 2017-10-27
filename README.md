# use-sqlserver-from-macos
Hate to use SSMS (GUI Client) of SQL Server, and try to run a command line on MacOs, and simulate Oracle Commands 

# What you can get here

- run sqlcmd on MacOS, as 'Oracle SQLPLUS' 
- run scripts in command line via sqlcmd
- run some scripts like export, import, plus DESC, TAB in SQLPLUS

# Why not using SSMS or Sqlcmd on Windows

- Do not like SSMS GUI, and prefer command line and scripts (can reuse scripts)
- Using MacOS, rather than Windows (My new i5 windows notebook is quit slow running huge SSMS)
- As a Oracle DBA, I can not find the right command in sqlcmd, such as 'describe table_x'


# Have a SQL Server Client on MacOS

No offical SQL Server Client for MacOS (as 2017/10/01). An alternative choice is some payed GUI client by third party, which you can search in Mac App Store.

Many thanks to Docker. There is using a [SQL Server docker image](https://hub.docker.com/r/microsoft/mssql-server-linux/), which contain a DB Server and client.

'''bash
docker pull microsoft/mssql-server-linux:2017-latest
'''


# Run Sqlcmd in bash of the docker

Run the client command line inner the docker. Either connect to a local Sqlserver DB or a remote one

'''bash
run_docker.sh        # run a docker and use bash of the container 

cd /work

/opt/mssql-tools/bin/sqlcmd -?
'''

# Source envs for remote/local DB and run scripts


