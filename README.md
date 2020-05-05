# About this repository 

This repository has Ansible playbooks examples to automate Arista EOS. 

# Playbooks description

The playbooks are at the root of this repository. The playbooks name is playbook_*.yaml.

- [playbook_parse_command.yml](playbook_parse_command.yml) shows how to collect a `show command` and parses it
- [playbook_enable_http_api.yml](playbook_enable_http_api.yml) uses SSH to enable eAPI 
- [playbook_configure.yml](playbook_configure.yml) generates the EOS configuration files [conf_generated](outputs/conf_generated) from the template [config.j2](templates/config.j2) and loads the configuration generated on the EOS devices. It is used to configure the [lab](#network-topology) 
- [playbook_collect_commands.yml](playbook_collect_commands.yml) collects the EOS `show commands` defined in the file [audit.yml](group_vars/eos/audit.yml) and save the output in the directory [cli](outputs/cli)
- [playbook_generate_audit_report.yml](playbook_generate_audit_report.yml) audits the devices and generates this [report](outputs/audit/report.md). It is used to audit the [lab](#network-topology) 
- [playbook_validate_states.yml](playbook_validate_states.yml) validates the devices states. It is used to validate the [lab](#network-topology) 
- [playbook_backup_configuration.yml](playbook_backup_configuration.yml) backups the running configuration in the directory [backup](outputs/backup) 
- [playbook_collect_facts_config.yml](playbook_collect_facts_config.yml) 
backups the running configuration in the directory [running_config](outputs/facts/running_config) 
- [playbook_collect_facts_hardware.yml](playbook_collect_facts_hardware.yml) collects the hardware facts and saves them in the directory [hardware](outputs/facts/hardware) 
- [playbook_collect_facts_resources.yml](playbook_collect_facts_resources.yml) collects some resources facts and saves them in the directory [resources](outputs/facts/resources)  
- [playbook_manage_vlans.yml](playbook_manage_vlans.yml) manages VLANs and L2 interfaces in a declarative way. 
- [playbook_configure_lines.yml](playbook_configure_lines.yml) shows how you can configure a device with a set of commands.  

# Repository structure 

- The playbooks are at the root of this repository. The playbooks name is playbook_*.yaml.  
- The inventory file is [inventory.ini](inventory.ini)
- The variables are defined in the [host_vars](host_vars) and [group_vars](group_vars) directories 
- The directory [templates](templates) has the jinja templates used by the playbooks 
- The directory [roles](roles) has the roles used by the playbooks
- The directory [outputs](outputs) has the playbooks output 
- The requirements file is [requirements.txt](requirements.txt)
- The Ansible config file is [ansible.cfg](ansible.cfg)
  
# Network topology

3 EOS devices connected in a triangle topology and configured with EBGP   

![topology.png](topology.png)
