## Running tales

This lesson instructs you how to find and run an existing tale in the Whole Tale system.

Questions:
* How to I run an existing tale?
* What does it mean to run a tale?
* What are the elements of a tale?
* What are the limits of the system?

Objectives:
* Learn how to run an existing tale and what happens
* Learn about public tales
* Learn about tales and tale instances
* Learn about the limits of Whole Tale

## Introduction

The Whole Tale platform allows users to create "public" tales that are available to anyone on the system. Public tales appear on the Browse page.

## Activity: Running your first tale

* On the Browse page, search for "Example" to find "Example Tale: Mapping Estimated Water Usage"
* Select "Launch" to start an instance of this Tale
* Once started, select the tale from the "Launched Tales" panel

What happened?
* An instance of the tale was created (i.e., Docker container)
* A notification window displayed the status of the tale as it started
* You are able to access an instance of JupyterLab

### What is a tale instance?
An instance is your private copy of the tale environment. Under the hood,
each instance is a Docker container with your home directory mounted along with
the tale workspace and any registered data.


### Activity: Exploring the running tale
If not already displayed, select the "Interact" tab. You should see an instance
of JupyterLab running with the three directories on the left. 

* Open the `workspace` folder and the README.md to read about the contents of the workspace.
* Browse the `home` folder. What do you see? We'll learn more about the home folder in the next lesson.
* Browse the `data` folder. What do you see? We'll learn more about the home folder in the next lesson.
* Select the "Files" tab and inspect the contents of the home, external data, and workspace folders. How do these relate to the contents of the running Jupyter environment?
* Select the "Metadata" tab and explore the properties of the tale.  Is the tale public?  Has it been published?
* Go back to the "Interact" tab. In JupyterLab, open the `wt_quickstart.ipynb` and run it by selecting the "play" button.

Questions:
* The instance that you're running requires the `bokeh` and `pandas` libraries, but you didn't need to install any packages. Why not?
* Assume that the generated map was used in publication. What issues do you see with the notebook or map?
* How do you feel about using an interactive notebook as the entrypoint to generate research output?

## Resource limits

Each user is currently limited to running 2 tale instances.

## Key points:
* You run an existing Tale by "launching" it
* When you run a Tale, you get a private instance (Docker container)
* If the Tale creator uses repo2docker compatible configuration files, the running instance has any dependencies pre-installed
