# Introduction

The purpose of this tutorial is to provide you with basic, hands-on experience using
the core capabilities of the Whole Tale platform.

## About the Whole Tale project

This section introduces the Whole Tale project and platform.

*Questions:*
* What is Whole Tale?
* What is a tale or research compendium?
* What are Docker and `repo2docker`?

*Objectives:*
* Learn about the Whole Tale project and platform
* Learn what a "tale" is and how it relates to similar research objects
* Learn what Docker and repo2docker are and how they relate to Whole Tale


### What is Whole Tale?

Read the [About](http://docs.wholetale.org/en/stable/README.html) section of the Whole Tale website.

### What is a "tale"?

A tale is a type of executable research object that combines data (by reference
or copy), code (computational methods), the computational environment, and
narrative (traditional science story). Tales are captured in a standards-based
archival format complete with metadata. Tales are inteded to be exposed for
reproducibility and reuse.

<img src=http://docs.wholetale.org/en/stable/_images/tale_diagram.png width=500>
We will cover the tale format in detail later, but for now just highlight that
a tale is intended to be re-runnable both in and outside of the Whole Tale
platform. This is achieved by using Docker and more specifically the
`repo2docker` component developed by the Project Jupyter community.  Each tale
has a "workspace" (folder) that includes information about the environment that
can be used to build a Docker image.

### What is a "research compendium"?

The concept of a research "compendium" was introduced by Gentleman and Lang
(2004) 

> "...as both a container for the different elements that make up the
document and its computations (i.e. text, code, data, ...), and as a means
for distributing, managing and updating the collection" for reproducible
research.

The phrase "research compendium" has been adopted by a number of communities to
describe a variety of conventions and practices for sharing and distributing
research artifacts to enable computational reproducibility.


### Activity: Exploring a research compendia

Research compendia come in a variety of forms. Let's look at some published examples:

**Example 1:** _Research compendium package for d'Alpoim Guedes and Bocinsky 2018_
* Published compendium: https://zenodo.org/record/1405073
* Associated Github repository: https://github.com/bocinsky/guedesbocinsky2018

**Example 2:** _Replication Data for: The Hostile Audience: The Effect of Access to Broadband Internet on Partisan Affect_
* Dataverse package: https://dataverse.harvard.edu/dataset.xhtml?persistentId=doi:10.7910/DVN/W1YJZQ

**Example 3:** _A Standard for the Scholarly Citation of Archaeological Data_
* Code Ocean Capsule: https://doi.org/10.24433/CO.ca12b3f0-55a2-4eba-9687-168c8281e535

Questions:
* Are these research compendia?
* If you were asked to verify or review them, where would you start?


### What is Docker?

Docker is a popular virtualization ("container") platform that has been widely adopted for the packaging, distribution, and deployment of software including scientific software. 

From https://www.docker.com/resources/what-container:

> A container is a standard unit of software that packages up code and all its dependencies so the application runs quickly and reliably from one computing environment to another. A Docker container image is a lightweight, standalone, executable package of software that includes everything needed to run an application: code, runtime, system tools, system libraries and settings.

> Container images become containers at runtime and in the case of Docker containers - images become containers when they run on Docker Engine. Available for both Linux and Windows-based applications, containerized software will always run the same, regardless of the infrastructure. Containers isolate software from its environment and ensure that it works uniformly despite differences for instance between development and staging.

A `Dockerfile` is a simple text file that contains instructions used to build a Docker image.

A Docker registery is a library of pre-built images that can be 'pulled'.  For example, https://hub.docker.com.

### Activity: Exploring Dockerfiles

Below is a very simple `Dockerfile`:

```
FROM ubuntu:18.04
RUN apt-get update -y && apt-get install -y vim
```

The `FROM` instruction specifies the base image to be used in the derived image. In this case, the base image is `ubuntu:18.04`. Look at the registry entry for this image https://hub.docker.com/_/ubuntu and the associated Ubuntu release description page http://releases.ubuntu.com/18.04/.

Questions:
* What does this Dockerfile do?
* What is `ubuntu` and what does `18.04` mean?

Many researchers have adopted Docker images as a method of distributing their software and facilitating computational reproducibility. The compendium in **Example 1** above includes a `Dockerfile`.  Inspect it and consider the following questions:

Questions:
* Why did the authors decide to include this in the compendium?
* What would it require for a reviewer or other researcher to use this approach?
* Do you use Docker?

### What is repo2docker (and why do we use it)?

repo2docker is part of the Binder platform developed by the Project Jupyter community. As suggested by the name `repo2docker` provides a way to convert a repository (e.g., Github) into a Docker image. If your repository (or local directory) contains some [well-defined and commonly used configuration files](https://repo2docker.readthedocs.io/en/latest/config_files.html), repo2docker can be used to build and run a Docker container with the specified software packages installed.  The Binder platform and [mybinder.org ](https://mybinder.org) is widely used by researchers in part because it eliminates the need to understand how to write and use Dockerfiles.  [mybinder.org](https://mybinder.org), supported in part by funding from the Sloan Foundation, provides the infrastructure to build and run "binders" so researchers don't have to.

To better align with the Jupyter community, in 2018 the Whole Tale team decided to replace a home-grown solution with repo2docker.

### Activity: Exploring repo2docker

Look at the list of supported [configuration files](https://repo2docker.readthedocs.io/en/latest/config_files.html)

* Do you recognize or use any of these already?
* Look at this [example binder](https://zenodo.org/record/1345320#.XP6Gr29Kh24). What type of Binder is it? How do you run it?
* What is the base operating system used on repo2docker generated images?

## Key points

* Whole Tale is an NSF funded Data Infrastructure Building Block project building an open source platform for reproducible research
* Tales are part of an emering class of composite research objects that can broadly be described as "research compendia"
* Docker is a specific technology used to package and distribute software with dependencies
* repo2docker is a tool developed by the Jupyter community to simplify the process of creating Docker images based on a set of simple configuration files.

