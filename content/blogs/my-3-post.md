+++
title = 'How to create variable.'
date = 2024-08-17T18:13:50-06:00
draft = false
+++


To create variable. 

```

export DB_USERNAME=dbuser       

export DB_PASSWORD=secretpwdvalue

export DB_NAME=mydb

printenv | grep DB

echo $DB_NAME  "IF YOU WANT TO SEE"

export DB_NAME=NEW-DB-NAME    "To change new name"

if you want to do it permanently you have to use "Vim"

vim .bashrc

"at the bottem" 

export DB_USERNAME=dbuser       

export DB_PASSWORD=secretpwdvalue

export DB_NAME=mydb

esc
:qw

source .bashrc

printenv | grep DB

"if you want to do it for all users" 

vim /etc/environment

Path
```