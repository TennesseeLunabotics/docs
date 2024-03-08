---
title: Getting Started
layout: default
nav_order: 2
---

# Editing the Site
{: .no_toc }

## Table of Contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

## Gaining Access

The files that make up this site live with the rest of our code in the Tennessee Lunabotics 
[Github Org]. To edit, you first must be a member of the organization to have write access. 
Create a Github account if you don't have one already, and message the current Control Systems 
Team Lead on Discord with your Github username.

An email will be sent with a link to accept the invitation to the organization. Alternatively, it
should also appear in your notifications center on Github.

## Editing Locally

If you are editing multiple files, it is much easier to edit locally, as the Github.com editor will
only let you edit one file at a time. If you wish to edit locally, very light knowledge of `git` 
will go a long way. The [Github Desktop Client] is a good alternative to the command line.

### Command Line

Navigate to where you want the files stored locally on your computer. Then run
```sh
git clone https://github.com/TennesseeLunabotics/docs
cd docs
```

If you have already cloned the files before, make sure to run `git pull` before you begin to edit. 
This is to make sure that you have the latest versions of all of the files.

Make the changes you wish to make (Visual Studio Code is a good app for this), then run
```sh
git add .
git commit -m"YOUR MESSAGE GOES HERE"
git push
```

Your changes are then uploaded to the site and published.

## Editing on the Web

You can browse this site's files on Github, and also go directly to a file from the site by
clicking on the `Edit this page on Github` link at the bottom of each page. On Github, click
on the pencil icon in the top right to open the editor to make changes. When done, click on 
the `Commit Changes` button, enter a change title and message (message optional), and click 
commit.

{: .note }
The markdown language, used in these files, does not support specialty elements such as this
callout. When using the preview features on Github, don't be alarmed if buttons, callouts, etc
don't render. They will when the site is deployed.

## Github.dev

If you do not wish to edit locally or do not want to use the editor built into Github,
you may wish to experiment with github.dev. This is a version of Visual Studio Code that runs
in your web browser. You can make larger edits easier without having to download the files.

To use, go to [github.dev/tennesseelunabotics/docs](https://github.dev/tennesseelunabotics/docs).
Make your changes, then click on the source control icon on the left, enter a message, then hit
the `Commit and Push` button.

At the time of writing, I am unsure of the limitations of this, or at what point you have to 
start paying. I made a test edit and was able to publish my changes, but I also happen to 
have a Github Pro account.

## General Page Format

Help with the markdown language (the language the files that make up these pages uses) can be
found in many places online. In addition to that, there's documentation and examples of what
can be done on these pages at [Markdown Help](docs/ui-components.md).

A couple things to note:
- Every page, with the exception of the homepage titled `index.md` will live inside of the docs folder.
- Every page will have a heading info block located at the top. This will consist of a title, layout (this should be default), and a nav order used for ordering the sidebar. The info block for this page is: 
```
---
title: Editing
layout: default
nav_order: 2
---
```
- The url for each page will be its filepath. If you wish to have nested pages (please do when applicable,
for the sake of organization), The heading info block will need a couple extra fields. Take a look at the headings 
for `docs/ui-components/code.md` and its child `docs/ui-components/line-numbers.md` as an example.

- If you wish to have a table of contents, add the following to the top of your page below the info block:
```
# Page Title
{: .no_toc }

## Table of Contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---
```

## Publishing

After committing your changes, github will attempt to rebuilt the entire site and publish. If you get a green check
next to your commit, then everything succeeded. If not, something didn't work. 

[](../assets/images/editing-help-commit-example.png)

Clicking on the red X and checking the details of the `CI / build (push)` job may help. If you are still unable to figure it out, reach out to programming (someone likely already got an email about the failed build, but don't sweat that).



[Github Org]: https://github.com/TennesseeLunabotics
[Github Desktop Client]: https://desktop.github.com/