# `zacharytamas`' personal ansible playbook

This is an evolving Ansible playbook for setting up and maintaining consistency between my
different machines.

It is likely not much use as-is for anyone else since it is obviously very personal but
some inspiration may be gleaned from it, I guess.

## Usage

### Using `ansible-pull`

Ansible comes with a CLI tool called `ansible-pull` which can be used to pull playbooks from external sources and execute them locally. When this happens, it automatically executes the playbook described in the `local.yml` file.

You can use this approach to execute this playbook without cloning it locally, using this command:

```console
$ ansible-pull -U https://github.com/zacharytamas/ansible -K
```

The `-K` flag will ask for your `BECOME` password, which is your Unix user's password.

### If you've cloned the repository locally

```console
$ ./run.sh
```

It will ask for a `BECOME` password, which is the password for your OS user. Certain tasks
in the playbook, such as ones which change shell settings, require elevated permissions.
