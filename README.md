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

These markdown pages are stored
in the *infopages/md* folder.

The first line of each markdown page must have
a comment on the first line the provides the page title used 
on the page bar in the app. This must be formatted as show below.
```
[//]: # (title: DECIDE score)
```
Note that the markdown pages are consumed in the app by a React
plugin that is capable of interpreting HTML too. We're using HTML/CSS
here and there within the MD pages, e.g. to float images.

## Images
Images for displaying in the markdown pages are all kept together in
the *infopages/images* folder. Images can be included in markdown
pages using standard markdown, but there are very limited formatting
options.

But the markdown parser used in the app is also capable of interpreting
HTML. Therefore it will normally be better, for the sake of formatting,
to use HTML to includes images.

Here is an example of HTML that can be used to include an image
file in a markdown page:
```
<img src="/infopages/images/score-image2.png" style="float:right; width: 400px; margin-left: 1em"/>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Etiam eget risus ac est mattis congue quis at lacus. Praesent dignissim nunc eget ante dignissim, nec sodales enim lacinia.
```
In that example the HTML `<img>` tag is used to include an image from the
*infopages/images* folder. The `style` attribute sets a number of 
CSS properties that style the image. In this example they set the width of
the image and 'float' it to the right of the paragraph that follows, 
which means that the the paragraph text will appear to the left of the 
image. The `margin-left` CSS property ensures that there is a gap
between the image and the text to it's left.

_Note that GitHub will not interpret the CSS properties so when you
view the markdown in GitHub, the image will not appear with the formatting
that will be used in the app._

## The menu.txt file
The *menu.txt* file, found in the *infopages* subfolder, is read and 
parsed by the app and it controls the
layout of the menu under the _Information_ item in the menu. The general
format of entries in this file is:
```
Menu item text ## markdown_filename
```
Do **NOT** use any leading spaces before menu item text _unless_ the 
item is in a submenu - see below.

A submenu is define simplly like this:
```
Name of submenu
```
Most importatnly it must be indented by one space from the menu
item above it. The all subsequent menu items that are
to come under that submenu must be indented by the same amount.
Submenus can themselves contain submenus.

