# AGOL Inventory Tool - Usage

This is a brief overview of options for running this tool.  If you need a high-level overview of what this tool does, refer to [this post](https://dancranford.github.io/2020/06/10/agol-inventory-tool-1.html).

1. TOC
{:toc}


## Basic Requirements

This tool runs in a Python environment.  The biggest dependency is the **ArcGIS API for Python**.  If you have an installation of ArcGIS Pro on your computer, you'll already have this.  Alternatively, you can create a new Python environment and install the ArcGIS API via **conda**.  [Here's a reference for that](https://developers.arcgis.com/python/guide/install-and-set-up/).  Alternatively, there is a new online notebook option that we will discuss below.

{% include alert.html text="An administrator role login is recommended but not required.  This tool can only view users, groups, or items that your login can view.  So if you have an administrative login, you'll be able to see more than a standard user login." %}


## Download the code
No matter how you choose to run this tool, you'll need to download or clone the github repository [located here](https://github.com/DanCranford/agol-inventory).

Here's some information on [cloning a repository](https://help.github.com/en/github/creating-cloning-and-archiving-repositories/cloning-a-repository)


## Local Python Environment

This approach will work with a local Python environment (either via ArcGIS Pro or conda install).

Once you've cloned or downloaded and unzipped the repository from the link above, you can open the **org_scanner** as either a script (.py) or a Jupyter Notebook (.ipynb).


## Basic Tool Usage

When you start the tool, you'll be asked for credentials.  The tool will prompt you for a URL, Username, and Password.  For information on how to enter this information for ArcGIS Online or ArcGIS Portal, [review this information](https://developers.arcgis.com/python/guide/working-with-different-authentication-schemes/).

After you've set up your login, the tool will scan your organization or portal for the following:
- all available groups
- all available users
- all available items

Once the tool has gathered this information, you can choose to export to SQLITE or excel.  The tool will export to SQLITE by default and will create several database views that provide extra insight into the relationships between your items, users, and groups.

{% include info.html text="SQLITE databases can be opened in ArcGIS Pro or in any SQLITE interface (such as SQLITE Studio or DB Browser)" %}

## Results

The simplest product of this tool includes tables (or sheets in the case of an excel output) that document the following:
- **USERS** - an inventory of all users
- **GROUPS** - an inventory of all groups
- **GROUP_MEMBERSHIP** - join table showing which users are in which groups
- **WEB_MAPS** - inventory of all Web Map items
- **FEATURE_SERVICES** - inventory of all feature services.  This table will also show source item for hosted feature views.
- **WEB_APPS** - inventory of Web Mapping Applications
- **OTHER_ITEMS** - all other items including Survey123 forms, dashboards, etc.
- **MAP_FS_REL** - Join table showing each layer in each web map and its source data
- **TAGS** - item tags - one-to-many with all items.  
- **CATEGORIES** - item categories - one-to-many with all items.

If you opt for a SQLITE output, the tool will create the following additional views:
- **USERS_VIEW** - user info showing number of days since last login
- **GROUPS_ZEROMEMBERS** - standing view of groups with no members.  
- **STORAGE_ESTIMATE** - rough estimate of hosted feature storage credit usage based on file size.  *This is just an estimate and is usually within 5% of real storage costs*.
- **ALL_ITEMS** - union of all items including web maps, web apps, feature services, and other
