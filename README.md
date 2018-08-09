Check_mk local check check_galera_cluster
=======================================

A Check_mk local check to check status of a galera cluster

Based on https://github.com/fridim/nagios-plugin-check_galera_cluster Version 1.1.4
    Author Alessandro Dolci <dolci.alessandro94@gmail.com>, Guillaume Coré <fridim@onfi.re>, Ales Nosek <ales.nosek@gmail.com>, Staf Wagemakers <staf@wagemakers.be>

This single script will print 4 local checks for:
1. Overall status of Galera cluster
2. Number of connected nodes to the cluster, checking also in the past
3. Check of wsrep_flow_control_paused
4. Check if primary node

## INSTALLATION
1. Put the script on your galera cluster nodes under local checks directory ($MK_LIBDIR/local/).
2. Edit it with custom thresholds.
3. Give read and execute permission for check_mk_agent user (default root)
4. Install mysql and bc commands (mysql-client is usually installed as dependency for mysql-server and mariadb-server)
5. Rerun service inventory from your check_mk server.
