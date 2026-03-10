This example shows how to request a specific sdf filesystem to be mounted into your pod.

We utilise different storageClasses to represent a specific sdf filesystem. This allows us stronger control over which filesystems can be mounted on specific vclusters and thus provides protection between facilities as each vcluster can only mount predefined (and approved) filesystems.

Please note that the supported
[accessModes](https://github.com/slaclab/slac-k8s-examples/blob/main/basic/storage/sdf-filesystem/pvc.yaml#L6-L7)
for `/sdf/group/<facility>` and `/sdf/data/<facility>` StorageClasses are
limited to `ReadWriteMany` or `ReadOnlyMany`
