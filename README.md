ansible-role-hetzner
====================

What does the role do?
----------------------
The role activates the rescue system and reboots the server into the rescue
mode, then it will install OS based on the instruction file and reboot the
server again.

Example usage
-------------

```yml
_inventory_
[hetzner]
server ansible_host=1.2.3.4
```

```yml
_group_vars/hetzner.yml_
partitions:
  - "PART /boot ext3 1G"
  - "PART /     ext4 all"
```

```yml
_site.yml_
- hosts: hetzner
  roles:
    - ansible-role-hetzner
```

Author information
------------------

This role was created by [Betacloud Solutions GmbH](https://betacloud-solutions.de).

License
-------

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at http://www.apache.org/licenses/LICENSE-2.0.

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
