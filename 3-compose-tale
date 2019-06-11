# Creating tales

In this lesson you'll learn how to create a tale in Whole Tale.

Questions:
* How do I create my own tale?
* What is the tale "workspace"?
* How do I upload files?
* What is the "home" directory
* How to I customize the environment
* How do I rebuild the Tale image?

Objectives:
* Learn how to create a tale
* Learn the difference between the home, external data, and workspace folders
* Learn how to rebuild the tale image and restart your instance

## Activity: Compose a Tale

* Select the "Compose" button
* Enter a title for your tale
* Select your desired environment
* Select "Launch New Tale"
* A notification panel will appear indicating the status of your new tale

What's happening:
* A new tale instance is being prepared (Docker container) with associate workspace (folder)
* Your personal home directory is mounted into the running container
* When the tale instance is ready, you should be redirected to the "Run" page

## "Run" page

The "Run" page provides access to your running tale instances. 
* Interact: access the interactive environment
* Files: Manage files and data
* Metadata: Provide descriptive metadata

## Activity: Accessing the interactive environment

* Select the "Interact" tab to access the running environment
* Select the "popout" icon to open the environment fullscreen

## Files: Home, External Data, and the Tale Workspace

* The "Files" tab allows you to manage files in Whole Tale. 
* The "Home" directory is a private space on the Whole Tale system for you to stage data or store information not associated with any tales.  The Home directory can be used to store utilities or private information (e.g., keys) that would never be included in a published tale. The Home directory is mounted across all of your running Tales.
* The "External Data" tab allows you to add or remove linked external data from your Tale. 
* The "Tale Workspace"  is a folder that contains all of the files associated your tale. This may include some combination of code, data, narrative, workflow scripts, and repo2docker compatible configuation files. Anything in this folder will be part of your tale during the export and publishing process.

## Activity: Uploading files

* Select the "Files" tab
* Select the "Home" folder then the blue "+" button and select "Upload file" to upload a file to your home folder
* Select the "Tale Workspace" folder then the blue "+" button and select "Upload file" to upload a file to the workspace
* Select the "Interact" tab and browse the "home" and "workspace" folders in the container
* Optionally, upload files directly to both folders via the interactive environment 

Question:
* Why do we have two ways to upload files to Whole Tale?

## Activity: Customizing the environment

* Select the "Interact" tab to access the running tale instance
* Create a [repo2docker compatible configuration file](https://repo2docker.readthedocs.io/en/latest/config_files.html)
* Select "Rebuild Tale"
* When the build is complete, select "Restart Tale" to restart your instance using the new image

A simple example would be to create a file called `apt.txt` containing just the package `byacc`.

What's happening:
* A new image is built based on the changes in your workspace
* The original interactive environment is still available while the image is being built.

## Key points:
* The Compose page is used to create a new tale using the selected environment
* The home directory is a place for you to store information that is not part of any Tale
* The workspace directory contains all of the files associated with your tale
* The tale environment can be customized using repo2docker compatible configuration files
