ping:
	ansible firefly_main -m ping

indexer_dev:
	ansible-playbook wazuh.yaml -e@vars-dev.yaml -t wazuh_indexer_server

indexer_prod:
	ansible-playbook wazuh.yaml -t wazuh_indexer_server

dry_prod:
	ansible-playbook wazuh.yaml --check --diff

inventory:
	ansible-inventory -i inventory.yaml --list

encrypt:
	ansible-vault encrypt inventory.yaml

edit:
	ansible-vault edit inventory.yaml

decrypt:
	ansible-vault decrypt inventory.yaml
