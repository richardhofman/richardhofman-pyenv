richardhofman.pyenv
=========

An Ansible role for installation and basic configuration of `pyenv`, and
installation of specific Python versions.

Requirements
------------

N/A

Role Variables
--------------

`install_virtualenv`: if true, `pyenv-virtualenv` will be installed.
`setup_virtualenvs`: if true, virtualenvs specified in `virtualenvs` will be created.
`virtualenvs`: a list of dictionaries of the form {name: Name_of_vEnv, version: python_version} representing virtualenvs that should be present.
`homedir`: pyenv home directory - by default it is within the user's home directory.
`pyenv_user`: user account to configure for pyenv.
`versions`: list of Python versions to install.
`global_default`: default global Python version to use.

Dependencies
------------

N/A

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: python_servers
      roles:
        - role: richardhofman.pyenv
          homedir: /usr/local/pyenv
          user: apache
          versions:
            - 2.7.3
            - 3.4.3
          global_default: python3.4.3

License
-------

MIT

Author Information
------------------

(c) Richard Hofman, 2017
https://rho.nz