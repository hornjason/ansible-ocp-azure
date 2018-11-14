Role Name
=========
azure_cloud_provider
    Role which defines the azure related variables.

Role Variables
--------------
    # Service principal name.
    sp_name: "css-azure-admin"

Example Playbook
----------------
    - hosts: localhost
      roles:
        - { role: azure_cloud_provider }
