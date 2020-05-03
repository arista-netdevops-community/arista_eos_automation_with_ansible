# About this repository 

This repository has Ansible playbooks examples to automate Arista EOS. 

# Network topology

3 EOS devices connected in a triangle topology and configured with EBGP   

![topology.png](topology.png)

# Playbooks description

- [playbook_configure.yml](playbook_configure.yml) generates the EOS configuration files [conf_generated](outputs/conf_generated) from the template [config.j2](templates/config.j2) and load the configuration generated on the EOS devices.  
- [playbook_collect_commands.yml](playbook_collect_commands.yml) collects the EOS `show commands` defined in the file [audit.yml](group_vars/eos/audit.yml) and save the output in the directory [cli](outputs/cli)
- [playbook_generate_audit_report.yml](playbook_generate_audit_report.yml) audits the devices and generate this [report](outputs/audit/report.md)
- [playbook_validate_states.yml](playbook_validate_states.yml) validates the devices states


# Repository structure 

- The requirements file is [requirements.txt](requirements.txt)
- The Ansible config file is [ansible.cfg](ansible.cfg)
- The directory [templates](templates) has the jinja templates used by the playbooks
- The directory [outputs](outputs) has the playbooks output
- The directory [roles](roles) has the roles used by the playbooks
- The inventory file is [inventory.ini](inventory.ini)
- The variables are defined in the [host_vars](host_vars) and [group_vars](group_vars) directories 
- The playbooks are at the root of this repository. The playbooks name is playbook_*.yaml.  
  
