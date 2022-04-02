# odoo-db

Manage Odoo databases from CLI

**Usage:** `odoo-db (list|ls|backup|restore|delete) [Options]`

Use "-h" on list, backup, restore, or delete command to getting spesific help.



## Available Commands

**- List all available database on a server.**

```
Usage: odoo-db (list|ls) -s hostname
List all available database on a server.

Options:
   --source, -s 
        Server's Hostname
```

**- Download a database from server.**

```
Usage: odoo-db backup -s hostname [Options]
Download a database from server.

Options:
   --source, -s 
        Server's Hostname
   --source-name, -sn 
        Server's Database Name
   --local-directory, -ld 
        Directory Where Downloaded Database Stored
```

**- Download a database from server then restore it into destination server.**

```
Usage: odoo-db restore -s hostname -d destination_host -dn database_name [Options]
Download a database from server then restore it into destination server.

Options:
   --source, -s 
        Server's Hostname (or a file)
   --source-name, -sn 
        Server's Database Name (unused when -s is a file)
   --destination, -d 
        Destination Server's Hostname
   --destination-name, -dn 
        Destination Server's Database Name
   --local-directory, -ld 
        Directory Where Downloaded Database Stored (unused when -s is a file)
```

**- Delete a database from server.**

```
Usage: odoo-db delete -s hostname -sn db_name [Options]
Delete a database from server.

Options:
   --source, -s 
        Server's Hostname
   --source-name, -sn 
        Server's Database Name
```

