## Environmental Assessment Office Internal Guidance

This is a skeleton repo containing the
[CFPB/DOCter](https://github.com/CFPB/DOCter)-based
[Jekyll](http://jekyllrb.com/) template for
[18F Guides](http://18f.github.io/guides/).

### Windows Installation

Download and install:

- Git Bash 2.14.1
- NodeJS v6.1.1.3
- Ruby 2.4.1-2

Installing Ruby:

When installing MSYS2 just hit enter.
Do not put a number in at all.

After all programs are installed go to the desired directory for the source code.

This step will hopefully be replaced with Dreamweaver.
In the directory, right-click and click on Git Bash Here.

Type in:

```

git clone https://github.com/bcgov-c/EAO-Internal-Guidance.git

```

You will be prompted for your git username and password.
This user must be allowed to pull from this repository.

Now type in:

```

cd EAO-Internal-Guidance

```

You are now in the project directory.

Type in:

```
gem install bundler

bundler install

./go serve

```

The server should be running.
In an internet browser go to the url:

http://127.0.0.1:4000/

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
