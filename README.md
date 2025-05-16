# Carebot Interview Homework

This repo contains ansible project that installs and configures docker and orthanc server on the target.

Target OS is assumed to be Debian/Ubuntu system. 

## Questions

 > How did you test it? What was your development environment?

Running the playbook with check option to test the playbooks locally.

```bash
ansible-playbook -i inventory/hosts.yaml --check playbooks/docker.yaml
```

```bash
ansible-playbook -i inventory/hosts.yaml --check playbooks/orthanc.yaml
```

To test it on a real machine, I set up a CI/CD pipeline on GitHub to run the playbook on the runner machine. Finally, to manually verify the correctness of the playbook and connectivity to orthanc server, I run the playbooks on a GCP VM instance. 

> How would you proceed if you needed to deploy second, identical server?

To deploy again, we could add the server to the list of hosts in the inventory and rerun the playbooks.