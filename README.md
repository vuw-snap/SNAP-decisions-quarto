# VUW-SNAP website

The VUW-SNAP website is managed via two repositories:

 - **github.com/vuw-snap/SNAP-decisions-quarto** <br/>
   This repository contains the source files. This is where all website editing takes place (so most issues and pull requests are best made here).
 - **github.com/vuw-snap/SNAP-decisions** <br/>
   This repository contains the compiled html for the website. This repository should never be edited directly. The html is compiled from the source files using quarto and then pushed (separately) to update the website.

We use Quarto to build the website from qmd (markdown) files. 
Before editing the source files you may wish to familiarise yourself with the basics of Quarto, see: <br/>
https://quarto.org/docs/get-started/hello/text-editor.html <br/>
https://quarto.org/docs/guide/

The basic structure of the **source** repository is:

 - _quarto.yml : sets out framework of website
 - various xxx.qmd files: contain markdown versions of the final .html files
 - styles.css: where you control some of formatting of the website
 - index.qmd: is the opening/landing page of the website

## Basic instructions for editing the website

If this is your first time editing the website, you'll want to do the following:

 - Change to a directory ("cd") where you will store both repositories
 - Clone SNAP-decisions: <br/>
   git clone https://github.com/vuw-snap/SNAP-decisions.git
 - Clone SNAP-decisions-quarto  <br/>
   git clone https://github.com/vuw-snap/SNAP-decisions-quarto.git

If you've edited the website before (i.e. already have local copies of these repositories), do a "git pull --rebase" in each directory.
If it has been a while since you've used Quarto, you might like to first update to the most recent version. 
Doing so should help minimise the number of changes that are made to older html files in the repository.
Download and install from https://quarto.org/docs/download/

Then, proceed to edit the website and render/preview your changes:
   
 - Modify/add files within SNAP-decisions-quarto with your editor
 - From within the "SNAP-decisions-quarto" directory produce the html by typing <br/>
   quarto render
 - Check your changes in your browser by typing <br/>
   quarto preview

NOTE: The compiled html will be in directory "../SNAP-decisions" <br/>
(You can potentially point it to another directory by opening _quarto.yml and editing the line 
"output-dir: ../SNAP-decisions", but please don't commit this change to the repository!
It is probably best you leave it as is.)

Once you are happy with your changes (and have checked them!), commit and push everything back to github. 
You need to do this for both repositories!
For example:

 - From inside SNAP-decisions-quarto do the standard git stuff: <br/>
   git add --all <br/>
   git commit -m "make sure to write a suitable commit message" <br/>
   git push https://github.com/vuw-snap/SNAP-decisions-quarto.git main <br/>
   Note: You may prefer to push via ssh, make sure to setup a key and change the git remote setting from https to ssh.
 - From inside SNAP-decisions do the standard git stuff: <br/>
   git add --all <br/>
   git commit -m "make sure to write a suitable commit message" <br/>
   git push https://github.com/vuw-snap/SNAP-decisions.git main <br/>
   Note: Again, you may prefer to push via ssh, make sure to setup a key and change the git remote setting from https to ssh.
   
The website will automatically update soon after you push changes to SNAP-decision.git

## Adding a blog post to the website

The most common change to the website will involve adding/editing a blog post.
For a new blog post you'll need to create a new (suitably named) sub-directory to the "posts/" directory.
Within the new sub-directory, create an index.qmd file and fill it out with the blog post content 
(you may wish to start by copying the index.qmd from an existing blog post).
If you are including an image or two (which is encouraged!) copy them into the blog sub-directory and make sure the index.qmd refers to them.
Once you are done you can compile/render the html, preview/check and publish the webpages (see above).
If you are uncomfortable doing this last step, one of the regular website maintainers/contributors can help or do this for you!
