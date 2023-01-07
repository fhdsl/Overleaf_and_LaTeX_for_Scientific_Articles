
# Writing with Overleaf

Now that you know the advantages of using overleaf and have started working with a template, we will now discuss more about how to make additional modifications to your document.

<img src="04-writing_files/figure-html//1UgGtVn7RsqdQ4pJxDk_dueSyREHcH-uWTNAT27E2mG8_g1c84a339a79_0_39.png" title="Learning Objectives: 1. Recognize some basic LaTeX tags, 2. Recognize how Overleaf offers extra support, 3. Add images to documents, 4. Add references to documents, 5. Identify when there is an Issue. 6. Know how to get help" alt="Learning Objectives: 1. Recognize some basic LaTeX tags, 2. Recognize how Overleaf offers extra support, 3. Add images to documents, 4. Add references to documents, 5. Identify when there is an Issue. 6. Know how to get help" width="100%" style="display: block; margin: auto;" />

## LaTeX Basics

Since we are working with a template, it isn't necessary to learn everything there is to know about writing in LaTeX to get started. However, it can be useful to understand some fundamentals. 

At the top of the template you will notice `\ducumentclass{article}` and a tag called `\usepackage{}` that is repeated several times with different information in the brackets:

<img src="04-writing_files/figure-html//1UgGtVn7RsqdQ4pJxDk_dueSyREHcH-uWTNAT27E2mG8_g1c84a339a79_262_0.png" title="The top of the template shows usepackage several times." alt="The top of the template shows usepackage several times." width="100%" style="display: block; margin: auto;" />
The first tag indicates that we would like to create a scientific article.


The next loads some packages, to allow us to use additional LaTeX features. These will be utalized later in the template. It is recommended that you leave this code as is, and only modify the rest of the template until you understand more about LaTeX. 

You may recall that we previously described how to bold font using `\textbf{bold text}`.

With LaTeX you will be using brackets often to designate what to do with a specific set of text.

Other important functions will be:

- `\section{section name}` - this will help you to create sections in our template. We don't need to do anything to modify the text, it will automatically bold the text and number the sections (1, 2, 3 etc.).

- `\subsection{subsubsection name}` - this will help you to create subsections, these headings will be one level down from the section headings and will be numbered like 1.1, 1.2. 

- `\subsubsection{subsubsection name}` - this will help you to create sections one level down from subsections, these heading will be numbered like 1.1.1, 1.1.2.


In the template you can see how these are formatted. 
