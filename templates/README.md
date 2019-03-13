# TU Libraries *PROJECT NAME* Playbook


Note here what this playbook is used for, and the expected infrastructure it runs on.

Go to our Circle-CI Dashboard to have this project's CI running (if the playbook is private; if public, use Travis). Grab the CI status badge for Circle-CI and put at the top of this README.

## Prerequisites

To run this playbook, you need the following in your Ansible run environment first:
- terminal or shell
- package manager knowledge for your system (e.g. homebrew or apt)
- text editor (e.g. vim, atom, whatever you want)
- vagrant (used as an easy route for local testing of Ansible)
- virtualbox (ditto)
- python (preferably 3.7; follow `.python-version` in top level)
- pipenv (you could also use virtualenv locally, but we're sticking with pipenv)
- ansible-vault password file at `$HOME/.vault`.

## Installing Requirements & Starting Shell

Overview: we run `ansible` commands within a `pipenv` shell where our requirements are installed from our playbook's `Pipfile` & `Pipfile.lock`. This helps make our Ansible usage across machines consistent, which then helps with debugging.

To setup the pipenv shell & install required roles for this playbook:
1. git clone the repository locally & `cd` into the root
2. change to the branch that you wish to run or test
3. run `pipenv install`
4. run `pipenv shell`
5. install the required external roles this playbook uses (note: these are no longer captured in the git repository to enforce retrieval of the latest or specified versions in our `requirements.yml`): `ansible-galaxy install -r DIR/required-roles.xml`

If you add new pip dependencies later, use `pipenv install` and `pipenv lock` to track those and add to our shared pipfile.

## Spinning up Local Dev Environment

Instructions on how to run this playbook in an development environment, preferably using Vagrant (for the time being).

## Deploying to Stage, QA, and Production Environments

Instructions on how to manually run this playbook on other environments, and details on any CD pipelines using this workflow.
