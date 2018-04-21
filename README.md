# DOCOclient
## Introduction
DOCOclient is a piece of software that enables you to make repetitive documentation tasks easy! By creating reusable document parts, DOCOclient enables you to compile documentation in a fashion that conforms to your organisation's standards and guidelines. By using spreadsheets you can enter variable data for the specific document you are creating. Equally, you use spreadsheets to enter variable data that applies to all documents inside your project. Think about details such as your organisation's name, address, telephone and email address details.

DOCOclient is the first part of a suite of software products called DOCO (DOcument COmpiler). The terminology used by DOCO for the reusable document parts is "recipe" and "ingredients". A recipe is an asciidoctor document (.adoc extension) that uses the "include::" directive to point to other .adoc files, which are called ingredients.

DOCO closes the gap between fully automated documentation creation software (like invoicing, account statements, etc) and manual document creation or repetitive, similar documents.

## Advantages
* Separation of layout, variable data and text
* Allows you to focus on writing your documentation
* Enforces a consistent look and feel of your documents
* Single entry of data used within various documents
* Project-based documentation generation

## Who we are
Aureus Group is a software and consultancy company. We publish software that assists our clients in automating repetitive documentation tasks. Please get in touch with us if you find any bugs or documentation updates. Our email address is: aureus-group@protonmail.com.

# Requirements
In order to make use of all features of DOCOclient, you should have the following software installed:

* asciidoctor 1.5.6.2 or higher
* asciidoctor-pdf 1.5.0.alpha.16 or higher
* spreasheet software that can save in Microsoft Excel 2007-2013 XML (.xlsx) format
* a text editor that can read and write UTF-8 encoded files (atom, brackets, notepad++)

Please note that asciidoctor and asciidoctor-pdf have their own software requirements.

# Installation
At this point in time, there is no installer available. This will change in the future. For the time being, if you want to use DOCOclient, you will need to either run the source code or run one of the pre-compiled binaries.

## Running source code
The software is written in Python. In order to run DOCOclient directly from the source, you will need to download the source code. The minimum requirements are:

* Python 3.5.2
* Python module: packaging
* Python module: pyperclip
* Linux users, please refer to https://pyperclip.readthedocs.io/en/latest/introduction.html#not-implemented-error regarding the "Not implemented error" in pyperclip.

## Pre-compiled binaries
To install the pre-compiled binaries, download the archive for your operating system. Extract the archive. Optionally, copy the extracted files to a location from where you want to execute them.

There are no pre-compiled binaries for Mac OSX available.

# Configuration and execution
Inside the extracted archive, you will find a directory called "templates". Inside this directory there are a directory called "recipes" and one called "themes". These directories contains sample recipes and a sample theme, respectively. You are free to copy these directories to other locations.

When you run the software for the first time, you will be asked to create a configuration file; the following details will need to be provided:

* Project directory - specify a path on your computer where you want to store the projects that you will create.
* Recipe directory - specify the path to the "templates/recipes" directory described above.
* Theme directory - specify the path to the "templates/themes" directory described above.

The following details are used to set as defaults inside every document you create.
* Author - Your full name. 
* Author title - Your job title.
* Author phone - Your telephone number.
* Author email - Your email address.

Please note, DOCOclient does not send any of this information to us or any of our associates. It is just there so you don't have to enter it for every document you create.

# Known bugs and limitations
## Known bugs
* There are currently no known bugs.

## Limitations
* The software was not tested on Mac OSX.
* Reading cell formatting information from .xlsx spreadsheets is currently limited. We are committed to improving the situation.
