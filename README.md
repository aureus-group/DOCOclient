# DOCOclient
## Introduction
DOCOclient is a piece of software that enables you to make customised, repetitive documentation tasks easy!

The power behind DOCO comes from the fact that it is recipe-centric, rather than template-centric. A traditional template in a word processing context contains a (non-enforced) layout, along with text and variables. The end-user updates the variables and modifies the text where required in order to create a custom document.

This approach has the following disadvantages:

* The end-user is responsible for ensuring the layout complies with their organisation's standards.
* As a result of copy/paste actions, fonts may have changed, table widths are not all aligned, etc.
* Updates like: change of organisation's address, phone number, logo, etc. need to be applied to every individual template.
* Variable data like: client details need to be entered for every document that is created as part of a project/case.
* A tendency may exist to re-use finished documents from similar projects which could cause embarrassing mistakes.
* Inconsistencies may exist across documents because slight differences exist within templates.

In order to overcome the disadvantages outlined above, we need to do three things:

* Separate the layout from the text inside a document.
* Separate the variable data from the document's content.
* Define layout, document title pages, page headers, etc. only once.

By doing so, the end-user can concentrate on customising the document without getting buried under the issues described previously.

## Who we are
Aureus Group is a software and consultancy company. We publish software that assists our clients in automating repetitive documentation tasks. Please get in touch with us if you find any bugs or documentation updates. Our email address is: aureus-group@protonmail.com.

# Terminology explained
DOCO software splits up a traditional template into the following parts:

* A theme that dictates the layout of a document.
* Spreadsheets that are used to capture variable data for your document.
* Ingredient files that hold predefined pieces of text.
* A recipe file that binds the above items together.

Let's explore these components below.

## Theme
A theme holds information on what a title page looks like. Which fonts does your document use, what size and colour are they? It holds information on what the header and footer of every page look like.

Once a document has been created, the theme is consulted to define what the end result actually looks like. Because the theme is defined only once, any updates to it will automatically be applied to all documents using the theme.

Please be aware that multiple themes can be defined, giving you the flexibility to not apply updates to existing documentation. Another use case for multiple themes is if you require different logos to be displayed, depending on who the customer is.

## Spreadsheets
We chose to use spreadsheets for the end-user to supply variable input into documentation. Doing so, allows you to use the power of your spreadsheet software: using formulas, pulling in data from external sources, etc.

Consider the following example. A proposal document for the supply and installation of a winch system at a boat ramp would include details regarding the maximum weight of a boat, the angle and length of the ramp, the tides, etc. Based on this information an appropriate winch, pulleys, and cable can be proposed. By entering the inputs in a spreadsheet, the spreadsheet software can calculate which equipment is suitable for the job. Those requirements can then be incorporated in the proposal document.

For new revisions of a document, you can simply (copy the spreadsheet and) update the values, without having to re-enter all data. Also, the spreadsheet format keeps all relevant data together for quick referencing. This prevents you from scrolling through pages of documentation in order to find the detail you are looking for.

## Ingredients
The recipe-centric approach that DOCO takes, recognises that every document across your organisation contains parts that are similar. Think of contractual details, a disclaimer notice, a page outlining contact details of stakeholders inside a project. By defining those document parts only once, it allows you to not only re-use them but also to update them in a single location.

Once updated, any new documents created that include the ingredient file will automatically use the updated version. There is no need to apply updates to multiple document templates.

Ingredients can reference other ingredients and they can reference data provided by spreadsheets.

## Recipes
A recipe contains references to ingredient files and spreadsheet data. Most notably, it also defines which theme is to be applied once the document is ready for publishing.

# Conclusion
By creating reusable document parts, DOCOclient enables you to compile documentation in a fashion that conforms to your organisation's standards and guidelines. By using spreadsheets you can enter variable data for the specific document you are creating. Equally, you use spreadsheets to enter variable data that applies to all documents inside your project. Think about details such as your organisation's name, address, telephone and email address details.

DOCOclient is the first part of a suite of software products called DOCO (DOcument COmpiler). DOCO closes the gap between fully automated documentation creation software (like invoicing, account statements, etc) and manual document creation. Please note that DOCO can also be employed for manual or semi-manual document creation.

## Advantages
* Separation of layout, variable data and text.
* Allows you to focus on writing your documentation.
* Enforces a consistent look and feel of your documents.
* Single entry of data that is used within multiple documents.
* Project-based documentation management.

# Requirements
In order to make use of all features of DOCOclient, you should have the following software installed:

* asciidoctor 1.5.6.2 or higher
* asciidoctor-pdf 1.5.0.alpha.16 or higher
* Spreadsheet software that can save in Microsoft Excel 2007-2013 XML (.xlsx) format.
* A text editor that can read and write UTF-8 encoded files (atom, brackets, notepad++).

Please note that asciidoctor and asciidoctor-pdf have their own software requirements.

# Installation
At this point in time, there is no installer available. This will changes in the future. For the time being, if you want to use DOCOclient, you will need to either run the source code or run one of the pre-compiled binaries.

## Running source code
The software is written in Python. In order to run DOCOclient directly from the source, you will need to download the source code. The minimum requirements (in addition to those listed above) are:

* Python 3.5.2
* Python module: packaging
* Python module: pyperclip
* Linux users, please refer to https://pyperclip.readthedocs.io/en/latest/introduction.html#not-implemented-error regarding the "Not implemented error" in pyperclip.

## Pre-compiled binaries
To install the pre-compiled binaries, download the archive for your operating system. Extract the archive. Optionally, copy the extracted files to a location from where you want to execute them.

There are no pre-compiled binaries for Mac OSX available.

# Configuration and execution
Inside the extracted archive, you will find a directory called "templates". Inside this directory there are a directory called "recipes" and one called "themes". These directories contain sample recipes and a sample theme, respectively. You are free to copy these directories to other locations.

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
* Error handling is not yet optimal. Under certain circumstances, the software can crash. A message should be displayed indicating what the problem is.

## Limitations
* The software was not tested on Mac OSX.
* Reading cell formatting information from .xlsx spreadsheets is currently limited. We are committed to improving the situation. Please let us know your suggestions.
* Limited testing has been performed on Ubuntu-gnome 16.04 and Windows 10.
