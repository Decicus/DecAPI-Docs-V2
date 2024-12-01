# Server Setup & Costs

DecAPI is a free service, but that doesn't mean it's free to run.  
Here's a bit of an overview of the infrastructure and its costs to run.

If you wish to help me cover some of the costs of running DecAPI, please check out the ["Support me" page](https://thomassen.sh/support-me/) on my personal website.  
Thanks! :heart:

## Server hosting

DecAPI currently uses [Hetzner Cloud](https://decic.us/hetzner) (:fontawesome-solid-money-bill-1:{ .dollar-bill } referral link) in Ashburn, Virginia, USA.

There are in total 6 CPX11 cloud servers. 3 of them run the application itself and another 3 for a database & cache (Redis) cluster.  
In addition to the cloud servers, there are two load balancer which are "managed" by Hetzner.  
The first load balancer (`WWW-LB-01`) distributes any requests to DecAPI to the 3 application servers, depending on which one is least busy and available.  
The second load balancer (`DB-LB-01`) is only for internal communication between the application servers and the database/cache servers, to distribute the load evenly.

During updates to DecAPI, servers will be removed from the load balancer, updated, and then added back to the load balancer. This way DecAPI can keep running while giving as few error responses to users as possible.

Since I live in Norway 🇳🇴, there's also a 25% VAT added to total cost that I have to pay.

| Server name | Description | Cost per month in Euros (including 25% VAT) |
| ----------- | ----------------------- | -------------------------- |
| `WWW-01`    | Application server #1 + Automated backups | €7.36 |
| `WWW-02`    | Application server #2 + Automated backups | €7.36 |
| `WWW-03`    | Application server #3 + Automated backups | €7.36 |
| `DB-02`     | Database & cache server #1 | €6.24 |
| `DB-03`     | Database & cache server #2 | €6.24 |
| `DB-04`     | Database & cache server #3 | €6.24 |
| `WWW-LB-01` | Load balancer for the application servers | €6.74 |
| `DB-LB-01`  | Load balancer for the database & cache cluster | €6.74 |
| | **Total (including 25% VAT)** | €54.28 |

## Domain costs

In addition to the server costs, there's also the yearly costs of the domains.  
Some of them are less necessary than others, but they're fairly cheap in comparison to the monthly recurring server costs.

| Domain name | Description | Cost per year in USD |
| ----------- | ----------- | ------------- |
| `decapi.me` | The primary domain for DecAPI | $14.85 |
| `decapi.net` | Secondary domain, used for unique hostnames for nodes | $10.10 |
| `decapi.dev` | Used for development / testing (not strictly necessary) | $10.79 |
| `decapi.link` | Used for DecAPI-related shortlinks | $7.70 |
| | **Total cost per year** | $43.44 |