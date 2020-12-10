ASBRL-MYSQL
=========

Deploy a single MySQL node as a Docker container.

Requirements
------------

Need to be Docker engine installed.

Role Variables
--------------

- default_user: 'ubuntu'
- IMAGE: 'mysql'
- BUILD: '8.0'
- PORT: 3306
- BIND_ADDRESS: 0.0.0.0
- ROOT_PASSWORD: 'Pa$$w0rd'
- SERVER_ID: 1
- MAX_CONNETIONS: 200
- KEY_BUFFER_SIZE: '8M'
- INNODB_FILE_PER_TABLE: 1
- INNODB_BUFFER_POOL_INSTANCES: 4 
- INNODB_BUFFER_POOL_SIZE: 256M 
- INNODB_LOG_BUFFER_SIZE: 16M
- INNODB_LOG_FILE_SIZE: 128M
- LOG_OUTPUT: 'TABLE'
- GENERAL_LOG: 0
- GENERAL_LOG_FILE: ''
- SLOW_QUERY_LOG: 0
- SLOW_QUERY_LOG_FILE: ''
- LONG_QUERY_TIME: 5

Dependencies
------------

None

Example Playbook
----------------

      - name: Deploy MySQL
        include_role:
          name: asbrl-mysql
        vars:
          ROOT_PASSWORD: '{{ MYSQL_ROOT_PASSWORD }}'
        tags:
          - asbrl-mysql

License
-------

BSD

Author Information
------------------

Moegui.com