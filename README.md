# DECIDE app

## Issue tracker
This repository does not store the code for the DECIDE 
app - that is stored in a private CEH GitLab repository from where it 
can be deployed to our Kubernetes clusters. The primary aim of this repository
is to provide a publicly accessible issue tracker for the app. We will also use 
milestones to assign particular issues and tasks
to particular releases of the app.

## Info pages
This repository is also used to store the Markdown pages served
as static content within the app.

These pages, and associated resources like images, are stored
directly under the *infopages* sub-folder. There is also a text file
in that folder - *menu.txt* - which defines the Infomation
pages menu within the app. 

The first line of each markdown page must have
a comment on the first line the provides the page title used 
on the page bar in the app. This must be formatted as show below.
```
[//]: # (title: DECIDE score)
```
Note that the markdown pages are consumed in the app by a React
plugin that is capable of interpreting HTML too. We're using HTML/CSS
here and there within the MD pages, e.g. to float images.

## The menu.txt file
The menu.txt file is read and parsed by the app and it controls the
layout of the menu under the _Information_ item in the menu. The general
format of entries in this file is:
```
Menu item text ## markdown_filename
```
Do **NOT** use any leading spaces before menu item text _unless_ the 
item is in a submenu - see below.

A submenu is define simplly like this:
```
Submenu name
```
Most importatnly it must be indented by one space from the menu
item above it. The all subsequent menu items that are
to come under that submenu must be indented by the same amount.
Submenus can themselves contain submenus.

