# AGOL Inventory Tool - Usage

This is a brief overview of options for running this tool.  If you need a high-level overview of what this tool does, refer to [this post](https://dancranford.github.io/2020/06/10/agol-inventory-tool-1.html).

1. TOC
{:toc}


## Basic Requirements

This tool runs in a Python environment.  The biggest dependency is the **ArcGIS API for Python**.  If you have an installation of ArcGIS Pro on your computer, you'll already have this.  Alternatively, you can create a new Python environment and install the ArcGIS API via **conda**.  [Here's a reference for that](https://developers.arcgis.com/python/guide/install-and-set-up/).  Alternatively, there is a new online notebook option that we will discuss below.

{% include alert.html text="Another soft requirement is that you approach this with an administrative login.  You don't necessarily need that, but this tool can only view users, groups, or items that your login can view.  So if you have an administrative login, you'll be able to see more than a standard user login." %}


## Download the code
No matter how you choose to run this tool, you'll need to download or clone the github repository [located here](https://github.com/DanCranford/agol-inventory).

Here's some information on [cloning a repository](https://help.github.com/en/github/creating-cloning-and-archiving-repositories/cloning-a-repository)


## Option A - Local Python Environment

This approach will work with a local Python environment (either via ArcGIS Pro or conda install).

Once you've cloned or downloaded and unzipped the repository from the link above, you can open the **org_scanner** as either a script (.py) or a Jupyter Notebook (.ipynb).

## Option B - ArcGIS Notebooks (beta)

If you have access to an ArcGIS Online account with ArcGIS Notebooks, you can choose to run this process in that environment.  The nice thing about this is that you won't need to configure any local python environment as the ArcGIS Notebooks cloud environment has all the dependencies to run this tool.

{% include alert.html text="At the time of this writing, ArcGIS Notebooks for ArcGIS Online is in beta" %}

Once you've cloned or downloaded and unzipped the repository, navigate to ArcGIS Online and click the **Notebook** tab.  Choose **ArcGIS Notebook Python 3 Standard (3.0)** when you're prompted to choose a notebook type.

![](/images/agol-notebook-1.png "ArcGIS Notebook Python 3 Standard (3.0)")



