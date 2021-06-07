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
withint the *infopages* sub-folder. There is also a text file
in that folder - *menu.txt* - which defines the Infomation
pages menu within the app. This text file references the markdown
pages via a tag encoded within a comment on the first line
of each markdown page.
