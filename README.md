
williamyeh.oracle-java for Ansible Galaxy (edited by Oleh Seniuk olegservice@gmail.com)
============

## Summary

This Ansible role has the following features for Oracle JDK:

 - Install JDK 8 version.
 - Install for CentOS.
 - Uninstall JDK.

## Role Variables

### Mandatory variables

None.

### Optional variables


User-configurable defaults:

```yaml
# uninstall?
java_uninstall false

# which version?
java_version: 8

# which subversion?
java_subversion: 112

# which directory to put the download file?
java_download_path: /tmp

# remove temporary downloaded files?
java_remove_download: true

# set $JAVA_HOME?
java_set_javahome: true
```

## Usage


### Step 1: add role

Add role name `williamyeh.oracle-java` to your playbook file.


### Step 2: add variables

Set vars in your playbook file.

Simple example:

```yaml
---
# file: simple-playbook.yml

- hosts: all

  roles:
    - williamyeh.oracle-java

  vars:
    java_version: 8
```


### (Optionally) pre-fetch .rpm and .tar.gz files

For some reasons, you may want to pre-fetch .rpm and .tar.gz files *before the execution of this role*, instead of downloading from Oracle on-the-fly.

To do this, put the file on the `{{ playbook_dir }}/files` directory in advance, and then set the `java_download_from_oracle` variable to `false`:

```yaml
---
# file: prefetch-playbook.yml

- hosts: all

  roles:
    - williamyeh.oracle-java

  vars:
    java_version: 8
    java_download_from_oracle: false
```

