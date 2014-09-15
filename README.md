# PostgreSQL role for Ansible

Installs/configures the specified version of PostgreSQL and creates the specified list of databases.

## Requirements

Tested on Ubuntu 12.04 Server.

## Role Variables

The default variables are as follows:

    postgres_version: '9.3'
    postgres_username: 'postgres'
    postgres_password: 'postgres'
    postgres_databases:
      - 'my_postgres_db'
      - 'my_other_postgres_db'
    locale: 'en_AU'
    encoding: 'UTF-8'
    locale_language_packs:
      - 'language-pack-en'
      - 'language-pack-en-base'

## Dependencies

[Locales](https://github.com/ssilab/ansible-locales)

## Example Playbook

    - hosts: 'servers'
      roles:
        - role: 'ssilab.postgres'
          postgres_version: '9.3'
          postgres_databases:
            - 'my_app_db'


# License

This playbook is provided 'as-is' under the conditions of the BSD license. No fitness for purpose is guaranteed or implied.