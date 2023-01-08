
# Writing with Overleaf

Now that you know the advantages of using overleaf and have started working with a template, we will now discuss more about how to make additional modifications to your document.

<img src="04-writing_files/figure-html//1UgGtVn7RsqdQ4pJxDk_dueSyREHcH-uWTNAT27E2mG8_g1c84a339a79_0_39.png" title="Learning Objectives: 1. Recognize some basic LaTeX tags, 2. Recognize how Overleaf offers extra support, 3. Add images to documents, 4. Add references to documents, 5. Identify when there is an Issue. 6. Know how to get help" alt="Learning Objectives: 1. Recognize some basic LaTeX tags, 2. Recognize how Overleaf offers extra support, 3. Add images to documents, 4. Add references to documents, 5. Identify when there is an Issue. 6. Know how to get help" width="100%" style="display: block; margin: auto;" />

## LaTeX Basics

Since we are working with a template, it isn't necessary to learn everything there is to know about writing in LaTeX to get started. However, it can be useful to understand some fundamentals, so we will go over most of the commands that you see listed in the template.

### Document Class 

At the top of the template you will notice `\ducumentclass{article}`.

<img src="04-writing_files/figure-html//1UgGtVn7RsqdQ4pJxDk_dueSyREHcH-uWTNAT27E2mG8_g1d07d88c199_0_7.png" title="Documentclass command" alt="Documentclass command" width="100%" style="display: block; margin: auto;" />


This specifies general typesetting information about the type of document that we intend to make. For example, it often specifies font size, the overall layout of the text, and alignment of various features of the text. Since we are writing a scientific article, the specification here is `article`.

To learn more about document classes see this [documentation link](https://libguides.utsa.edu/c.php?g=522165&p=3570198) form @wu_libguides.


### Packages

Next you will see that  `\usepackage{}` is repeated several times with different information in the brackets:

<img src="04-writing_files/figure-html//1UgGtVn7RsqdQ4pJxDk_dueSyREHcH-uWTNAT27E2mG8_g1c84a339a79_262_0.png" title="The top of the template shows usepackage several times." alt="The top of the template shows usepackage several times." width="100%" style="display: block; margin: auto;" />

We will refer to these tags with brackets such as `\usepackage{}` as **commands** from now on (as this is what the are generally referred to) and they cause a change to either the text within the brackets or the overall document.

The next commands install some packages. Packages are additional code to help you do additional things with your documents. If a command comes from a specific package, you will need to install the package that it comes from first. Commands from these packages will be utilized later in the template. It is recommended that you leave this code as is, and only modify the rest of the template until you learn more. 

In addition to determining what commands you can use, packages will also determine how the content is formatted or laid out.


### Author section

You may recall that we previously described how to bold font using `\textbf{bold text}`.
With LaTeX you will be using brackets often to designate what to do with a specific set of text that is contained within the brackets.

<div class = "warning">
If you do not close a set of brackets you will get an error, so be careful about this.
</div>

Next, we see the `\title` command that we previously worked with, as we already modified the text within the brackets to change the title. 


<img src="04-writing_files/figure-html//1UgGtVn7RsqdQ4pJxDk_dueSyREHcH-uWTNAT27E2mG8_g1d07d88c199_0_12.png" title="Recap of the title command" alt="Recap of the title command" width="100%" style="display: block; margin: auto;" />


Then we see the `\author` command to add authors to the paper. These will be formatted in the way that is shown on the template. When you see `\\` two backslashes, this indicates that the line is finished and a new one is to be made. It is best to  [avoid](https://tex.stackexchange.com/questions/225893/what-does-double-backslash-in-latex-mean)  using this for line breaks within the paragraphs that you might include in the paper, but for tables or formatting like the authors, it should work well.

<img src="04-writing_files/figure-html//1UgGtVn7RsqdQ4pJxDk_dueSyREHcH-uWTNAT27E2mG8_g1d07d88c199_0_45.png" title="Double backslash ends a line." alt="Double backslash ends a line." width="100%" style="display: block; margin: auto;" />


We also see another command `\textttt{}` used within the `\author{}` command to change the text to typewriter font.

<img src="04-writing_files/figure-html//1UgGtVn7RsqdQ4pJxDk_dueSyREHcH-uWTNAT27E2mG8_g1d07d88c199_0_67.png" title="The texttt command changes the font within the brackets to typewriter font." alt="The texttt command changes the font within the brackets to typewriter font." width="100%" style="display: block; margin: auto;" />

You may also notice `%% examples of other authors` is in green and does not show up in the rendered document. This is what is called a **comment** and it can be used to write notes about the material.

<img src="04-writing_files/figure-html//1UgGtVn7RsqdQ4pJxDk_dueSyREHcH-uWTNAT27E2mG8_g1d07d88c199_0_79.png" title="The double percent sign %% creates a comment that will not show up in the final document." alt="The double percent sign %% creates a comment that will not show up in the final document." width="100%" style="display: block; margin: auto;" />

In the author section, the `\And` allows for additional authors to be added and needs to be used between each other. 

<img src="04-writing_files/figure-html//1UgGtVn7RsqdQ4pJxDk_dueSyREHcH-uWTNAT27E2mG8_g1d07d88c199_0_31.png" title="In the author section, the And tag allows for additional authors to be added and needs to be used between each other." alt="In the author section, the And tag allows for additional authors to be added and needs to be used between each other." width="100%" style="display: block; margin: auto;" />

Finally, the author section needs to be completed by closing the brackets.


<img src="04-writing_files/figure-html//1UgGtVn7RsqdQ4pJxDk_dueSyREHcH-uWTNAT27E2mG8_g1d07d88c199_0_93.png" title="In the author section, the brackets for the original author command need to be closed." alt="In the author section, the brackets for the original author command need to be closed." width="100%" style="display: block; margin: auto;" />

### Beginning Commands 

The next command `\begin{document}` enables us to format text for the body of the article. If you put `%%` in front of the command to change it to a comment and therefore not use the command, you will see that the document is formatted overall slightly differently. It will be paired with `\end{document}` that you will see at the bottom of the template if you scroll down.


The `\maketitle` will add the title the page where the `begin{document}` command was used. Otherwise, if you used it before `begin{document}`, the title and authors will show up on a separate page first. You can test moving this command around to see how the document changes.


<img src="04-writing_files/figure-html//1UgGtVn7RsqdQ4pJxDk_dueSyREHcH-uWTNAT27E2mG8_g1d07d88c199_0_101.png" title="The begin and maketitle commands specify where certian formatting should occur." alt="The begin and maketitle commands specify where certian formatting should occur." width="100%" style="display: block; margin: auto;" />

### Abstract

The abstract section can be distinguished using the `begin{}` and `end{}` functions just like we used for the body of the document. These two commands will be used later as well to indicate that a specific part of the document has started or ended.


### Section commands:

- `\section{section name}` - This will help you to create sections in our template. We don't need to do anything to modify the text, it will automatically bold the text and number the sections (1, 2, 3 etc.).

- `\subsection{subsubsection name}` - This will help you to create subsections, these headings will be one level down from the section headings and will be numbered like 1.1, 1.2. 

- `\subsubsection{subsubsection name}` - This will help you to create sections one level down from subsections, these heading will be numbered like 1.1.1, 1.1.2.


In the template you can see how these are formatted:

<img src="04-writing_files/figure-html//1UgGtVn7RsqdQ4pJxDk_dueSyREHcH-uWTNAT27E2mG8_g1d07d88c199_0_0.png" title="Example of sections in the template showing how it creates a number and bold text" alt="Example of sections in the template showing how it creates a number and bold text" width="100%" style="display: block; margin: auto;" />

The `\paragraph{}` command works similarly, but it will not be numbered. The text within the brackets is an optional word that is bold to start the paragraph. You can also leave it empty. However, you can specify if you want sections to be not be numbered as well when using an asterisks `*` between the command name and the brackets `section*{}`.

### Dummy text

You may notice that `\lipsum[]` is used to create random chunks of text. The number within the brackets indicates how what specific dummy paragraph to use out of 150.

### Equations

It can be very helpful to include a mathematical equation. To do so we need to use our handy `\begin{equation}` and `\end{equation}` functions to indicate the boundaries. Using `equation` within the brackets indicates that this should be formatted in a certain way. It will center the text nicely and number it.

For more information about mathematical expressions in overleaf see the [Overleaf documentation](https://www.overleaf.com/learn/latex/Mathematical_expressions).


