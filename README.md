# zabbix-server-apache-mysql

This role installs zabbix server on a liunx machine.

## Requirements

[GNU C Library](https://www.gnu.org/software/libc/) English language pack is required to have a functioning front-end. [PyMySQL](https://pypi.org/project/pymysql/) is required for database configuration by Ansible.

both of these packages installation is handled by ansible role. but it is good to know the importance of them.

## Role Variables

All the required package and repository lists are placed in var/main.yml. Other parameters such as username, database name, package versions, etc are set in default/main.yml.
In required cases, it is recommended to change parameters with respect to guidelines provided in [zabbix](https://www.zabbix.com/download) official webite.

## Dependencies

None.

## Galaxy

In order to install this role from ansible galaxy you can use command below:

    ansible-galaxy role install masoud-maghsoudi.zabbix-server-apache-mysql

## Example Playbook

It is recommended not to pass any variable to role, instead you can modify package versions in defaults/main.yml with respesct to [zabbix](https://www.zabbix.com/download) official website.

    - hosts: all
      gather_facts: true
      roles:
         - masoud-maghsoudi.zabbix-server-apache-mysql

## License

MIT

## Author Information

| Author | Masoud Maghsoudi                      |
| ------ | ------------------------------------- |
| Email  | masoud_maghsopudi@yahoo.com           |
| Github | <https://github.com/masoud-maghsoudi> |
