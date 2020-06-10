# AGOL Inventory Tool - Usage

This is a brief overview of options for running this tool.  If you need a high-level overview of what this tool does, refer to [this post](https://dancranford.github.io/2020/06/10/agol-inventory-tool-1.html).

1. TOC
{:toc}


## Basic Requirements

This tool runs in a Python environment.  The biggest dependency is the **ArcGIS API for Python**.  If you have an installation of ArcGIS Pro on your computer, you'll already have this.  Alternatively, you can create a new Python environment and install the ArcGIS API via **conda**.  [Here's a reference for that](https://developers.arcgis.com/python/guide/install-and-set-up/).  Alternatively, there is a new online notebook option that we will discuss below.

Another soft requirement is that you approach this with an administrative login.  You don't necessarily need that, but this tool can only view users, groups, or items that your login can view.  So if you have an administrative login, you'll be able to see more than a standard user login.

No matter how you choose to run this tool, you'll need to download or clone the github repository [located here](https://github.com/DanCranford/agol-inventory).

## Option 1 - Local Python Environment

This approach will work with a local Python environment (either via ArcGIS Pro or conda install).


