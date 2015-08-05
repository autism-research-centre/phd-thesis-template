## Read Me file for the ARC adapted phd-thesis-template version
#### This is an adapted version of the phd-thesis-template in LaTeX for PhD theses for the University of Cambridge created by Krishna Kumar

### Introduction
This README file gives an overview of the settings you need to change in order to create a thesis file using LaTeX that is deemed acceptable for the Dept of Psychiatry. It is also possible to use Lyx, which is a different LaTeX version with a more interactive interface, but that would require a different file and instructions may slightly differ (please see kks32’s home github page for the Lyx file). These instructions are completely based on the LaTeX version.

First of all, please read the README file created by kks32 so that you have an idea of the structure of the file and how you can change this that are not reported here. Then download the template zip file from GitHub (https://github.com/kks32/phd-thesis-template/releases/tag/v2.0), but make sure to check for the latest release.

This file will also give examples of tables and longtables (across several pages) in landscape and portrait format and examples of figures, which you can use as a template for your own tables and figures. 

Note that I will be adding more instructions to this file over the next few weeks.
I hope that this helps and if you have any questions or would like to add/correct anything, please feel free to commit a change or send me an email (ar560@cam.ac.uk).

Amber


### Softwares to use for editing
The LaTeX software you use will depend on your OS. The ones that I have used are listed below. 

For Mac:
- Download TeX for Mac 
- TeXShop editor

For Windows:
- Download TeX for Windows
- TeXworks editor, very useful and easy editor. I recommend this editor for creating figures, tables, and setting up my initial chapters **_NOTE_ if you use TexWorks to edit your chapters in the files provided by the template, do not run these but just save them**, more on this later.
- TeXstudio editor, more advanced editor. I recommend this editor to compile the final thesis document.

### Structure of the thesis documentation layout.
Coming soon...

### Changes to the front page
The file thesis-info.tex holds the front page information. Please see below for the changes to be made.

Change the following in the file thesis-info.tex:
1. Enter your title on line 3. Note, if your title has capital letters other than at the start of the sentence, e.g. uses abbreviations like MRI or DNA, make sure your entire title is in between double curly brackets. e.g. \title{{Brain structure in ASC measured using MRI}}. If you do not put these between double curly brackets, they will be printed as lowercase. 
2. You can also give a subtitle on line 9, but leave this option blank or comment it out using a % if you do not have a subtitle.
3. Change the author name on line 12 to your full name (including middle names etc)
4. Change the department of “Department of Psychiatry” on line 15
5. Change your College affiliation on line 30
6. Optional to change your meta-information to keywords associated with your thesis.
7. You do not have to set the submission date, this is automatically done when you compile your entire document.



