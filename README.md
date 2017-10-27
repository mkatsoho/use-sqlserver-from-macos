# use-sqlserver-from-macos
Hate to use SSMS (GUI Client) of SQL Server, and try to run a command line on MacOs, and simulate Oracle Commands 


# Have a SQL Server Client on MacOS
No offical SQL Server Client for MacOS (as 2017/10/01). An alternative choice is some payed GUI client by third party, which you can search in Mac App Store.

Many thanks to Docker. There is using a [SQL Server docker image|https://hub.docker.com/r/microsoft/mssql-server-linux/], which contain a DB Server and client.

'''bash
docker pull microsoft/mssql-server-linux:2017-latest
'''


# Run Sqlcmd

