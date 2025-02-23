---
title: MoveTables reversetraffic
series: vtctldclient
---
## vtctldclient MoveTables reversetraffic

Reverse traffic for a MoveTables VReplication workflow.

```
vtctldclient MoveTables reversetraffic
```

### Examples

```
vtctldclient --server localhost:15999 movetables --workflow commerce2customer --target-keyspace customer reversetraffic
```

### Options

```
  -c, --cells strings                          Cells and/or CellAliases to switch traffic in
      --dry-run                                Print the actions that would be taken and report any known errors that would have occurred
      --enable-reverse-replication             Setup replication going back to the original target keyspace to support switching traffic again (default true)
  -h, --help                                   help for reversetraffic
      --max-replication-lag-allowed duration   Allow traffic to be switched only if VReplication lag is below this (default 30s)
      --tablet-types strings                   Tablet types to switch traffic for
      --timeout duration                       Specifies the maximum time to wait, in seconds, for VReplication to catch up on primary tablets. The traffic switch will be cancelled on timeout. (default 30s)
```

### Options inherited from parent commands

```
      --action_timeout duration   timeout for the total command (default 1h0m0s)
      --server string             server to use for connection (required)
      --target-keyspace string    Keyspace where the tables are being moved to and where the workflow exists (required)
```

### SEE ALSO

* [vtctldclient MoveTables](../)	 - Perform commands related to moving tables from a source keyspace to a target keyspace.

