# Exporting and Publishing Tales

Questions:
* How do I export a tale?
* Can I run it locally?
* How do I publish a tale to DataONE?

Objectives:
* Learn how to export a tale and a little about BagIt and the BagIt-RO format
* Learn how to run the tale locally
* Learn how to publish a tale to a DataONE network member node
* Learn which repositories are supported

# Exporting a tale

The export process can be used to create either a basic zip archive or a [BagIt](https://en.wikipedia.org/wiki/BagIt) archive of your tale. While simple zip files are more intuitive, BagIt offers a number of additional useful features:
* BagIt is an archival format origially developed by the library of congress and widely adopted in the research data repository community
* Standards are beginning to emerge around technical metadata for research compendia, such as the [Research Object Archive](https://github.com/ResearchObject/bagit-ro).
* Tools such as [bdbag](https://github.com/fair-research/bdbag) can be used to validate BagIt archives and also fetch external data.

## Activity: Export your tale
From the earlier exercise, export your tale in BagIt format:
* Select the "Run" tab and your instance
* Select the "..." menu and "Export as BagIt"
* Open the zipfile on your laptop
* Explore the directories

Question:
* How is this different than a simple zip file?
* Where is the workspace?
* How do can you tell which external datasets are included?

## Activity: Run locally
If you have [Docker](https://docs.docker.com/install/) installed, you can run the exported tale on your laptop:

* Open a terminal
* Change directory to the root of the extracted BagIt archive
* `sh run-local.sh`

What happens:
* If not already present on your system, the Docker image is built
* `bdbag` runs to download any external datasets
* A Docker container instance is started

# Publishing

Whole Tale is a platform to create, execute, and publish tales but it is itself not an archival repository.  Whole Tale is designed to leverage existing research data infrastructure for issuing digital object identifiers and long-term archiving of published tales. 

The current version of Whole Tale supports publishing to the Knowledge Network for Biocomplexity (KNB) and the NSF Arctic Data Center. We also support publishing to a non-production "sandbox" repository hosted by NCEAS.

## Activity: Publishing your tale

* Select the "Run" tab and your instance
* Select the "..." menu and "Publish"
* Select "DataONE Development" (please do not publish to either production repository)
* Select "Publish"
* You'll be prompted to login via ORCID, which may require setting up an ORCID account

What's happening:
* Your tale is converted from the Whole Tale BagIt-RO format to the DataONE format and a data package created on the sandbox repository on your behalf.
* A DOI is issued by DataONE for your tale. The DOI can be used in your publications.

## What about other repositories?
We are working on adding Dataverse and Zenodo as publishing targets for Whole Tale as well as adding support for more DataONE network members.  In the meantime, you can always publish the exported zip file to any general-purpose repository.

## Key points:
* You can export your tale from Whole Tale
* If you have Docker installed, you can run your tale locally
* The exported tale can be a simple zip file or in an archival format
* You can publish your tales to a sandbox instance for testing or to KNB or the Arctic Data Center
