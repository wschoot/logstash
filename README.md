# logstash

```
vagrant destroy -f; \
	ansible-lint playbook.yml && \
	vagrant up && \
	vagrant ssh-config > ~/.ssh/vagrant; \
	vagrant ssh -- -L 5601:localhost:5601; \
	kill $(ps auxf | grep ssh | grep 192.168 | awk '{ print $2 }')
```
