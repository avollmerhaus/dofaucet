dofaucet
===

# tl;dr
Read YAML-formatted ansible inventory, create digitalocean droplets accordingly.
Complete with multiple DNS records.
Optionally add droplets to digitalocean "project". 

# example usage
```
dofaucet --token 23234242 --project foo --inventory foo.yml
```

# future ideas

could parse the inventory using ansibles very own functions.
```
from ansible.parsing.dataloader import DataLoader
from ansible.vars.manager import VariableManager
from ansible.inventory.manager import InventoryManager

loader = DataLoader()
inventory = InventoryManager(loader=loader, sources='~/inventory.yml')
variable_manager = VariableManager(loader=loader, inventory=inventory)
```