
# Ansible Example Project

This is a hypothetical implementation of an Ansible project to manage a complex, heterogeneous environment.

## Structure

- `environments/`: Contains inventory files for different environments.
- `roles/`: Contains roles for different server types (app1, app2, databases).
- `main.yml`: The main playbook that includes roles based on the target hosts.

## How to Run

1. Navigate to the `environments/dev/` directory and edit the `inventory.ini` file to match your actual server IPs/hostnames.
2. Run the playbook with the following command:

    ```bash
    ansible-playbook -i environments/dev/inventory.ini main.yml
    ```
    

## Multi-Environment Support

This project also includes sample inventories for multiple environments:

- Development (`dev`)
- Pre-Production (`preprod`)
- Qualification (`qualification`)
- Production (`prod`)

To run the playbook for a specific environment, adjust the `-i` flag accordingly:

```bash
ansible-playbook -i environments/[env_name]/inventory.ini main.yml
```
    

## New Roles and Environment-Specific Directives

### Roles

- `mariadb`: Ensures MariaDB is installed and securely configured.
- `nginx`: Configures NGINX for load balancing and SSL.
- `react`: Sets up React for frontend.
- `nestjs`: Sets up NestJS for backend.

### Environment-Specific Directives

- MariaDB is installed and securely configured on hosts under the `databases` group.
- NGINX is installed and configured for load balancing and SSL on hosts under the `load_balancer` group.
- React is used for frontend servers under the `frontend` group.
- NestJS is used for backend servers under the `backend` group.

The inventory files for each environment (`dev`, `preprod`, `qualification`, `prod`) include variables that control these directives.

To run the playbook for a specific environment, use the following command:

```bash
ansible-playbook -i environments/[env_name]/inventory.yml main.yml
```
    

## Areas for Further Study

The `main.yml` playbook includes comments, indications, notes, and TODOs for areas you should explore to deepen your understanding of Ansible and DevOps practices. These areas include:

- Variable Scope and Precedence
- Conditionals and Loops
- Templates and Jinja2
- Roles and Include
- Error Handling
- Ansible Vault
- Dynamic Inventory
- Testing
- CI/CD Integration
- Community Resources

Refer to the `main.yml` playbook for specific tasks and examples to guide your further study.
    

## Step-by-Step Guide and Considerations

### Step 1: Understand the Inventory
- **Consideration**: Learn how the YAML inventory is structured and how to represent different environments.

### Step 2: Explore the Roles
- **Consideration**: Dive into the roles directory to understand the tasks and variables associated with each role.

### Step 3: Run the Playbook in a Test Environment
- **Consideration**: Always test your playbook in a non-production environment first.

### Step 4: Review the Playbook Output
- **Consideration**: Understand what each task is doing and how to interpret the output.

### Step 5: Add Custom Tasks
- **Consideration**: Try adding your own tasks to the playbook for specific customizations.

### Step 6: Use Ansible Vault for Sensitive Data
- **Consideration**: Encrypt sensitive data like passwords and API keys using Ansible Vault.

### Step 7: Dynamic Inventory
- **Consideration**: Learn how to use dynamic inventories for environments that change frequently.

### Step 8: Error Handling and Debugging
- **Consideration**: Add error handling to your playbook and learn how to debug issues.

### Step 9: Testing
- **Consideration**: Use testing tools like Molecule or Ansible Lint to validate your playbook.

### Step 10: CI/CD Integration
- **Consideration**: Integrate Ansible into a CI/CD pipeline for automated deployments.

Refer to the `main.yml` playbook for specific tasks and examples that align with each step.
    