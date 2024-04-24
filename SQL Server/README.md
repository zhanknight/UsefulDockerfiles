# SQL Server in a Container

See more details [here.](https://learn.microsoft.com/en-us/sql/linux/quickstart-install-connect-docker?view=sql-server-ver16&tabs=cli&pivots=cs1-bash) 

## Commands
1. `docker pull mcr.microsoft.com/mssql/server:2022-latest`

1. `docker run -e "ACCEPT_EULA=Y" -e "MSSQL_SA_PASSWORD=<YourStrong@Passw0rd>" 
   -p 1433:1433 --name sql1 --hostname sql1 
   -d 
   mcr.microsoft.com/mssql/server:2022-latest`

1. `docker exec -it sql1 /opt/mssql-tools/bin/sqlcmd 
   -S localhost -U SA -P "<YourStrong@Passw0rd>" 
   -Q "ALTER LOGIN SA WITH PASSWORD='<YourNewStrong@Passw0rd>'"`

1. Then disable the SA account.

## Connect

The database can be connected to and used either within the container itself using the CLI and sqlcmd or externally using SSMS or anything else, using the container hostname/ip/port.

### Connect within container

1. `docker exec -it sql1 "bash"` in a terminal.
1. `sudo /opt/mssql-tools/bin/sqlcmd -S localhost -U <userid> -P "<YourNewStrong@Passw0rd>"`




   
