# azure_lab

1. Create Web App using frameworks=dotnetcore can not fix

2. Using azure.azure_preview_modules fix "Create database elastic pool". {Fix 2019/10/05}

[root@jenkins ~/Project/azure_lab]
# ansible-playbook playbook/infra/bsw/infra.yaml

PLAY [Build BSW in Azure] ***************************************************************************************************************************************

TASK [Gathering Facts] ******************************************************************************************************************************************
ok: [localhost]

TASK [bsw : include_tasks] **************************************************************************************************************************************
included: /root/Project/azure_lab/roles/infra/bsw/tasks/common/infra.yaml for localhost

TASK [bsw : Create resource group] ******************************************************************************************************************************
changed: [localhost]

TASK [bsw : Create Web App] *************************************************************************************************************************************
changed: [localhost] => (item={'server_name': 'prod-server', 'frameworks_name': 'net_framework', 'version': '4.7'})
changed: [localhost] => (item={'server_name': 'prod-admin', 'frameworks_name': 'net_framework', 'version': '4.7'})

TASK [bsw : Create MS-SQL DB] ***********************************************************************************************************************************
 [WARNING]: Azure API profile latest does not define an entry for SqlManagementClient

changed: [localhost]

TASK [bsw : Create database elastic pool] ***********************************************************************************************************************
changed: [localhost]

TASK [bsw : Create SQL Database] ********************************************************************************************************************************
changed: [localhost]

PLAY RECAP ******************************************************************************************************************************************************
localhost                  : ok=7    changed=5    unreachable=0    failed=0    skipped=0    rescued=0    ignored=0

[root@jenkins ~/Project/azure_lab]