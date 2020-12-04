# Full-Stack-Onboarding

## Install Visual Studio Code
https://code.visualstudio.com/

---

## Install Git
https://git-scm.com/download

Note: Please make sure you have installation rights.

---

## Install Node
https://nodejs.org/en/

Note: Please make sure you have installation rights.

---

## Setup proxy

Example:

User name: `abcxyz`

Password: `abc@123` (Note that if password has @ then replace it with equivalent url encoding. i.e. `%40`. All special characters has to be replaced with equivalent url encoding)

Proxy URL: `proxy.company.com`

Port: `8080`

Reference: https://www.w3schools.com/tags/ref_urlencode.asp

For above username and password proxy would be:
`http://abcxyz:abc%40123@proxy.company.com:8080/`


Run following 4 commands through command line:
```
git config --global http.proxy http://<USERNAME>:<PASSWORD>@proxy.company.com:<PORT>/
git config --global https.proxy http://<USERNAME>:<PASSWORD>@proxy.company.com:<PORT>/
npm config set http-proxy http://<USERNAME>:<PASSWORD>@proxy.company.com:<PORT>/
npm config set https-proxy http://<USERNAME>:<PASSWORD>@proxy.company.com:<PORT>/
```

`<USERNAME>` is your windows username.

`<PASSWORD>` is your windows password.

---

## Install SQL Server Express
[SQL EXPRESS](https://www.microsoft.com/en-us/sql-server/sql-server-editions-express)

Server=localhost\SQLEXPRESS;
Database=master;
Trusted_Connection=True

---

## Install SQL Server Management Studio
https://docs.microsoft.com/en-us/sql/ssms/download-sql-server-management-studio-ssms?view=sql-server-2017

### Go to Microsoft SQL Server Management Studio

Expand Security folder

Right Click Logins

Click New Login...

add Login name as `mssql`

Select SQL Server authentication

write password as `mssql`

Uncheck Enable password policy.

Highlight `Service Roles`

check `sysadmin`

Click Ok

Right click on SQL Server and select properties option.

Go to security. Select `SQL Server and Windows Authentication mode` and click ok.


### Open SQL Server Configuration Manager

Expand `SQL Server Network Configuration` and click on `Protocols for MSSQLSERVER`

Right click on `TCP/IP` and choose `Enable`

Click `OK` on the Warning that the service will have to be restarted

Right click on `TCP/IP` again and select `Properties`

Select the IP Addresses tab and make sure the TCP Port for IPAII is 1433.

Click on `SQL Server Services`

Right click on `SQL Server (MSSQLSERVER)` and choose `Restart`


### SQL Server Browser windows service:

Navigate to "Services"

Select "Properties" on "SQL Server Browser"

Flip "Start up type" to "Automatic"

Start the service

