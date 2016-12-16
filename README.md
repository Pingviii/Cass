
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
java_uninstall: false

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
