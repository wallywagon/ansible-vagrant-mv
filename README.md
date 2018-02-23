# Ansible provisioned multi-vendor DC

*topology overview*

![alt text](https://github.com/packetferret/ansible_network_multivendor_02/raw/master/topo.jpg "Topology")

provision via Ansible:

`ansible-playbook all.yml --ask-vault-pass`

(vault password is `password`)

if executing within Ansible container:

*fire up the container in the background*

`docker run -itd -h ansible --name ansible -v $PWD:/home/ packetferret/netdevops`

*execute playbook within container*

`docker exec -it ansible ansible-playbook all.yml --ask-vault-pass`

(vault password is `password`)
