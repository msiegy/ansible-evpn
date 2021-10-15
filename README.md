# ansible-evpn
Automate EVPN fabrics with Ansible

### Installation:
- Clone this Repo to your local machine `git clone https://github.com/msiegy/ansible-evpn.git`
- Install required python libraries (consider using venv) `pip install -r requirements.txt`
- Edit the hosts.ini host_vars and main.yml variable files to include your target routers and relevant values.
- Run with `ansible-playbook jnja2_fabric.yml`

#### Directory Structure
```bash
hosts.ini
ansible.cfg
host_vars
 ── leaf1.yml
 ── leaf2.yml
 ── spine1.yml
roles
├── jinja2_leaf
│   └── tasks
│       └── main.yml
│   └── templates
│       └── leaf.j2
│   └── vars
│       └── main.yml
│   └── files
│       └── leaf1.cfg
│       └── leaf2.cfg
├── jinja2_spine
│   └── tasks
│       └── main.yml
│   └── templates
│       └── spine.j2
│   └── vars
│       └── main.yml
│   └── files
│       └── spine1.cfg
```
