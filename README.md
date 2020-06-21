ansible-role-postfix
=========

Role to setup postfix for froxlor.

Requirements
------------
This role was created for Debian 10.x (Buster). It is configured to work with [froxlor](https://froxlor.org).The role needs a mysql-database and expects a database-schema as it is used by froxlor.
You might use this role in conjunction with the roles:

* ansible-role-apache
* ansible-role-mysql
* ansible-role-froxlor
* ansible-role-dovecot

Role Variables
--------------
In `defaults/main.yaml` the following variables and default-values are specified.

```yaml
froxlor_mysql_user: froxs4
froxlor_mysql_db: froxs4
```

The following variables don't have defaults. You need to specify them either in a file in group_vars, host_vars directory or via command-line.

```yaml
root_mail_address: valid e-mail address you can access
mail_server_fqdn: froxlor_domain
froxlor_mysql_password: the froxlor mysql database password
```

Example Playbook
----------------
This role can be easily used in a playbook like this: 

```yaml
- hosts: froxlor-servers
  roles:
      - ansible-role-postfix
```

License
-------
GNU GENERAL PUBLIC LICENSE VERSION 3

Author Information
------------------
[blog.retter.jetzt](https://blog.retter.jetzt)
