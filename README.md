# Carebot Interview Homework


## Questions

- How did you test it? What was your development environment?

Running the playbook with check option to test the playbooks 
`ansible-playbook -i inventory/hosts.yaml --connection=local --check playbooks/docker.yaml`

- How would you proceed if you needed to deploy second, identical server?

To deploy again, we could add the server to the list of hosts in the inventory and rerun the playbook.