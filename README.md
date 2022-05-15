# azure-sql-edge-compose

Docker compose file for working with azure sql edge

I want to run a SQL Server on Mac with M1 but SQL Server for Linux docker image does not run on M1 chip, which uses ARM architecture.

So I found this post [How to Install SQL Server on an M1 Mac (ARM64)](https://database.guide/how-to-install-sql-server-on-an-m1-mac-arm64/) explaining how to run Azure SQL Edge on Mac M1 machine.


sudo docker run --cap-add SYS_PTRACE -e 'ACCEPT_EULA=1' -e 'MSSQL_SA_PASSWORD=bigStrongPwd' -p 1433:1433 --name sqledge -d mcr.microsoft.com/azure-sql-edge

