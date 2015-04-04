Ansible Role: autofs [![Build Status](https://travis-ci.org/cmprescott/ansible-role-autofs.svg?branch=master)](https://travis-ci.org/cmprescott/ansible-role-autofs)
=========

Installs autofs. Manages indirect maps for autofs.

Requirements
------------

System | Family | Distribution | Versions
-------|--------|--------------|---------:
Darwin | * | * | (Mtn Lion) 10.8+
Linux | Debian | * | LTS+
Linux | RedHat | * | LTS+
Linux | Suse | * | LTS+

<!---

@TODO: Determine values/feasability/interest of these

* | * | * | LTS+
AIX | * | * | LTS+
FreeBSD | * | * | 8.4+
HP-UX | * | * | LTS+
Linux | * | * | LTS+
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
autofs_indirect_maps:                              
  - name: "nfs"                                    # Suggest use share type
    path: /mnt/nfs                                 # Suggest use /mnt dir 
    mounts:                                         
      - name: "isos"                               # Suggest match folder url 
        fstype: "nfs,rw,bg,hard,intr,tcp,resvport" # Add NFS options here 
        url: "nfs.server.com:/data/isos"           # Add username/pw here 

# Cross-OS default settings
autofs_pkg_cache_time: 86400
autofs_pkg_cache_update: Yes
autofs_dir_tmp_download: /tmp
autofs_dir_src_download: /usr/local/src

# OS settings; Overwridde OS vars files by setting these
autofs_pkg_names: []
autofs_pkg_urls: []
autofs_dir_install: ""
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
     - role: ansible-role-autofs
```

Playbook using settings

```yaml
- hosts: servers
  roles:
     - role: ansible-role-autofs
	   autofs_setting_var: "custom value"
```

License
-------

BSD

Author Information
------------------

- [ ] Put in your name
- [X] Global replace of word `autofs` with your role name
- [ ] When completed all checkboxes in readme, delete all checkboxes in readme 

Lastname Firstname
