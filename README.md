Ansible Role: GENERIC
=========

- [ ] Write something like `Installs and configures GENERIC.`
- [ ] Delete how to use this project

This is a GENERIC ansible role that by forking you get 

1. built in testing
  - integration tests
  - travis script
2. enhanced readme 
  - role variable yaml highlighting
  - example playbook yaml highlighting
  - OS requirement table
3. precreated files 
  - OS variable files
  - import OS variable in main task
  - OS pkg manager setup tasks
  - configuration task
4. consistent YAML
  - Only uses the structured map
  - variable naming format
5. instructions 
  - checkboxes in readme for steps to convert from GENERIC role to something useful
  - all vanilla files are examples that by default won't modify the system

I hope by forking this role

1. It saves the trouble of the next steps after running `ansible-galaxy init ansible-role-GENERIC`
2. It helps standarize ansible roles for maximum OS support
3. It helps standarize ansible roles readme's look
4. The checkboxes in the readme will give clearer instructions on best practices and rapid development

Requirements
------------

- [ ] Delete unsupported rows from this table 
  - **EX**: Does not support all system's, delete `* | * | * | LTS+`
- [ ] Delete redundant rows
  - **EX**: Supports all Linux, delete all Linux rows except `Linux | * | * | LTS+`
- [ ] Update the rows with supported OS
  - **EX**: Requires Darwin (Yosemite) 10.9+, update `(Lion) 10.7+` to `(Mavericks) 10.9+`

System | Family | Distribution | Versions
-------|--------|--------------|---------:
* | * | * | LTS+
Darwin | * | * | (Lion) 10.7+
FreeBSD | * | * | 8.4+
Linux | * | * | LTS+
Linux | Debian | * | LTS+
Linux | RedHat | * | LTS+
Linux | Suse | * | LTS+

<!---

@TODO: Determine values/feasability/interest of these

AIX | * | * | LTS+
HP-UX | * | * | LTS+
Linux | Alpine | * | LTS+
Linux | Archlinux | * | N/A
Linux | Debian | Debian | (Wheezy) 7+
Linux | Debian | Raspbian | ???
Linux | Debian | Ubuntu | (Precise) 12.04+
Linux | Gentoo | * | N/A
Linux | Gentoo | Funtoo | N/A
Linux | Gentoo | Gentoo | N/A
Linux | Mandrake | * | LTS+
Linux | Mandrake | Mandrake | ???
Linux | Mandrake | Mandriva | ???
Linux | OpenWrt | * | * 
Linux | OtherLinux | * | * 
Linux | RedHat | Amazon | ???
Linux | RedHat | Ascendos | ???
Linux | RedHat | Centos | 6.0+ 
Linux | RedHat | CloudLinux | ???
Linux | RedHat | Fedora | 20+
Linux | RedHat | OEL | ???
Linux | RedHat | OracleLinux | ???
Linux | RedHat | OVS | ???
Linux | RedHat | PSBM | ???
Linux | RedHat | RedHat | 6.0+ 
Linux | RedHat | Scientific | ???
Linux | RedHat | SLC | ???
Linux | RedHat | XenServer | ???
Linux | Suse | openSUSE | 11.4+
Linux | Suse | SLED | ???
Linux | Suse | SLES | 11.1+
OpenBSD | OpenBSD | OpenBSD | LTS+
??? | Solaris | * | LTS+
??? | Solaris | OmniOS | ???
??? | Solaris | OpenIndiana | ???
??? | Solaris | Nexenta | ???
??? | Solaris | Solaris | ???
??? | Solaris | SmartOS | ???
??? | VMwareESX | * | LTS+

-->

Role Variables
--------------

- [ ] Update with your variables
- [ ] Updates comments in same style

```yaml
GENERIC_setting_var: "val" # Short inline comment for settings

# Cross-OS default settings
GENERIC_pkg_cache_time: 86400
GENERIC_pkg_cache_update: Yes
GENERIC_dir_tmp_download: /tmp
GENERIC_dir_src_download: /usr/local/src

# OS settings; Overwridde OS vars files by setting these
GENERIC_pkg_names: []
GENERIC_pkg_urls: []
GENERIC_dir_install: ""
```

Dependencies
------------

- [ ] If you can use Ansible Galaxy, list out roles
- [ ] If you have to use GitHub, instructions of what to clone
- [ ] Else, write `None`

None

Example Playbook
----------------

- [ ] Update basic playbook
- [ ] Update playbook with variables
- [ ] Create additional example playbooks when variables can branch

Basic playbook

```yaml
- hosts: servers
  roles:
     - role: ansible-role-GENERIC
```

Playbook using settings

```yaml
- hosts: servers
  roles:
     - role: ansible-role-GENERIC
	   GENERIC_setting_var: "custom value"
```

License
-------

BSD

Author Information
------------------

- [ ] Put in your name
- [ ] Global replace of word `GENERIC` with your role name
- [ ] When completed all checkboxes in readme, delete all checkboxes in readme 

Lastname Firstname
