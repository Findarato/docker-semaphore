Role Name
=========

docker-semaphore

Requirements
------------

Just basic docker support and have it installed

Role Variables
--------------

```bash

docker_smokeping_storage: /docker/containers/

# Default Enviornmental Variables
docker_semaphore_db_user: semaphore
docker_semaphore_db_pass: semaphore
docker_semaphore_db_host: mysql # for postgres, change to: postgres
docker_semaphore_db_port: 3306 # change to 5432 for postgres
docker_semaphore_db_dialect: mysql # for postgres, change to: postgres
docker_semaphore_db: semaphore
docker_semaphore_playbook_path: /tmp/semaphore/
docker_semaphore_admin_password: changeme
docker_semaphore_admin_name: admin
docker_semaphore_admin_email: admin@localhost
docker_semaphore_admin: admin
docker_semaphore_access_key_encryption: gs72mPntFATGJs9qK0pQ0rKtfidlexiMjYCH9gWKhTU=
docker_semaphore_ldap_activated: 'no' # if you wish to use ldap, set to: 'yes' 
docker_semaphore_ldap_host: dc01.local.example.com
docker_semaphore_ldap_port: '636'
docker_semaphore_ldap_needtls: 'yes'
docker_semaphore_ldap_dn_bind: 'uid=bind_user,cn=users,cn=accounts,dc=local,dc=shiftsystems,dc=net'
docker_semaphore_ldap_password: 'ldap_bind_account_password'
docker_semaphore_ldap_dn_search: 'dc=local,dc=example,dc=com'
docker_semaphore_ldap_search_filter: "(\u0026(uid=%s)(memberOf=cn=ipausers,cn=groups,cn=accounts,dc=local,dc=example,dc=com))"

```

Dependencies
------------

Nothing so far

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

- hosts: watching
  roles:
      - role: findarato.docker-semaphore
        tags: [ semaphore ]

License
-------

GPL-3
