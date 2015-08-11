## Read Me file for the ARC adapted phd-thesis-template version
#### This is an adapted version of the phd-thesis-template in LaTeX for PhD theses for the University of Cambridge created by Krishna Kumar

### Introduction
This README file gives an overview of the settings you need to change in order to create a thesis file using LaTeX that is deemed acceptable for the Dept of Psychiatry. It is also possible to use Lyx, which is a different LaTeX version with a more interactive interface, but that would require a different file and instructions may slightly differ (please see kks32’s home github page for the Lyx file). These instructions are completely based on the LaTeX version.

First of all, please read the README file created by kks32 so that you have an idea of the structure of the file and how you can change this that are not reported here. Then download the template zip file from [GitHub](https://github.com/kks32/phd-thesis-template/releases/tag/v2.0), but make sure to check for the latest release.

This file will also give examples of tables and longtables (across several pages) in landscape and portrait format and examples of figures, which you can use as a template for your own tables and figures. 

Some general tips: 
1. the percentage symbol “%” is used to comment out lines in LaTeX
2. the backslash “\” is used to start commands
3. two backslashes “\\” are used to insert a line break.
4. any document in LaTeX (outside of the thesis environment) need to always start by specifying the document class, secondly you will load in packages to use, and thirdly you will start the document using “\begin{document}” and you will finish the document with “\end{document}”
5. Google is your friend and knows everything about LaTeX, or well at least where you can find the answers to your questions: [stackoverflow](http://stackoverflow.com) being a great resource and the [LaTeX wikibooks](https://en.wikibooks.org/wiki/LaTeX) another.
6. Anything between dollar signs will automatically be in math mode, e.g. $x + x$

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
  1. document class specifications:
a4paper - keep as is
12pt - keep as is
times - optional, if you prefer fourier font, change “times” to “fourier”
numbered - optional, for referencing, this refers to the numbered referencing style. If you prefer author-year format, change “numbered” to “authoryear”
abstract - is optional and only for when you want to print your thesis title page,the abstract page and declaration page (of which you need to hand in separate copies at the Student Registry)
print - keep
There are several other options such as index, chapter, draft etc., please read about those in the README or in the thesis.tex files
  2. Custom Page Margins - keep as is
  3. Fonts - keep as is
  4. Bibliography style - keep as is
  5. Page Style - keep as is
  6. Preamble - keep as is
  7. Thesis Info & Meta-Data - keep as is if you have already changed your thesis-info.tex file
  8. Abstract Separate - keep as is
  9. Chapter Mode - keep as is, see the thesis.tex/README file for more information
  10. Front Matter - optional, I would suggest leaving the declaration, acknowledgement and abstract commands active, if you would like to add a dedication, keep this active too, if you do not, comment the line out as so “%\include{Dedication/dedication}”
  11. Adding TOC and List of Figures - keep as is
  12. Main Matter - CHANGE. This will include all your chapters, so make sure you add a command for all your chapters.
  13. Back Matter - keep as is
  14. Bibliography - keep as is
  15. Appendices - CHANGE. Include all your appendices here.
  16. Index - keep as is


### Chapter template
Each chapter should be outlined in sections and have a reference to where your figures (.png or .pdf files) can be called from.
Please see below for a generic template and several suggestions on how to put in a reference (will be outlined more below) and a abbreviation, which will automatically be put in the nomenclature abbreviations list. Note that you should only call the nomenclature command for an abbreviation once per chapter, otherwise you will have a double abbreviation in the list.

    %%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%
    %%%%%%%%%%%%%%%% First Chapter %%%%%%%%%%%%%%%%
    %%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%

    % Title of your chapter
    \chapter{Title of your Chapter}
    \label{sec:Chapter1}

    %%%%%%%%%%%%%% Define Graphics Path%%%%%%%%%%%%%%
    \ifpdf
    \graphicspath{{Chapter1/Figures/}}
    \else
    \graphicspath{{Chapter1/Figures/}} % if you only have one path, this should be equal to the first, 
    									% if more than one path different
    \fi

    %%%%%%%%%%%%%%%%% First Section %%%%%%%%%%%%%%%%
    \section{Introduction} % Section - 1.1
    \label{sec:chp1_sec1_intro}

    % Main body text section
    Put some text here on what you are writing about. Maybe you could put in a reference using the bibtex 
    format \citep{bc11_plosbiol}. If you are talking about abbreviations such as deoxyribonucleic acid (DNA)
    \nomenclature[z]{DNA}{Deoxyribonucleic Acid} and magnetic resonance imaging (MRI) 
    \nomenclature[z]{MRI}{Magnetic Resonance Imaging}, you only have to include the nomenclature 
    command once. If you would repeat it when saying DNA and MRI again, then you get an error 
    message.

    \subsection{For equations} % Section 1.1.1
    \label{sec:chp1_sec1.1_forequations}

    If you would like to put equations in your text than you should use the following format.
    
    \begin{equation}
    \label{eq:chp1_eq1}
    y ~ \beta_{y} + \alpha_{z} + \varepsilon_{i}
    \end{equation}

    You can then refer back to your equation \ref{eq:chp1_eq1} and even your sections 
    \ref{sec:chp1_sec1_intro}, so make sure you name them well in order not to get too confused. And if 
    you want to add in a table or a figure, just go ahead and LaTeX will place them appropriately in the text. 

    \section{Conclusion} % Section 1.2
    \label{sec:chp1_sec2_conclusion}
    Just play around with it. You can use the same format for appendices, just called it an appendix instead 
    of a chapter.


### Figure template
I would suggest trying to create your figures in a separate LaTeX document to try out the layout etc before putting it into the Chapter’s main body of text.

If you do try this in a separate document, you first need to specify the following commands. 

    % Specify document class
    \documentclass[12pt]{article}

    % Load packages
    \usepackage{graphicx}
    \usepackage{subcaption}

NOTE, these commands are not necessary if you are using the figure in the chapter#.tex file.

Now we begin the figure example format. I have chosen an example where I combined both images and graphs in one figure. This means that I used the command [“subfigure”](https://en.wikibooks.org/wiki/LaTeX/Floats,_Figures_and_Captions).

I always recommend putting your figure in a “group” so that it is nicely formatted in the text.

    %Begin document
    \being{document}
    
    % Start group and figure
    \begingroup
    \begin{figure}[!ht] % !ht has something to do with the centring of the table
      \centering % I like to use indents to make distinctions between commands and how they relate to each other
    % note: an empty line creates a line break (enter) in the figure environment

      \begin{subfigure}[b]{0.48\textwidth} % This means that the figure will be 48\% of the of the text width. 
    									% The reason for choosing this amount is because I want two 
    									% sets of figures to fit next to each other on the page. If you only 
    									% have one figure you could chose the figure to be “\textwidth”
        \includegraphics[width = \textwidth]{“path to figure”}
        \includegraphics[width = \textwidth]{“path to figure”}
        \caption{\footnotesize{“subtitle”}} % I prefer the text within my figure to be smaller than the main text
        \label{“figure label”}
      \end{subfigure}
    ~
      \begin{subfigure}[b]{0.48\textwidth} 
        \includegraphics[width = \textwidth]{“path to figure”}
        \includegraphics[width = \textwidth]{“path to figure”}
        \caption{\footnotesize{“subtitle”}} 
        \label{“figure label”}
      \end{subfigure}
    ~

    \caption[Figure Short Caption]
    {Figure Long Caption \\
    \footnotesize{Figure legend text
    }}

    \label{fig:fig#_chp#_title}
    % You use the label for referring to your table in the text so make it easy and understandble


    % End figure and group environments
    \end{figure}
    \endgroup

    % End document class
    \end{document}


### Table templates
There are several ways of creating tables in LaTeX. You can use the tabularx package for normal tables, however this package will not work for tables that go across several pages. The package that you need for those kinds of tables is longtable. In addition, the package lscape will be able to put your table in a landscape format. 

As the margins of your thesis are set, you should keep these in mind when building your tables. I found that a maximum table size of 14cm width works well for portrait tables and 20cm width works well for landscape tables. I would suggest keeping all your tables the same width to keep consistency in your formatting. Furthermore, if you have several long tables spanning several pages, I would suggest using the longtable package for all your tables, including those that do not span several pages as tabularx leads to slightly different formatting than longtable when compiled in the thesis document.

As for figures, I would suggest trying to create your tables first in a separate LaTeX document to try out the layout etc before putting it into the Chapter’s main body of text. If you do try this in a separate document, you first need to specify the following commands. 

    % Specify document class
    \documentclass[12pt]{article}

    % Load packages
    \usepackage{longtable}
    \usepackage{lscape}
    \usepackage{tabularx}
    \usepackage{booktabs}

NOTE, these commands are not necessary if you have the table in the chapter#.tex file. And again, I always recommend putting your table in a “group” so that it is nicely formatted in the text.

## The longtable portrait example format. 
This [longtable](ftp://ftp.dante.de/tex-archive/macros/latex/required/tools/longtable.pdf) should come out as a working example in LaTeX. It has 9 rows, space for notes and abbreviations at the bottom of the table, and has three rows for column headings, as used for sub-columns. The & sign is the separator between columns. Try running this example in LaTeX and play around with it so you understand what all the little commands mean. For a table that spans over 2 pages, try adding on 20 more lines of main body table content (just copy paste as an example) to see the full effect of the longtable package.


    % Begin document
    \begin{document}
    
    % Start group and table
    \begingroup

      \centering
      \footnotesize # As with figures, I prefer to have my tables in a smaller font than the main text

    \begin{longtable}{p{4.1cm} p{1.8cm} p{1.2cm} p{1cm} p{1cm} p{1cm} p{1cm}} \\ % never exceed 14cm in total

    \caption{\mbox{Your table title}} \\
    \label{tab:tab#_chp#_title_shortcut} \\

    % First Head
    \toprule
    	&	&	\multicolumn{5}{l}{Language differences} 
    % the 5 indicates that the column spreads over 5 columns, the “l” indicates that the text is leftward
    \cmidrule(l{3pt}){3-7}
    	&	&	\multicolumn{3}{l}{Controls}		&	\multicolumn{2}{l}{Autism} \\
    \cmidrule(r{3pt}){3-5}	\cmidrule(r{3pt}){6-7}
    Structure	&	Test	&	$F$ 	&	$t$	&	$p$	&	$t$	&	$p$ \\
    \midrule
    \endfirsthead

    % Head
    \multicolumn{7}{l}
    {\tablename\ \thetable\ — \textit{Continued from previous page}} \\

    \midrule
    	&	&	\multicolumn{5}{l}{Language differences} 
    \cmidrule(l{3pt}){3-7}
    	&	&	\multicolumn{3}{l}{Controls}		&	\multicolumn{2}{l}{Autism} \\
    \cmidrule(r{3pt}){3-5}	\cmidrule(r{3pt}){6-7}
    Structure	&	Test	&	$F$ 	&	$t$	&	$p$	&	$t$	&	$p$ \\
    \midrule
    \endhead

    % Foot
    \midrule
    \multicolumn{7}{p{14cm}}{\scriptsize{Notes: put some text here.}} \\
    \multicolumn{7}{p{14cm}}{\sciptsize{Abbreviations: put your abbreviations here.}} \\
    \midrule
    \multicolumn{7}{r}{\textit{Continued on next page}} \\
    \endfoot

    % End Last Foot
    \midrule
    \multicolumn{7}{p{14cm}}{\scriptsize{Notes: put some text here.}} \\
    \multicolumn{7}{p{14cm}}{\sciptsize{Abbreviations: put your abbreviations here.}} \\
    \bottomrule
    \endlastfoot

    % Main body table (which you can easily make in excel and copy over)
    Brain region	&	Outcome	&	5.3	&	7.4	&	0.04	&	6.4	&	0.05 	\\
    Brain region	&	Outcome	&	5.3	&	7.4	&	0.04	&	6.4	&	0.05 	\\
    Brain region	&	Outcome	&	5.3	&	7.4	&	0.04	&	6.4	&	0.05 	\\

    \\[-4.8ex] & & & & \\
    Brain region	&	Outcome	&	5.3	&	7.4	&	0.04	&	6.4	&	0.05 	\\
    Brain region	&	Outcome	&	5.3	&	7.4	&	0.04	&	6.4	&	0.05 	\\
    Brain region	&	Outcome	&	5.3	&	7.4	&	0.04	&	6.4	&	0.05 	\\
    Brain region	&	Outcome	&	5.3	&	7.4	&	0.04	&	6.4	&	0.05 	\\
    Brain region	&	Outcome	&	5.3	&	7.4	&	0.04	&	6.4	&	0.05 	\\
    Brain region	&	Outcome	&	5.3	&	7.4	&	0.04	&	6.4	&	0.05 	\\

    % End longtable and group
    \end{longtable}
    \endgroup

    % End document
    \end{document}


## The longtable landscape example format. 

    % Begin document
    \begin{document}
    
    % Start group, landscape and table
    \begingroup
    \begin{landscape}

      \centering
      \footnotesize # As with figures, I prefer to have my tables in a smaller font than the main text

    \begin{longtable}{p{4.5cm} p{1.5cm} p{1.5cm} p{1.5cm} p{1.5cm} | p{1.5cm} p{1.5cm} p{1.5cm} p{1.5cm}} \\ 
    % never exceed 20cm in total

    \caption{\mbox{Your table title}} \\
    \label{tab:tab#_chp#_title_shortcut} \\

    % First Head
    \toprule
    	&	&	\multicolumn{4}{c}{\textbf{Females (N=100)}} 	& \multicolumn{4}{c}{\textbf{Males (N=100)}} \\
    \cmidrule(2-9}
    Region	&	Mean	&	St. Dev.	&	Min	&	Max	& Mean	&	St. Dev.	&	Min	&	Max	\\
    \midrule
    \endfirsthead

    % Head
    \multicolumn{9}{l}
    {\tablename\ \thetable\ — \textit{Continued from previous page}} \\
    \midrule
    	&	&	\multicolumn{4}{c}{\textbf{Females (N=100)}} 	& \multicolumn{4}{c}{\textbf{Males (N=100)}} \\
    \cmidrule(2-9}
    Region	&	Mean	&	St. Dev.	&	Min	&	Max	& Mean	&	St. Dev.	&	Min	&	Max	\\
    \midrule
    \endhead

    % Foot
    \midrule
    \multicolumn{9}{p{20cm}}{\scriptsize{Notes: put some text here.}} \\
    \multicolumn{9}{p{20cm}}{\sciptsize{Abbreviations: put your abbreviations here.}} \\
    \midrule
    \multicolumn{9}{r}{\textit{Continued on next page}} \\
    \endfoot

    % End Last Foot
    \midrule
    \multicolumn{9}{p{20cm}}{\scriptsize{Notes: put some text here.}} \\
    \multicolumn{9}{p{20cm}}{\sciptsize{Abbreviations: put your abbreviations here.}} \\
    \bottomrule
    \endlastfoot

    % Main body table (which you can easily make in excel and copy over)
    \multicolumn{9}{l}{\textit{Global volumes}} \\
    Brain region	&	200	&	15	&	185	&	215	&	250	&	25	&	225	&	275	\\
    Brain region	&	200	&	15	&	185	&	215	&	250	&	25	&	225	&	275	\\
    Brain region	&	200	&	15	&	185	&	215	&	250	&	25	&	225	&	275	\\

    \\[-4.8ex] & & & & \\
    \multicolumn{9}{l}{\textit{Regional volumes}} \\
    Brain region	&	200	&	15	&	185	&	215	&	250	&	25	&	225	&	275	\\
    Brain region	&	200	&	15	&	185	&	215	&	250	&	25	&	225	&	275	\\
    Brain region	&	200	&	15	&	185	&	215	&	250	&	25	&	225	&	275	\\

    % End longtable, landscape and group
    \end{longtable}
    \emd{landscape}
    \endgroup

    % End document
    \end{document}


### Referencing
I used the bibtex format for referencing, see the [wikipage](https://en.wikibooks.org/wiki/LaTeX/Bibliography_Management) for more information on referencing as well. This format requires you to have a references.bib file in the folder References. In the references.bib file you have all your references in the bibtex format. You can easily export references to the bibtex format from EndNote, Papers, Mendeley, Zotero, etc. Obviously not all reference managers will have all your references in the same format, e.g. titles can be in any of these formats:

- Sex Differences In The Brain: Implications for Explaining Autism
- Sex differences in the brain: Implications for explaining autism % I prefer this format
- SEX DIFFERENCES IN THE BRAIN: IMPLICATIONS FORE EXPLANING AUTISM

So you need to check all your references for these tiny inconsistencies. Similarly author names could different too so be sure to check those and journal names as well:

- Baron-Cohen, Simon and Knickmeyer, Rebecca C and Belmonte, Matthew K
- Baron-Cohen, S and Knickmeyer, R C and Belmonte, M K 
I prefer the latter format as some journals do not give full names


One thing is that you need to link each of references to a specific code. I usually use nameyear_journalabbreviation. 
For examples  on whole references see below.

    @article{bc05_science,
    author = {Baron-Cohen, S and Knickmeyer, R C and Belmonte, M K},
    title = {{Sex differences in the brain: Implications for explaining autism}},
    journal = {Science},
    year = {2005},
    volume = {310},
    number = {5749},
    pages = {819—823}
    }

    @book{bc04_book,
    author = {Baron-Cohen, S and Lutchmaya, S and Knickmeyer, R},
    title = {Prenatal Testosterone in Mind: Amniotic Fluid Studies}},
    publisher = {MIT Press},
    year = {2004}
    }


