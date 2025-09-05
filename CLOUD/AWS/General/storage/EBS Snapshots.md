
EBS snapshots are point-in-time backups of EBS volume. They can be used for disaster recovery, data migration, volume resizing, and for creating consistent backups of production workloads. EBS snapshots are incremental, so they only save the blocks on the volume that have changed after your most recent snapshot.

EBS snapshots can be used to create multiple new volumes, and new volumes created from a snapshot are an exact copy of the original volume at the time the snapshot was taken. Snapshots of EBS volumes are stored redundantly in multiple Availability Zones using Amazon S3.


### Working with EBS snapshots

In keeping with the AWS shared responsibility model, as the customer, you are responsible for scheduling and managing regular EBS snapshots as part of your backup strategy. This includes monitoring snapshot costs and deleting unnecessary snapshots to avoid excessive charges. You also need to make sure sensitive data within snapshots is encrypted, verify snapshot integrity, and test restoration procedures regularly.

The following illustration shows how EBS snapshots are created from an EBS volume over time. To learn more about how EBS snapshots interact with EBS volumes, choose each of the following three markers.

## Initial snapshot

When you create the first snapshot of an EBS volume, a full copy of all the data on the volume at that point in time is included.

This initial snapshot serves as the baseline and contains all the data blocks that were in use on the volume.

## Subsequent incremental snapshots

For all snapshots after the initial one, only the blocks that have changed since the last snapshot are captured and stored.

These are called _incremental snapshots_. They're much smaller and faster to create than full snapshots.

Each incremental snapshot contains references to the previous snapshots, creating a chain that allows for point-in-time recovery.

## Snapshot consolidation and management

Despite being incremental, each snapshot appears as a full point-in-time copy of your volume.

The relationship between multiple snapshots of the same volume are managed automatically.

When you delete a snapshot, only the data unique to that snapshot is removed. Data referenced by other snapshots is preserved.


## Benefits

Review the main benefits of EBS Snapshots and how it improves your data protection strategy in Amazon EBS.

* Snapshots enable fast data recovery from corruption, accidental deletion, or system failures using point-in-time backups.
* Snapshots enable operations like cross-Region data migration, volume resizing, volume cloning, and sharing data across AWS accounts.
* Snapshots use incremental backup technology, storing only changed blocks after the initial backup, reducing storage costs and backup time.