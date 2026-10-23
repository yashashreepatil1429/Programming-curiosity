# Rabbit Holes 5–7

## 5. When I upload a photo to Instagram, where does that photo actually go?

The app sends the image and metadata over an authenticated, encrypted connection to Instagram's service. Servers validate permissions and file properties, then may resize or transcode the image and store media in object storage distributed across data centres. Database records connect the media to an account and post, while caches or content-delivery networks serve copies closer to viewers. The exact architecture is private and changes over time; deleting a post may also require cleanup of replicas, caches, and backups according to retention rules.

## 6. How can millions of people use the same application at the same time?

The service runs many instances behind load balancers, so requests can be handled by different machines. Caches and content-delivery networks serve frequently requested data, while databases and queues distribute work and preserve state. The system monitors load and failures, adds capacity where needed, and uses replication or failover to continue when components break. It is not literally one shared program running once: many coordinated processes handle separate requests, and bottlenecks, data consistency, and cost must all be managed.

## 7. What happens if two users try to modify the same database record at exactly the same time?

The database uses a concurrency-control mechanism—such as locks or multiversion concurrency control—to keep operations from corrupting stored data. Depending on the transaction and isolation level, one update may wait, read a prior version, fail with a conflict, or be serialized after the other. The application should detect conflicts and either retry safely or ask a user to resolve competing edits. Without a deliberate strategy, a later write can overwrite an earlier one even though the database remains structurally valid; see [database transactions](../06-databases/transactions.md).
