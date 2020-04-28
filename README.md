# About this repository 

This repository has Ansible playbooks examples to automate Arista EOS. 

# Repository structure 

- The requirements file is [requirements.txt](requirements.txt)
- The Ansible config file is [ansible.cfg](ansible.cfg)
- The directory [templates](templates) has the jinja templates used by the playbooks
- The directory [outputs](outputs) has the playbooks outout
- The inventory file is [inventory.ini](inventory.ini)
- The variables are defined in the [host_vars](host_vars) and [group_vars](group_vars) directories 
- The playbooks are at the root of this repository. The playbooks name is playbook_*.yaml.  

# Description of some playbooks 

- The playbook [playbook_collect_commands.yml](playbook_collect_commands.yml): 
  - runs the EOS `show commands` defined in the file [audit.yml](group_vars/eos/audit.yml)
  - save the output in the directory [cli](outputs/cli)
- The playbook [playbook_generate_audit_report.yml](playbook_generate_audit_report.yml): 
  - collects data from EOS devices and registers the data collected
  - renders the template [audit_report.j2](templates/audit_report.j2) to parse the data registered and to generate this report [report.md](outputs/audit/report.md)
- The playbook [playbook_validate_states.yml](playbook_validate_states.yml): 
  - collects data from EOS devices 
  - parses the data collected (to build the actual state)
  - compares it against the desired state 

# Network topology

3 EOS devices connected in a triangle topology and configured with EBGP   



