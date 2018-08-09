---
Title: Replacing a node
description: $description
weight: $weight
alwaysopen: false
---
If a node in your cluster is faulty, its status appears as **Down **in
the **Status** column of the **Nodes** page, and in the **Cluster \>
Configuration** page.

![Example of a node
failure](/wp-content/uploads/2014/11/node-failure.png){.alignnone
.size-full .wp-image-25649 width="600" height="152"}

**To replace a faulty node**:

1.  Acquire a new node that is identical to the old node, install and
    configure Redis Enterprise Software on it per the [install
    instructions](/redis-enterprise-documentation/administering/installing-upgrading/downloading-installing/).

    Note: If you are using [Redis on
    Flash](/redis-enterprise-documentation/redis-e-flash/), you must
    make sure the required flash storage is set up on this new node.

2.  Add a new node, as described in [adding a new node to a
    cluster](/redis-enterprise-documentation/administering/cluster-operations/adding-node/).
3.  Make sure the new node has as much available memory as the faulty
    node.
4.  A message appears, informing you that the cluster has a faulty node
    and that the new node will replace the faulty node.
5.  If the new node has insufficient memory, you are prompted to add a
    different node -- one with sufficient memory.

**Note**: If there is a faulty node in the cluster to which you are
adding a node, RP will enforce using the new node to replace the faulty
one.

 

**Note**: If you are using the DNS NS record based connection approach,
the DNS records must be updated each time a node is added or replaced.
For additional details, For more information, refer to the [connection
management
page](/redis-enterprise-documentation/administering/installing-upgrading/configuring/cluster-name-dns-connection-management/).