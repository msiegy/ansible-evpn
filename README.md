# ansible-evpn
Another Ansible role for automating EVPN fabrics

### Installation:
- Clone this Repo to your local machine `git clone https://github.com/msiegy/ansible-evpn.git`
- Install required python libraries (consider using venv) `pip install -r requirements.txt`
- Edit the hosts.ini host_vars and main.yml variable files to include your target routers and relevant values.
- The jnja2_fabric playbook will deploy underlay and overlay configs to the routers in your inventory. Use access-vlan_provision to configure switchports.
- Run with `ansible-playbook jnja2_fabric.yml`

#### Directory Structure
```bash
├── ansible.cfg
├── hosts.ini
├── host_vars
│   ├── leaf1.yml
│   ├── leaf2.yml
│   └── spine1.yml
├── jinja2_fabric.yml
├── README.md
├── requirements.txt
├── roles
│   ├── jinja2_leaf
│   │   ├── files
│   │   │   ├── leaf1.cfg
│   │   │   ├── leaf2.cfg
│   │   │   └── leaf3.cfg
│   │   ├── tasks
│   │   │   └── main.yml
│   │   ├── templates
│   │   │   └── leaf.j2
│   │   │   └── VNIs.j2
│   │   └── vars
│   │       └── main.yml
│   └── jinja2_spine
│       ├── files
│       │   └── spine1.cfg
│       ├── tasks
│       │   └── main.yml
│       ├── templates
│       │   └── spine.j2
│       └── vars
│           └── main.yml
```
