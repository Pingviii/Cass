
williamyeh.oracle-java for Ansible Galaxy (edited by Oleh Seniuk olegservice@gmail.com)
============

## Summary

This Ansible role has the following features:

 - Install JDK 8 version.
 - Install for CentOS.
 - Uninstall JDK and Apache Cassandra. (optionally)
 - Install Apache Cassandra.

## Role Variables

### Mandatory variables

None.

### Optional variables


User-configurable defaults:

```yaml
# uninstall java and cassandra?
uninstall: false

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

# which version?
cassandra_version: 3

# which subversion?
cassandra_subversion: 6
```
