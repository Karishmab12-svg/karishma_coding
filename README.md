
# SRE CHALLENGE
## Instructions to Deploy

1. Ansible playbook to deploy the webserver and config

- New WebServer setup
```
ansible-playbook playbook.yml  --tags setup, deploy --extra-vars="playbook_dir=`pwd`"
```

- Apply the src code changes
```
ansible-playbook playbook.yml  --tags deploy --extra-vars="playbook_dir=`pwd`"
```

### Considerations

1. Created self-signed certificates with url test.kfc.com
2. Deploy directory /var/www/kfc/


### Testing
After code is deployed, below checks will be done against localhost
1. Check and Validate nginx service status
2. Hit the localhost and should get `200` response code
