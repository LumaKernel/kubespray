```sh
# fish
python3 -m venv venv
source ./venv/bin/activate.fish
pip3 install -r requirements.txt
# set IPS ...
CONFIG_FILE=inventory/mycluster/hosts.yaml python3 contrib/inventory_builder/inventory.py $IPS

ansible-playbook -i inventory/mycluster/hosts.yaml  --become --become-user=root cluster.yml
```
