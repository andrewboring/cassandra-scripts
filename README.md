# cassandra-scripts
Simple Cassandra backup script to object storage.
The intent is to illustrate how a "management" console might create
a daily container in Swift object storage, use parallel-ssh to connect 
to multiple Cassandra nodes, run nodetool(1) to dump the keyspace, 
and then copy those files to the container.

Requires parallel-ssh: https://code.google.com/archive/p/parallel-ssh/
Requires python-swiftclient CLI: http://docs.openstack.org/cli-reference/common/cli_install_openstack_command_line_clients.html

Note: this is a very simple demo script, demo'ed in Virtualbox with 
two Cassandra nodes and one SwiftStack node (using the hosted controller).
There is no real error checking as this is not intended to be used
in a production environment.
