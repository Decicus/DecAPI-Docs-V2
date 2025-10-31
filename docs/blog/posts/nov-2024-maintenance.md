---
date: 2024-11-22
slug: nov-2024-maintenance
categories:
    - General announcements
tags:
    - maintenance
    - infrastructure
---

# Maintenance & Infrastructure Changes - November 2024

There will be some maintenance and infrastructure upgrades to DecAPI, at some point in the near-ish future.
There's no set date yet, as it honestly depends on when I have the time. Might happen this Sunday (November 24th), might be a week or two from now.

Assuming I have configured things properly, there should be minimal downtime (a few minutes), but I've been doing this for long enough to know that anything can happen in these cases.  
Of course, I will be doing some testing beforehand to make sure everything works as expected. This testing will not affect the live version of DecAPI.

Once the maintenance is happening, updates will be posted in the [Discord server](https://decapi.link/discord) in the `#announcements` channel and on [Bluesky](https://bsky.app/profile/decapi.me).

A more technical explanation can be found below.

----

As listed on the [server setup page](../../server-setup.md#server-hosting), DecAPI effectively runs on 4 servers total.
3 for the actual DecAPI application and a single server for the database and cache (Redis). So far, that database / cache server has been very reliable. No extended downtime has been caused due to that server specifically going down.
However, since it is a single server, it's also a single point of failure. If that server goes down, DecAPI goes down completely until that server comes back up.

The infrastructure upgrades will go from 1 database / cache server to 3 database / cache servers (a cluster), with their own load balancer.

In the beginning only the database will be migrated to the new cluster. I wanna spend a few days looking at performance to make sure it's all good.
Once the database server has been stable for a while, the cache server will also be pointed to the new cluster.

The plan is essentially this:

- Reduce DecAPI's load balancer to point to only 1 of the application servers. DecAPI might slow down a bit during this time.
- Dump the current database data, import into new database cluster
- Point the 2 leftover application servers to the new database cluster. Run a few test requests to make sure they can connect to the database cluster without issues.
- Put the leftover application servers back behind the load balancer, remove the "old" application server.
- Update the configuration on the "old" application server to point to the new DB cluster.
- Put the "old" (now updated) application server behind the load balancer again, making DecAPI run on 3 application servers as normal.

Surely nothing could go wrong :)