## Environmental Assessment Office Internal Guidance

This is a skeleton repo containing the
[CFPB/DOCter](https://github.com/CFPB/DOCter)-based
[Jekyll](http://jekyllrb.com/) template for
[18F Guides](http://18f.github.io/guides/).

### Getting started

#### Installing Ruby

You will need [Ruby](https://www.ruby-lang.org) ( > version 2.1.5 ). To check
whether it's already installed on a UNIX-like system, open up a terminal
window (e.g. Terminal on OS X) and type `ruby -v` at the command prompt. For
example, you should see something similar to the following:

```shell
$ ruby -v
ruby 2.2.3p173 (2015-08-18 revision 51636) [x86_64-darwin14]
```

If the version number is less than 2.1.5, or instead you see something like:

```shell
$ ruby -v
-bash: ruby: command not found
```

Then Ruby is not installed, and you should choose one of the installation
methods below. [The "Installing Ruby" page of the official
Ruby language web
site](https://www.ruby-lang.org/en/documentation/installation/) explains how
to do this in a number of ways across many different systems.

##### Quickest Ruby install/upgrade for OS X

On OS X, you can use [Homebrew](http://brew.sh/) to install Ruby in
`/usr/local/bin`, which may require you to update your `$PATH` environment
variable:

```shell
$ brew update
$ brew install ruby
```

##### Optional: using a version manager

Whether or not Ruby is already installed, we strongly recommend using a Ruby
version manager such as [rbenv](https://github.com/sstephenson/rbenv) or
[rvm](https://rvm.io/) to help ensure that Ruby version upgrades don't mean
all your [gems](https://rubygems.org/) will need to be rebuilt.

#### Cloning and serving the Guides Template locally

To create a new guide and serve it locally, where `MY-NEW-GUIDE` is the name
of your new repository:

```shell
$ git clone git@github.com:bcgov-c/EAO-Internal-Guidance.git
$ cd MY-NEW-GUIDE
$ ./go serve
```

The `./go` script will check that your Ruby version is supported, install the
[Bundler gem](http://bundler.io/) if it is not yet installed, install all the
gems needed by the template, and launch a running instance on
`http://localhost:4000/`.

#### Follow the template instructions

The Guides Template (either [running locally](http://localhost:4000) or the
[published version](https://pages.18f.gov/guides-template/)) will walk you
through the rest of the steps to edit and publish your guide.

### Editing the E-Guide

This section will explain how to add new sections to the side bar as well as edit the pages they correspond with.
Before editing be sure to run the server using the following command.

```shell
$ ./go serve --watch
```

--watch will (usually) automatically regenerate files.
If the website is not updating you may have to wait several minutes.
If the site is still not updating, restart the server and allow Jekyll to regenerate files. 

#### Editing the sidebar

To change the settings in the sidebar open _config.yml.
The following is an example of a seperate section with a heading and a child for that heading:

```
- text: OTHER RESOURCES
  internal: true
- text: Office Procedures
  url: Office%20Procedures/
  internal: true
  children:
  - text: Admin Resources
    url: Admin%20Resources/
    internal: true
```
Note: %20 corresponds with a space.

Text corresponds with the title that will appear on the side bar.

Url corresponds with the path to the webpage that will be displayed if the heading is clicked.

#### Editing a page

To change a page go to the directory _pages.
This folder contains .md files that will dictate what will appear on the page.

If we wanted to create a page for the Office Procedures, you must create a new .md file entitled 'Office Procedures.md'

If we wanted to create a child page first you must create a directory with the name of its parent.
So if we wanted to make a page for Admin Resources then we need to make a directory named 'Office Procedures'
Within that folder you must create a file called 'Admin Resources.md

Within a .md file you will have several ways to format a page.

##### Divider:

'---'

##### Title:

'title:[YOUR_TITLE]'

##### Bullet Point:
'*'

##### Headings:

'###' where the number of pounds corresponds with how large the heading is. (Less means larger)

##### PDF:

```
[Exemptions](/docs/fees/files/EA%20Exemption%20Fee%20Process_Dec2016.pdf) (Dec 2016)[PDF]
```

The text above is an example of how to add a pdf.

The string in the first [] will correspond with the text of the hyperlink.

The string in the first () will correspond with the path to where the .pdf file is.

Everything after the first () will be text that will trail the hyperlink.

### Public domain

This project is in the worldwide [public domain](LICENSE.md). As stated in [CONTRIBUTING](CONTRIBUTING.md):

> This project is in the public domain within the United States, and copyright and related rights in the work worldwide are waived through the [CC0 1.0 Universal public domain dedication](https://creativecommons.org/publicdomain/zero/1.0/).
>
> All contributions to this project will be released under the CC0
>dedication. By submitting a pull request, you are agreeing to comply
>with this waiver of copyright interest.
