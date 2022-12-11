---
title: Recon-ng
layout: default
---

# Recon-ng
Open Source Intelligence gathering tool aimed at reducing the time spent harvesting information from open sources.

Detailed information [here](https://github.com/lanmaster53/recon-ng/wiki)

# Techniques covered
- Technical Information Gathering
    - T1250 Determine domain and IP address space
    - T1261 Enumerate externally facing software applications, technologies, languages, and dependencies
- People Information Gathering
    - T1271 Identify personnel with an authority/privilege

# Basic Usage
There are 2 contexts in recon-ng - global and module.
recon-ng works in interactive mode. General flow of using recon-ng is to populate some table with seed data and use modules from marketplace to transform and enrich data in all tables. You can always type help to see general commands.

```shell
> help workspaces
# create workspace for target
> workspaces create pluralsight
# data and configuration is seggregated for all workspaces
> help options
# check list of available options
> options list
# we need to provide seed data to perform other transformations
> help db
# insert data into companies table
> db insert companies
> show companies
# transform data into something useful
# modules can be installed from marketplace
> help marketplace
# show all modules
> marketplace search
# some modules may have dependencies which need to be manually installed
> marketplace search companies-
> marketplace install recon/companies-multi/whois_miner
# list installed modules
> modules search
# load module - pattern matches name from installed modules
> modules load miner
> help
> options list
# run the module
> run
# view data filled by running module
> show locations
> show netblocks
> show contacts
# expanding dataset
> db insert domains
> show domains
# exit module context
> back
# search modules that can transform previously fetched contacts
> marketplace search contacts-
> marketplace install hibp
> modules load hibp
# be specific when loading when multiple modules has same name
> modules load recon/contacts-credentials/hibp_breach
# Note: You need to configure hibp api key before running this module
> run
# view breached credentials for contacts
> show credentials
# you can also query table directly
> db query select * from credentials
> exit
```

You can also use recon-web for web interface. Web interface can be used to analyze, clean and export data fetched from previous steps.
```
recon-web --host 0.0.0.0
```