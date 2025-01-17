
# Percona XtraBackup - Documentation

!!! note ""

    This documentation is for the latest release: Percona XtraBackup {{release}} ([Release Notes](release-notes/8.0/{{release}}.0.md)).

*Percona XtraBackup* is an open source hot backup utility, for
*MySQL* - based servers, that keeps your database fully available during planned maintenance windows.

Whether it is a 24x7 highly loaded server or a low-transaction-volume
environment, *Percona XtraBackup* is designed to make backups a seamless
procedure without disrupting the performance of the server in a production
environment. Percona XtraBackup (PXB) is a 100% open source backup solution with a [commercial support](https://www.percona.com/mysql-support/) available for organizations who want to benefit from comprehensive, responsive, and cost-flexible database support for MySQL.

### Supported storage engines

*Percona XtraBackup* can back up data from *InnoDB*, *XtraDB*,
*MyISAM*, and MyRocks tables on *MySQL* 8.0 servers as well as *Percona Server for MySQL*
with *XtraDB*, [*Percona Server for MySQL* 8.0](https://docs.percona.com/percona-server/8.0/), and [*Percona XtraDB Cluster* 8.0](https://docs.percona.com/percona-xtradb-cluster/8.0/).

!!! admonition "Version updates"
   
    Version 8.0.6 and later supports the MyRocks storage engine. 
    An incremental backup on the MyRocks storage engine does not 
    determine if an earlier full or incremental backup 
    contains the same files. **Percona XtraBackup** copies all 
    MyRocks files each time it takes a backup.
    **Percona XtraBackup** does not support the TokuDB storage engine. Find more information in [Percona TokuBackup](https://docs.percona.com/percona-server/latest/tokudb/toku_backup.html). 

### Limitations

*Percona XtraBackup* 8.0 does not support making backups of databases
created in versions prior to 8.0 of *MySQL*, *Percona Server for MySQL* or
*Percona XtraDB Cluster*. As the changes that *MySQL* 8.0 introduced
in *data dictionaries*, *redo log* and *undo log* are incompatible
with previous versions, it is currently impossible for *Percona XtraBackup* 8.0 to also support versions prior to 8.0.

Due to changes in MySQL 8.0.20 released by Oracle at the end of April 2020,
*Percona XtraBackup* 8.0, up to version 8.0.11, is not compatible with MySQL version 8.0.20 or
higher, or Percona products that are based on it: Percona Server for MySQL and
Percona XtraDB Cluster.

For more information, see [Percona XtraBackup 8.x and MySQL 8.0.20](https://www.percona.com/blog/2020/04/28/percona-xtrabackup-8-x-and-mysql-8-0-20/)


!!! admonition "Learn more about other Percona products"

    [Percona Distribution for MySQL 8.0](https://docs.percona.com/percona-distribution-for-mysql/8.0/) 
