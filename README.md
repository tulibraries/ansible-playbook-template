# TU Libraries Ansible Playbook Template

This repository will help you generate a new Ansible playbook for a TU Libraries application.

## Generating a  new playbook

Run the `./bin/generate_playbook` command passing in the name of the applicaito this will be a playbook for as a command line argument.

`./bin/generate_playbook some-application`

This will create a new playbook in the `generated` directory named `ansible-playbook-some-application`.

This generated playbook will contain:
* a basic `README.md`
* an `inventory` directory with vagrant, qa, staging, and prod inventories.
* a `roles` directory where external roles will be stored (but not version controlled).
* a `playbook.yml` for composing the main logic for your playbook.
* a `.circleci` directory containing config for running basic tests on the playbook.
* a `requirements.yml` for external roles that will be used by this playbook.
* an `ansible.cfg` file that is common to TU Libraries playbooks
* a `Pipfile` and `.python-version` for python requirements, like the ansible version to use
* a `.gitignore`


For more detail on what that playbook contains, see the [README added as part of the new playbook](templates/README.md) 
