
# Figure, tables, and citations oh My!

No that you know some of the basics about how to add text to a template, we want to help you add other elements that are important for scientific communication, like adding figures and images, adding tables, and adding references/citations. In this next chapter, we will introduce how to do this in LaTeX/Overleaf.

<img src="05-elements_files/figure-html//1UgGtVn7RsqdQ4pJxDk_dueSyREHcH-uWTNAT27E2mG8_g1d07d88c199_0_131.png" title="Learning Objectives: 1. Add figures and images to documents, 2. Add references and citations to documents, 3. Add tables to documents, 4. Create internal links back to a figure, table, reference or section" alt="Learning Objectives: 1. Add figures and images to documents, 2. Add references and citations to documents, 3. Add tables to documents, 4. Create internal links back to a figure, table, reference or section" width="100%" style="display: block; margin: auto;" />

You will notice that the template has a few examples of each of these elements and we will walk through these now. 

## Figures and Images

Most scientific articles have figures, so it is helpful to know how to add these to documents. There are two main steps involved in this once you have a figure file that you are ready to add, say a PNG or a JPEG file.

When you add a figure in LaTeX you will use the `\begin{}` and `end{}` functions just like you have done previously. However, this time the you will use `\begin{figure}` and `\end{figure}` to tell Overleaf that this is the type of element you are creating.

If you focus on the second figure in the template, which is probably all you will need to learn (the first figure is a box created in LaTeX), then you will notice that in addition to the `\begin{figure}` and `\end{figure}`  commands, there is a `\centering{}`command, which will align the figure to the center of the page. The `includegraphics{text.png}` portion of the code actually adds the figure into the document. 

<img src="05-elements_files/figure-html//1UgGtVn7RsqdQ4pJxDk_dueSyREHcH-uWTNAT27E2mG8_g1c91f28435b_0_4.png" title="Example of the code for a figure when you have a png file to use." alt="Example of the code for a figure when you have a png file to use." width="100%" style="display: block; margin: auto;" />

<div class = "notice" > 
Note that comments with one percent sign can be used after code - thus the `% picture` is just telling you that this part of the code is adding a picture. People use different numbers of percent signs based on preference and convention, but just one percent sign is sufficient to turn anything following that into a comment. 
</div>
 
You may notice on the left side of the template in overleaf that there are a few files listed, including the name of the image file used in the code for the figure: `test.png`. The `template.tex` file is the file we have been working in.

<img src="05-elements_files/figure-html//1UgGtVn7RsqdQ4pJxDk_dueSyREHcH-uWTNAT27E2mG8_g1c91f28435b_0_9.png" title="The template.tex file is the file we have been working in. You can see it in the left menu." alt="The template.tex file is the file we have been working in. You can see it in the left menu." width="100%" style="display: block; margin: auto;" />

If you click on the name of the image file you will see a preview of the image.

<img src="05-elements_files/figure-html//1UgGtVn7RsqdQ4pJxDk_dueSyREHcH-uWTNAT27E2mG8_g1c91f28435b_0_19.png" title="Location of the image file called test.png in the left menu." alt="Location of the image file called test.png in the left menu." width="100%" style="display: block; margin: auto;" />

<details><summary> **What are these other files?**</summary>
<div class = "notice">
The **template.tex** file is the file we have been working in that contains the main document  content text and code to format the text.
The **`reference.bib`** file contains the bibliography information that will be used by the template.tex file.
The **`README.md`** file will tell you more about the template that you are using. <br>
The **`arxiv.sty`** file is a style file that contains code more specifically style the document  for arXiv preprints. This code is then applied in our `template.tex` file (the one we have been working in) by the command \usepackage{arxiv}, because that is the name of the `.sty` file. 
</div>
</details>


To upload a new image to add a new figure, you can click on the new file button which has an icon that looks like a piece of paper with the right upper corner folded.

<img src="05-elements_files/figure-html//1UgGtVn7RsqdQ4pJxDk_dueSyREHcH-uWTNAT27E2mG8_g1c91f28435b_0_27.png" title="New file button" alt="New file button" width="100%" style="display: block; margin: auto;" />

Then select the upload button to drag and drop a new image file from your computer.

<img src="05-elements_files/figure-html//1UgGtVn7RsqdQ4pJxDk_dueSyREHcH-uWTNAT27E2mG8_g1c91f28435b_0_33.png" title="Menu for uploading a file.." alt="Menu for uploading a file.." width="100%" style="display: block; margin: auto;" />

Then to add this new figure to your document you would just need to modify the code above so that the name of the image file matched you uploaded.

`\begin{figure} % picture`<br>
`.   \centering`<br>
`.   \includegraphics{new.png}`<br>
`\end{figure}`<br>

## Tables 

Similar to figures, you need the `\begin{}` and `\end{}` commands in you file to designate where the instructions for your table begin and end. In this case we use table with `\begin{table}` and `\end{table}`. 

Here is all of the code to create the following table. We will go through each command and what it does to create the table.


<img src="05-elements_files/figure-html//1UgGtVn7RsqdQ4pJxDk_dueSyREHcH-uWTNAT27E2mG8_g1c91f28435b_0_38.png" title="All the code for the table." alt="All the code for the table." width="100%" style="display: block; margin: auto;" />


<img src="05-elements_files/figure-html//1UgGtVn7RsqdQ4pJxDk_dueSyREHcH-uWTNAT27E2mG8_g1c91f28435b_0_105.png" title="The resulting table" alt="The resulting table" width="100%" style="display: block; margin: auto;" />



We can add a caption using the `\caption{}` command. The table number will automatically be determined by the order of the tables. Like before with the figure, the `\centering` command will then align the resulting table to be centered.

<img src="05-elements_files/figure-html//1UgGtVn7RsqdQ4pJxDk_dueSyREHcH-uWTNAT27E2mG8_g1c91f28435b_0_43.png" title="The caption command adds the table title." alt="The caption command adds the table title." width="100%" style="display: block; margin: auto;" />





Then to create the table in the template we will first indicate how we want the table arranged using the `tabular` environment. The command `\begin{tabular}{lll}` indicates that we will have three columns that are left aligned. 

<img src="05-elements_files/figure-html//1UgGtVn7RsqdQ4pJxDk_dueSyREHcH-uWTNAT27E2mG8_g1c91f28435b_0_63.png" title="The caption command adds the table title." alt="The caption command adds the table title." width="100%" style="display: block; margin: auto;" />



- The `\toprule` command adds a solid line at the top of the table. If you add this command again you will see two lines - test it out to see how it works!

<img src="05-elements_files/figure-html//1UgGtVn7RsqdQ4pJxDk_dueSyREHcH-uWTNAT27E2mG8_g1c91f28435b_0_77.png" title="The toprule command adds a line to the top of the table after the title." alt="The toprule command adds a line to the top of the table after the title." width="100%" style="display: block; margin: auto;" />


- The command `\multicolumn{2}{c}{Part}\\` indicates that will will merge some columns together to create a "multicolumn" in this case the `{2}` means we will merge together 2 columns, the `{c}` indicates that it will be center aligned and the `{Part}` is the text we want for this. We need the `\\` to finish that row, otherwise "Part" will end up on the next row.

<img src="05-elements_files/figure-html//1UgGtVn7RsqdQ4pJxDk_dueSyREHcH-uWTNAT27E2mG8_g1c91f28435b_0_94.png" title="The multicolumn command allows you to create text that spans across multiple columns." alt="The multicolumn command allows you to create text that spans across multiple columns." width="100%" style="display: block; margin: auto;" />

The `\cmidrule` command adds the line or "rule" under the multicolumn that says "Part". This command creates lines that are not the full width of the table. The `(r) {1-2}` indicates that the line should be trimmed on the right side to leave a gap after the span of 2 column widths.   

<img src="05-elements_files/figure-html//1UgGtVn7RsqdQ4pJxDk_dueSyREHcH-uWTNAT27E2mG8_g1c91f28435b_0_112.png" title="The cmidrule command adds the line or rule under the multicolumn that says Part." alt="The cmidrule command adds the line or rule under the multicolumn that says Part." width="100%" style="display: block; margin: auto;" />

Now we are ready to put some text within our table cells. to do so we can simply type the words with an `&` in between the text for each cell to indicate where the column breaks are. The `\\` indicates when we are done with that row. Since we have a special character to represent mu, we can use mathematical notation by using a dollar sign `$`.

<img src="05-elements_files/figure-html//1UgGtVn7RsqdQ4pJxDk_dueSyREHcH-uWTNAT27E2mG8_g1c91f28435b_0_122.png" title="Adding text within the tables requires an &amp; to indicate different cells within the table." alt="Adding text within the tables requires an &amp; to indicate different cells within the table." width="100%" style="display: block; margin: auto;" />


To add a line under these values we can use the `\midrule` command.

<img src="05-elements_files/figure-html//1UgGtVn7RsqdQ4pJxDk_dueSyREHcH-uWTNAT27E2mG8_g1c91f28435b_0_145.png" title="Adding lines to specific parts of the middle of the table requires the midrule command." alt="Adding lines to specific parts of the middle of the table requires the midrule command." width="100%" style="display: block; margin: auto;" />

To add more text within the rows after this line, we can do this similarly to before with the `&` indicating column breaks and the `\\` indicating the end of the row. The `$` is also used to create mathematical notations.

<img src="05-elements_files/figure-html//1UgGtVn7RsqdQ4pJxDk_dueSyREHcH-uWTNAT27E2mG8_g1c91f28435b_0_159.png" title="The contents of the table for these rows can be added similar to the one above where the &amp; creates column divisions and the $ creates mathematical notations. The double backslash is need for each row to end the row." alt="The contents of the table for these rows can be added similar to the one above where the &amp; creates column divisions and the $ creates mathematical notations. The double backslash is need for each row to end the row." width="100%" style="display: block; margin: auto;" />
To add the line at the bottom, we need to use a command that is similar to `toprule{}` and `midrule{}`- which is `bottomrule{}`.


<img src="05-elements_files/figure-html//1UgGtVn7RsqdQ4pJxDk_dueSyREHcH-uWTNAT27E2mG8_g1c91f28435b_0_159.png" title="The contents of the table for these rows can be added similar to the one above where the &amp; creates column divisions and the $ creates mathematical notations. The double backslash is need for each row to end the row." alt="The contents of the table for these rows can be added similar to the one above where the &amp; creates column divisions and the $ creates mathematical notations. The double backslash is need for each row to end the row." width="100%" style="display: block; margin: auto;" />

Now we just need to finish off our table.

First we need to get out of the tabular mode, and  we need our trust `\end{}`function to do so with `\end{tabular}` and to end the table overall with `\end{table}`. We will discuss what the `\lab{}` function does soon.


<img src="05-elements_files/figure-html//1UgGtVn7RsqdQ4pJxDk_dueSyREHcH-uWTNAT27E2mG8_g1c91f28435b_0_159.png" title="The contents of the table for these rows can be added similar to the one above where the &amp; creates column divisions and the $ creates mathematical notations. The double backslash is need for each row to end the row." alt="The contents of the table for these rows can be added similar to the one above where the &amp; creates column divisions and the $ creates mathematical notations. The double backslash is need for each row to end the row." width="100%" style="display: block; margin: auto;" />
To add the line at the bottom, we need to use a command that is similar to `toprule{}` and `midrule{}`- which is `\bottomrule{}`.


<img src="05-elements_files/figure-html//1UgGtVn7RsqdQ4pJxDk_dueSyREHcH-uWTNAT27E2mG8_g1c91f28435b_0_178.png" title="The end function is used to stop the tabular mode and to finish the table." alt="The end function is used to stop the tabular mode and to finish the table." width="100%" style="display: block; margin: auto;" />


## Creating internal links

You may have noticed a command `\label{}` when looking through the template.
This is a very helpful command that helps you to create a tag to refer back to when you have a figure or a section header that you want to refer to. There is a nifty command `\ref{}` that helps you create these references. However, it is a tiny bit tricky, so we will walk through a couple of examples.

You need the `\ref{}` command to match up with exactly what you have listed for the `\label{}` command for whatever figure, table, or section you are referring to.

You also need to have the same notation for each type:
- `tab:` for tables
- `fig:` for figures
- `sec:` for section headers

<img src="05-elements_files/figure-html//1UgGtVn7RsqdQ4pJxDk_dueSyREHcH-uWTNAT27E2mG8_g1c91f28435b_0_190.png" title="The end function is used to stop the tabular mode and to finish the table." alt="The end function is used to stop the tabular mode and to finish the table." width="100%" style="display: block; margin: auto;" />

Here we show how to do the same thing for a section of text. We will create a new link for the introduction. To do so we first need to add a label to the introduction using the `label{}` function. We will call it `intro` and we need to specify that this is a section header with `sec` , like so: `label{sec:intro}`.

We then need to refer to this in the same way somewhere else using the `ref{}` function, like so: `ref{sec:intro}`. This will create a link to that section.

<img src="05-elements_files/figure-html//1UgGtVn7RsqdQ4pJxDk_dueSyREHcH-uWTNAT27E2mG8_g1c91f28435b_0_233.png" title="To create a link to the introduction, which is section 1, we can apply the same method using the sec tag." alt="To create a link to the introduction, which is section 1, we can apply the same method using the sec tag." width="100%" style="display: block; margin: auto;" />

## References

Ok, now pretty much all scientific articles need references. To add these we need to add to the `references.bib` file, which can again be found on the left menu. 

There are many ways to get the bib version of a reference, one easy way is to use [Zotero](https://www.zotero.org/), which is a free tool for writing bibliographies that has a [chrome extension](https://chrome.google.com/webstore/detail/zotero-connector/ekhagklcjbdpajgpjgmbionohlpdbjgc?hl=en). 

The cool think about the chrome extension is if you are viewing an article or a website online, you can often right click to add the file to Zotero.

Then you can find the file in Zotero and right click to export the item to BibTeX format. This is a bibliography format that is compatible with `TeX`. We can then copy and paste this into the `references.bib` file, being careful to make sure that the brackets are closed.

Then the first part of the bib item will indicate what to refer to it in the text to create a citation to the reference. The first item that starts with an `@` in the template `references.bib` file shows `kour2014real` as the first thing in the brackets. We can see that line 100 uses the `\cite{}` function to cite this article, as well as another article.

This results in a number and a link to the reference.


<img src="05-elements_files/figure-html//1UgGtVn7RsqdQ4pJxDk_dueSyREHcH-uWTNAT27E2mG8_g1c91f28435b_0_241.png" title="To create a citation, use the cite command and be sure that you update your bib file." alt="To create a citation, use the cite command and be sure that you update your bib file." width="100%" style="display: block; margin: auto;" />


To add a bibliography, we can just undo the comment in front of the  bibliography command. This is sufficient to create the bibliography. The code after this in the template to create each reference individually is not needed.


<img src="05-elements_files/figure-html//1UgGtVn7RsqdQ4pJxDk_dueSyREHcH-uWTNAT27E2mG8_g1c91f28435b_0_248.png" title="To add a bibliography, we can just undo the comment infront of the  bibliography command. This is sufficient to create the bibliography if we have a .bib file. " alt="To add a bibliography, we can just undo the comment infront of the  bibliography command. This is sufficient to create the bibliography if we have a .bib file. " width="100%" style="display: block; margin: auto;" />

## Conclusion

We hope that this chapter has given you some guidance about how to start adding images, tables, internal links, references and citations to your document.

In conclusion, here are some of the major take-home messages:

1. Many of these elements require the `\begin{}` and `\end{}` function to indicate where the element starts and finishes.
1. Images can be added by first uploading an image file to Overleaf and using the `\begin{figure}`, `\includegraphics{imagfileename.png}`, and `\end{figure}` at minimum.
1. Tables can be quite tricky, but you can control basically every aspect about how a table looks which can be really powerful. Remember to start with `begin{table}` and end with `\end{table}`, this helps add a new number to each of your tables when they are automatically numbered.
1. the `\begin{tabular}` function helps you to start a table. It can also help you define the overall width and default alignment.
1. Table content within cells can be delineated with an `&` to indicate column breaks. The `\\` is needed to end a row.
1. To refer to a table, figure, or section of text you can use the `\label{}` and `\ref{}` commands, but make sure that the label is the same and that you use `tab` for table, `fig` for figure, and `sec` for section.
1. The `\references.bib` file of the template can be modified to add different or additional references. These can come from using Zotero to get a BibTeX version of the reference.
1. To cite a paper within the document you can use the `\cite{}` command. 
1. To add the bibliography we can just use the command that was in comments `bibliography{references}`. 

