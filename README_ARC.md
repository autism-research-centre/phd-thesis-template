## Read Me file for the ARC adapted phd-thesis-template version
#### This is an adapted version of the phd-thesis-template in LaTeX for PhD theses for the University of Cambridge created by Krishna Kumar

### Introduction
This README file gives an overview of the settings you need to change in order to create a thesis file using LaTeX that is deemed acceptable for the Dept of Psychiatry. It is also possible to use Lyx, which is a different LaTeX version with a more interactive interface, but that would require a different file and instructions may slightly differ (please see kks32’s home github page for the Lyx file). These instructions are completely based on the LaTeX version.

First of all, please read the README file created by kks32 so that you have an idea of the structure of the file and how you can change this that are not reported here. Then download the template zip file from [GitHub](https://github.com/kks32/phd-thesis-template/releases/tag/v2.0), but make sure to check for the latest release.

This file will also give examples of tables and longtables (across several pages) in landscape and portrait format and examples of figures, which you can use as a template for your own tables and figures. 

Some general notes: 
1. the percentage symbol “%” is used to comment out lines in LaTeX
2. the backslash “\” is used to start commands
3. two backslashes “\\” are used to insert a line break.
4. any document in LaTeX (outside of the thesis environment) need to always start by specifying the document class, secondly you will load in packages to use, and thirdly you will start the document using “\begin{document}” and you will finish the document with “\end{document}”

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

### Structure of the thesis documentation layout
After you have unzipped the file downloaded from kks32, the folder will have several files called “thesis” in different file formats. The only “thesis” file you are interested in is the thesis.tex file. 
Furthermore, there will be folders for each chapter and appendix and folders for abstract, declaration, references, etc. Please adhere to this folder structure.

In each chapter folder you should find a file called chapter#.tex, and chapter#.aux, e.g. chapter1.tex and chapter1.aux. Again, you are only ever interested in the .tex files. Depending on how you want to add in your figures, you may also have a folder within your chapter folder called “Figures”.

### Changes to the front page
The file thesis-info.tex holds the front page information. Please see below for the changes to be made. Change the following in the file thesis-info.tex:

1. Enter your title on line 3. Note, if your title has capital letters other than at the start of the sentence, e.g. uses abbreviations like MRI or DNA, make sure your entire title is in between double curly brackets. e.g. \title{{Brain structure in ASC measured using MRI}}. If you do not put these between double curly brackets, they will be printed as lowercase. 
2. You can also give a subtitle on line 9, but leave this option blank or comment it out using a % if you do not have a subtitle.
3. Change the author name on line 12 to your full name (including middle names etc)
4. Change the department of “Department of Psychiatry” on line 15
5. Change your College affiliation on line 30
6. Optional to change your meta-information to keywords associated with your thesis.
7. You do not have to set the submission date, this is automatically done when you compile your entire document.


### Changes to the formatting
The files thesis.tex and preamble.tex set information such as the referencing style, font, margins, which LaTeX packages you want to use etc. These are some of the options that I have played with/changed/added. For all the items I have changed, I will give the defaults and then the options for changing them.

1. The folder Preamble holds the file preamble.tex, just open it using TeXShop or TeXworks.
  1. Custom Margin - Keep as is. These are the settings as required by the Student Registry for margin spacing.
  2. Fonts - Optional. The standard font is _Times_ I believe, however, I liked the _Fourier_ font much better as formulas were better readable. However, that is of course your choice. If you like the standard font, do not change anything. If you want to change your font to fourier, uncomment out line 20 to make the command “\RequirePackage{helvet}” active. You will also need to change a command in the thesis.tex file but I will come back to that.
  3. The following sections are are part of “Custom Packages”, you can change things as you like, I will recommend the addition of certain packages but this can be altered to your needs.
  4. Algorithms and Pseudocode - Keep as is
    1. Captions and Hyperreferencing / URL - Keep as is
    2. Graphics and Figures - Keep as is
    3. Tables - Optional. Uncomment the lines for “\usepackage(long table}” and “\usepackage{tabular}”. Add a line with the command: \usepackage{lscape} (this is the package for landscape formatted tables). The package multicol is for using tables with multiple columns in one row, so if you want to build a table with exactly that, you should uncomment that line as well.
    4. SI Units - Optional
I had some trouble getting the right maths fonts, especially since I used the fourier font. So in addition to the siunitx package I also added the following packages, one per line: \usepackage{amsfonts}; \usepackage{amsmath}; \usepackage{amssymb}
    5. Line Spacing - Keep as is
    6. Formatting/Footnote - Keep as is
  5. Bibliography - Keep as is
  6. User Defined Commands and all its subcomponents - Keep as is

2. thesis.tex can be found in the main folder.
2.1 document class specifications:
a4paper - keep as is
12pt - keep as is
times - optional, if you prefer fourier font, change “times” to “fourier”
numbered - optional, for referencing, this refers to the numbered referencing style. If you prefer author-year format, change “numbered” to “authoryear”
abstract - is optional and only for when you want to print your thesis title page,the abstract page and declaration page (of which you need to hand in separate copies at the Student Registry)
print - keep
There are several other options such as index, chapter, draft etc., please read about those in the README or in the thesis.tex files
2.2 Custom Page Margins - keep as is
2.3 Fonts - keep as is
2.4 Bibliography style - keep as is
2.5 Page Style - keep as is
2.6 Preamble - keep as is
2.7 Thesis Info & Meta-Data - keep as is if you have already changed your thesis-info.tex file
2.8 Abstract Separate - keep as is
2.9 Chapter Mode - keep as is, see the thesis.tex/README file for more information
2.10 Front Matter - optional, I would suggest leaving the declaration, acknowledgement and abstract commands active, if you would like to add a dedication, keep this active too, if you do not, comment the line out as so “%\include{Dedication/dedication}”
2.11 Adding TOC and List of Figures - keep as is
2.12 Main Matter - CHANGE. This will include all your chapters, so make sure you add a command for all your chapters.
2.13 Back Matter - keep as is
2.14 Bibliography - keep as is
2.15 Appendices - CHANGE. Include all your appendices here.
2.16 Index - keep as is



