# validat0rs/ansible-thorchain-kubernetes-cluster

An Ansible playbook for configuring a new kubernetes cluster worker for THORChain.

## Prerequisites

- [Python3](https://realpython.com/installing-python)
- [Ansible](https://docs.ansible.com/ansible/latest/installation_guide/intro_installation.html)

_Ideally ansible should be installed via [pip](https://pip.pypa.io/en/stable/), the package installer for python._

## Assumptions

This README assumes that you've already installed `ubuntu` onto the target environment/s.

## Setup

1. Rename the `hosts.example` file in `inventory/` to `hosts`:

```console
cp inventory/hosts.example inventory/hosts
```

2. Install the required git submodule dependencies:

```console
git submodule update --init
```

3. Install the ansible `community.general` and `kubernetes.core` collections:

```console
ansible-galaxy collection install community.general kubernetes.core
```

## Types

The following types are supported:

- [Worker](WORKER.md)
