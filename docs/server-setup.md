# Server Setup & Costs

DecAPI is a free service, but that doesn't mean it's free to run.  
Here's a bit of an overview of the infrastructure and its costs to run.

If you wish to help me cover some of the costs of running DecAPI, please check out the ["Support me" page](https://thomassen.sh/support-me/) on my personal website.  
Thanks! :heart:

## Server hosting

DecAPI currently uses [Hetzner Cloud](https://decic.us/hetzner) (:fontawesome-solid-money-bill-1:{ .dollar-bill } referral link) in Ashburn, Virginia, USA.

There are in total 4 CPX11 cloud servers. 3 of them run the application itself, while the last one is for the database and cache (Redis) server.  
In addition to the cloud servers, there's a load balancer which is "managed" by Hetzner. The load balancer distributes any requests to DecAPI to the 3 application servers, depending on which one is least busy and available.

During updates to DecAPI, servers will be removed from the load balancer, updated, and then added back to the load balancer. This way DecAPI can keep running while giving as few error responses to users as possible.

Since I live in Norway 🇳🇴, there's also a 25% VAT added to total cost that I have to pay.

| Server name | Description | Cost per month in Euros (excluding VAT) |
| ----------- | ----------------------- | -------------------------- |
| `WWW-01`    | Application server #1 + Automated backups | €5.12 |
| `WWW-02`    | Application server #2 + Automated backups | €5.12 |
| `WWW-03`    | Application server #3 + Automated backups | €5.12 |
| `DB-01`     | Database & cache server + Automated backups | €5.12 |
| `LB-01`     | Load balancer | €5.39 |
| | **Total (_including_ VAT)** | €25.87 + 25% = **€32.3375** |

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