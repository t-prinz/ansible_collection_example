## Sample playbook to execute a collection store in an Ansible Private Automation Hub instance

The ansible.cfg file needs to be modified to reference the private automation hub.  As an example

[galaxy]
server_list = private_automation_hub

[galaxy_server.private_automation_hub]
url=https://private-automation-hub-server/api/galaxy/content/published/
token=abc123

`ansible-galaxy collection install -r collections/requirements.yml`
