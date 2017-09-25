## Install PostgreSQL 9.1 **
* Make sure you already have install python-software-properties
```
$sudo apt-get install python-software-properties
```

* Add PPA repository to my Ubuntu.
```
$sudo add-apt-repository ppa:pitti/postgresql
```

* After adding PPA, update your system apt:
```
$sudo apt-get update
```

* Finally install postgresql-9.1:
```
$sudo apt-get install postgresql
```
> In case of errors :
**Note:**If you having any error, make sure you already install libpq-dev.The libpq-dev package is for compiling wrappers/clients against libpq.
```
$sudo apt-get install postgresql-9.1 libpq-dev
```

* Now check it out installation is successful or…..
```
$ locate postgresql
```

* If done!!!, Cheers ………… Check the install version.
```
$psql -V //sometime does not work.But chill
```

* Postgres uses Linux users as the normal users. Create user from Command prompt
```
sudo -u postgres createuser postgresuser
Shall the new role be a superuser? (y/n) n
Shall the new role be allowed to create databases? (y/n) y
Shall the new role be allowed to create more new roles? (y/n) n
```

* Change Postgres User Password
```
First login to postgres
sudo -u postgres psql
Change the password
ALTER USER 'Postgresuser' WITH PASSWORD 'NEW PASSWORD';
```

* Incase of error ‘FATAL: Ident authentication failed for user ‘ , on development 
machine (Not on production!)
```
sudo nano /etc/postgresql/9.1/main/pg_hba.conf
Change => local all all ident
To => local all all trust
if still doesn't work change to=> local all all md5
```

* You make change in config file, So once restart you postgres
```
$sudo /etc/init.d/postgresql restart * Restarting PostgreSQL 9.1 database server
```
