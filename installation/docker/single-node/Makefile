cert-gen:
	docker compose -f generate-indexer-certs.yml run --rm generator

max_map_count: # change in `/etc/sysctl.conf` to set this value permanently
	sudo sysctl -w vm.max_map_count=262144