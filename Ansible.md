# Ansible Commands

This document provides a list of useful Ansible commands for automating configuration management.

## Ansible Ad-Hoc Commands

### `ansible <host> -m <module>`
- Runs a module on the specified host or group of hosts.

### `ansible <host> -m ping`
- Pings a host to check if it is reachable.

### `ansible <host> -m command -a "<command>"`
- Executes a command on the remote host.

### `ansible <host> -m shell -a "<command>"`
- Executes a shell command on the remote host.

### `ansible <host> -m copy -a "src=<src> dest=<dest>"`
- Copies files to remote hosts.

### `ansible <host> -m user -a "name=<username> state=present"`
- Manages user accounts on remote hosts.

### `ansible <host> -m file -a "path=<path> mode=<mode>"`
- Manages files and their attributes on remote hosts.

### `ansible <host> -m apt -a "name=<package_name> state=present"`
- Manages packages using the APT package manager.

### `ansible <host> -m yum -a "name=<package_name> state=present"`
- Manages packages using the YUM package manager.

## Ansible Playbook Commands

### `ansible-playbook <playbook.yml>`
- Runs an Ansible playbook.

### `ansible-playbook <playbook.yml> --check`
- Performs a dry-run of the playbook (no changes are made).

### `ansible-playbook <playbook.yml> --diff`
- Shows the difference between the current state and the desired state when making changes.

### `ansible-playbook <playbook.yml> --ask-become-pass`
- Prompts for privilege escalation password (e.g., `sudo` password).

### `ansible-playbook <playbook.yml> --tags <tag_name>`
- Executes only tasks with the specified tag.

### `ansible-playbook <playbook.yml> --skip-tags <tag_name>`
- Skips tasks with the specified tag.

### `ansible-playbook <playbook.yml> --limit <host>`
- Restricts playbook execution to a specific host or group.

### `ansible-playbook <playbook.yml> --start-at-task="<task_name>"`
- Starts the playbook from the specified task.

### `ansible-playbook <playbook.yml> -i <inventory_file>`
- Specifies a custom inventory file for the playbook.

## Ansible Inventory Commands

### `ansible-inventory --list`
- Displays the current inventory in JSON format.

### `ansible-inventory --host <hostname>`
- Displays details about a specific host in the inventory.

### `ansible-inventory -i <inventory_file> --graph`
- Displays the inventory structure as a graph.

### `ansible-inventory -i <inventory_file> --yaml`
- Displays the inventory in YAML format.

## Ansible Configuration and Setup

### `ansible-config list`
- Lists all configuration options available in Ansible.

### `ansible-config dump`
- Displays the current configuration in YAML format.

### `ansible-playbook --help`
- Displays help for running Ansible playbooks.

### `ansible --help`
- Displays general help for Ansible commands.

### `ansible-playbook --help`
- Displays help for running Ansible playbooks with various options.

### `ansible-galaxy <command>`
- Manages roles and collections from Ansible Galaxy (e.g., installing or creating roles).

### `ansible-pull -U <repository_url>`
- Pulls a playbook from a Git repository and executes it on the local machine.

## Ansible Role and Collection Management

### `ansible-galaxy install <role_name>`
- Installs a role from Ansible Galaxy.

### `ansible-galaxy install <role_name>,<version>`
- Installs a specific version of a role.

### `ansible-galaxy init <role_name>`
- Initializes a new role with a standard directory structure.

### `ansible-galaxy collection install <collection_name>`
- Installs an Ansible collection.

### `ansible-galaxy collection init <collection_name>`
- Initializes a new collection.

### `ansible-galaxy remove <role_name>`
- Removes a role from Ansible Galaxy.

### `ansible-galaxy collection remove <collection_name>`
- Removes a collection from Ansible Galaxy.

## Ansible Debugging and Output

### `ansible-playbook <playbook.yml> -v`
- Increases verbosity (use `-vv`, `-vvv`, etc., for more detailed output).

### `ansible-playbook <playbook.yml> --extra-vars "<var_name>=<value>"`
- Passes extra variables to the playbook.

### `ansible-playbook <playbook.yml> --diff`
- Shows differences between the current and desired state when running the playbook.

### `ansible-playbook <playbook.yml> --start-at-task="<task_name>"`
- Skips to a specific task in the playbook.

## Ansible Vault Commands

### `ansible-vault create <filename>`
- Creates a new encrypted file using Ansible Vault.

### `ansible-vault edit <filename>`
- Edits an encrypted file with Ansible Vault.

### `ansible-vault encrypt <filename>`
- Encrypts a file with Ansible Vault.

### `ansible-vault decrypt <filename>`
- Decrypts a file encrypted by Ansible Vault.

### `ansible-vault rekey <filename>`
- Changes the password for an encrypted file.

### `ansible-vault view <filename>`
- Displays the contents of an encrypted file.

### `ansible-playbook <playbook.yml> --ask-vault-pass`
- Prompts for the password to decrypt encrypted files during playbook execution.

### `ansible-playbook <playbook.yml> --vault-password-file <file>`
- Uses a file to provide the password for encrypted files during playbook execution.

## Ansible Facts

### `ansible <host> -m setup`
- Gathers facts (system information) from a remote host.

### `ansible <host> -m setup -a "filter=<fact_name>"`
- Gathers a specific fact from a remote host.

### `ansible <host> -m setup -a "gather_subset=<subset>"`
- Gathers a subset of facts (e.g., `network`, `hardware`).

## Other Useful Commands

### `ansible-pull -U <repository_url> <playbook.yml>`
- Pulls a playbook from a Git repository and runs it locally.

### `ansible-playbook <playbook.yml> --tags <tag_name>`
- Runs only the tasks with the specified tag.

### `ansible-playbook <playbook.yml> --skip-tags <tag_name>`
- Skips tasks with the specified tag.
