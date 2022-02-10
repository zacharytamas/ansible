# `zacharytamas`' personal ansible playbook

This is an evolving Ansible playbook for setting up and maintaining consistency between my
different machines.

It is likely not much use as-is for anyone else since it is obviously very personal but
some inspiration may be gleaned from it, I guess.

## Usage

```shell
$ ./run.sh
```

It will ask for a `BECOME` password, which is the password for your OS user. Certain tasks
in the playbook, such as ones which change shell settings, require elevated permissions.
