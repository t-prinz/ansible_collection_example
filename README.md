## Use a collection stored in an Ansible Private Automation Hub instance

This assumes that
- The collection has been published to the private automation hub instance in the "published" repository
- The URL and token to access the "published" repository is available.

Once these steps have been completed, carry out the following steps:

1. Configure the ansible.cfg file to reference the private automation hub:

        [galaxy]
        server_list = private_automation_hub
        
        [galaxy_server.private_automation_hub]
        url=https://private-automation-hub-server/api/galaxy/content/published/
        token=abc123

2. Install the collection:

    `ansible-galaxy collection install -r collections/requirements.yml`

3. Test the playbook:

    `ansible-playbook sayhello.yml`
