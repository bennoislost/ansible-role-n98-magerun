# Ansible Role: N98-magrun

An Ansible Role that installs the Magento CLI tool N98 Magerun on Linux.

## Role Variables

The below variables can be modified to your playbooks needs or if the PHAR archive url chnages!

```
bennoislost_magerun_enabled: true
bennoislost_magerun_download_url: "http://files.magerun.net/n98-magerun-latest.phar"
bennoislost_magerun_bin_path: "/usr/bin/n98-magerun.phar"

bennoislost_magerun2_enabled: false
bennoislost_magerun2_download_url: "http://files.magerun.net/n98-magerun2-latest.phar"
bennoislost_magerun2_bin_path: "/usr/bin/n98-magerun2.phar"
```

By defualt the Magento2 version of the CLI tool is disabled - this can bee easily changed in your `vars` file.

## Example Playbook & Vars

```
- hosts: webservers
  vars_files:
    - vars/main.yml
  roles:
    - { role: bennoislost.n98-magerun }
```

*Contents of `vars/main.yml`*

```
# Enable Magento2
bennoislost_magerun2_enabled: true
```

## License

MIT

## Thanks To

* The team at Netz98 and all contributors to n98-magerun!