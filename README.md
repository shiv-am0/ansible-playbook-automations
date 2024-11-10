# Ansible Playbooks Collection

This repository contains a collection of Ansible playbooks to automate basic server administration tasks. These playbooks cover tasks such as installing/uninstalling packages, creating/deleting files, and managing users. This repository serves as a learning resource for beginners in Ansible and will be updated regularly with more playbooks.

## Table of Contents
- [About the Repository](#about-the-repository)
- [Prerequisites](#prerequisites)
- [Installing Ansible](#installing-ansible)
- [Running the Playbooks](#running-the-playbooks)

---

## About the Repository

This repository includes Ansible playbooks designed for various server administration tasks. The main purpose of this repository is to provide easy-to-follow examples of basic tasks, making it easier for users to understand and implement Ansible automation.

Each playbook is structured to be simple and beginner-friendly, with comments to explain each step.

## Prerequisites

- **Ansible**: Ensure Ansible is installed on your local machine or control node.
- **Inventory File**: Prepare an inventory file (`hosts`) that defines the target servers where the playbooks will be executed. You can define this file in the root of the repository or specify it when running a playbook.
- **SSH Access**: You should have SSH access to the target servers.

## Installing Ansible

For installation instructions, please refer to the [Ansible Documentation](https://docs.ansible.com/ansible/latest/installation_guide/intro_installation.html).

## Running the Playbooks

Each playbook is designed to be run on a target host or group of hosts specified in your inventory file. Here's a basic guide to running the playbooks in this repository:

### Step 1: Define Your Inventory

Create an `inventory` file (or use the one provided in the repository) to list the hosts you want to manage. Here’s an example format:

```ini
[webservers]
server1.example.com
server2.example.com
```

### Step 2: Run a Playbook

To execute a playbook, use the following command:

```bash
ansible-playbook -i inventory playbook_name.yml
```

* `-i inventory`: Specifies the inventory file.
* `playbook_name.yml`: Replace with the name of the playbook you want to run.

If you encounter permission issues, you may need to add `--ask-become-pass` to the command:

```bash
ansible-playbook -i inventory playbook_name.yml --ask-become-pass
```

---

Happy automating with Ansible!