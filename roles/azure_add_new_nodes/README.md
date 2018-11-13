Role Name
=========
azure_add_new_nodes

    Add new nodes (master, infra, app) to the existing Azure infra.

Requirements
------------
Assumes this role is run after running the 'azure_infra' role to create the initial cluster.

Role Variables
--------------
    # New Master nodes to be created. Each item in the list is of type 'int' and indicate the 
    # nth number of master node to be created
    new_master_nodes: [] 
    
    # New infra nodes to be created. Each item in the list is of type 'int' and indicate the 
    # nth number of infra node to be created
    new_infra_nodes: []
    
    # New app nodes to be created. Each item in the list is of type 'int' and indicate the 
    # nth number of app node to be created
    new_app_nodes: []

Example Playbook
----------------
    - hosts: localhost
      vars:
        new_app_nodes: [4,5,6]
      roles:
         - { role: azure_add_new_nodes }
