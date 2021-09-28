Deploy
=========

This Ansible is used for deploying your Docker application on a Debian server

Requirements
------------

- SSH access to the server

Role Variables
--------------

If you want to use a differently named docker-compose file, you can change that. The default is docker-compose.yml

```yaml
docker-compose_name:
```

Give the url of the git repo from which needs to be pulled.

```yaml
repository_url:
```

Give the directory where the application needs te be installed on the server. The default is /home/deploy/project

```yaml
project_directory:
```


Dependencies
------------

None.

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

```yaml
#!/usr/bin/env ansible-playbook


- hosts: production
  become: true
  become_flags: "--preserve-env=SSH_AUTH_SOCK"

  roles:
   - geerlingguy.git
   - geerlingguy.docker
   - geerlingguy.nginx
   - skrepr.deploy
```

License
-------

MIT / BSD

Author Information
------------------

This role was created in 2021 by [Jeroen van der Meulen](https://github/jeroenvandermeulen), commisioned by [Skrepr](https://skrepr.com)
