# LaTeX

You may or may not have heard people talking about [LaTeX](https://www.latex-project.org/about/) (pronounced '/ˈlɑːtɛx/' LAH-tekh or '/ˈleɪtɛx/' LAY-tekh), which is not to be confused with the the material latex (pronounced '/ˈleɪtɛks/' LAY-tekhs). In this course we will explain what LaTeX is and how it came to be.


<img src="02-latex_files/figure-html//1UgGtVn7RsqdQ4pJxDk_dueSyREHcH-uWTNAT27E2mG8_g1be15cb26d3_0_0.png" alt="LaTex is not latex (the material used for protective gloves and other items)." width="100%" style="display: block; margin: auto;" />

## Learning Objectives

<img src="02-latex_files/figure-html//1UgGtVn7RsqdQ4pJxDk_dueSyREHcH-uWTNAT27E2mG8_g1bb9ca840c8_0_360.png" alt="Learning Objectives: 1. Explain what LaTeX is and how it came to be 2. Understand that writing a document involves two distinct steps 1) writing the content and 2) determining how the content should be displayed, 3. Recognize that applications like microsoft word interactively show you the formatting/arrangement of the document as you write, while markup languages embed how a file should display using specific tags within the text that are later manifested, 4.Begin to understand how markup language tags result in changes in how text is displayed" width="100%" style="display: block; margin: auto;" />

## Document Preparation System

LaTeX is a "document preparation system" according to the LaTeX project [@latex]. It is often used to write scientific or technical documents, but it can be used for formatting or arranging any type of document. This process of determining the final look of a writing product is called [typesetting](https://en.wikipedia.org/wiki/Typesetting). 

<div class = "dictionary">
Typesetting determines how text looks and where it is located in a document when it is its final stage - like when it is rendered or printed. It refers to fonts, text sizing, line spacing, the arrangement of tables and images, and more.
</div>

Although LaTeX has a reputation for being quite tricky, it is very powerful in enabling users to create documents with complex and customized text formatting and layouts much more easily than doing so with systems like Microsoft Word. 


<img src="02-latex_files/figure-html//1UgGtVn7RsqdQ4pJxDk_dueSyREHcH-uWTNAT27E2mG8_g1be15cb26d3_0_18.png" alt="LaTeX allows for fancy document typesetting (meaning formatting and text layout), where as traditional text editors like Microsoft Word requires manual formatting and layout, which often leads to typical looking documents." width="100%" style="display: block; margin: auto;" />
 



## History

LaTeX was originally released in 1984 by [Leslie Lamport](https://en.wikipedia.org/wiki/Leslie_Lamport). LaTeX is one of several programs (but probably the most widely used in academia - in part, because it is free!) that makes it easier to use the [typesetting](https://en.wikipedia.org/wiki/Typesetting) system called TeX.


<details><summary> **Why is it called LaTeX?**</summary>
<div class = "why">
The "La" is believed to be for Lamport's last name. <br>
The "Tex" is for the typesetting system Tex.
</div>
</details>


### TeX

TeX (pronounced '/ˈtɛx/' tekh) is a typesetting system developed by [Donald E. Knuth](https://en.wikipedia.org/wiki/Donald_E._Knuth) in the 1970s to help him format the text in his books more to his satisfaction [@tex_2022]. 

<details><summary> **Why is it called Tex?**</summary>
<div class = "why">
Tex is named as an abbreviation for the Greek word [τέχνη (ΤΕΧΝΗ techn)](https://en.wikipedia.org/wiki/Techne), which directly translates to art or craft [@tex_2022].
</div>
</details>

<br>

Typesetting has origins in how documents used to be printed using manual stamping mechanisms, where someone would provide the contents of the text in writing by hand that would be translated to a version with the intended layout and style for printing.


<img src="02-latex_files/figure-html//1UgGtVn7RsqdQ4pJxDk_dueSyREHcH-uWTNAT27E2mG8_g1be15cb26d3_0_45.png" alt="Historically making printed documents required two steps: 1. Writing the content by hand, 2. Determine the layout and font and arrangement of the text with stamps." width="100%" style="display: block; margin: auto;" />


Overtime this process got replaced by digital options and eventually resulted in the concept of WYSIWYG (What you see is what you get), where programs like Microsoft Word let you interactively work with the typesetting of a document as you write the content. 


<img src="02-latex_files/figure-html//1UgGtVn7RsqdQ4pJxDk_dueSyREHcH-uWTNAT27E2mG8_g1be15cb26d3_0_67.png" alt="WYSIWYG - What you see is what you get - the document is displayed like the final product as you write it." width="100%" style="display: block; margin: auto;" />


When you use a program like Microsoft Word, you are essentially giving it two sets of directions simultaneously, one which is the content of the text, and one which is the style and layout of the text. 

With LaTeX we are more aware that we are actually telling the computer how to arrange the text. It also gives us much more control of how we arrange, format, and style the text. If you are interested in taking a deep dive into how this all came to be, check out this [blog post](https://towardsdatascience.com/why-should-you-learn-latex-or-at-least-give-it-a-try-8d0f3218b8e) by @tirado_reasons_2020 and this [O'Reilly book](https://www.oreilly.com/library/view/making-tex-work/1565920511/) by @walsh_making_1994.

## Process

LaTeX can also be called a [markup language](https://en.wikipedia.org/wiki/Markup_language). These means that certain text tags can be used to indicate how the content text should be formatted or displayed. Another markup language is HTML (which actually stands for HyperText Markup Language), which has text tags to indicate how the content text should be displayed on webpages. It is often used in computer science to enable humans to read or write files more easily and for computers to interpret these files more easily. 

Let's use a simple example of making some text **bold** to illustrate this. 

**Microsoft Word:** <br>
If we wanted to some text bold in Microsoft Word, we would type the plain text that we want to bold just like the rest of the text. We would then select that text and click some buttons to make the text bold. 

**HTML:**<br>
In HTML we could instead use `<b>` at the beginning of the text we want to bold, and `</b>` at the end to indicate that this text should be bold when it is rendered into it's final state. 

**LaTeX:**<br>
Just like in HTML, LaTeX also uses text around the actual content text to describe how to produce the final product. In this case, we would indicate that we want bold text using a tag `\textbf` with brackets around the text we want to change like so: `\textbf{bold text}`.

<img src="02-latex_files/figure-html//1UgGtVn7RsqdQ4pJxDk_dueSyREHcH-uWTNAT27E2mG8_g1babf2134b3_0_153.png" alt="A table of the methods just described to bold text to indicate that text around the plain text is used to format the text itself within markup languages." width="100%" style="display: block; margin: auto;" />

As you can see, LaTeX will feel a bit different from writing in Microsoft Word, as we will be using text tags to define how we want the content text to look.

## Benefits of LaTeX

Now that you are a little more clear about what LaTeX is, it might be easier to appreciate it's benefits:

1) Allows you to focus on the content and worry less about formatting (once you have a good template to work with). There are many specific templates to use format documents for various goals, such as formatting manuscripts for scientific journals.
2) Allows for much more customization for complex typesetting/formatting of text.
3) Once you have a template you like working with, say for a journal you frequently publish with, it is super easy to format future similar documents.
4) If you need to change the typesetting/formatting of a document for the requirements of a different journal or preprint archive, you can do it much more quickly and with more ease than if you were to do it manually using a text editor like Microsoft Word. 
5) You can add languages with different alphabets or mathematical notation with much more ease than with traditional text editors
6) You can collaborate with people who use LaTeX more easily

<img src="02-latex_files/figure-html//1UgGtVn7RsqdQ4pJxDk_dueSyREHcH-uWTNAT27E2mG8_g1be15cb26d3_0_77.png" alt="Benefits of Using LaTeX: Using a template allows you to focus on the content and not the formatting/layout, Can create very complex documents, Can reproduce style/typesetting of a document easily again, Can easily change the typesetting of an entire document, Can add languages with other alphabets or mathematical notation easily, If you know LaTeX you can collaborate with others who use it!" width="100%" style="display: block; margin: auto;" />

## Conclusion

We hope that this chapter has given you some more knowledge about what LaTeX is and how it came to be, as well as the benefits of using it.

Here are some of the major take-home messages:

1. Computers actually separate document creation into two tasks, creating the content text and arranging and styling that text. Traditional text editors like Microsoft Word show us what the final document will look like as we write it.
2. LaTeX is a document preparation system that makes it easier to use the typesetting system TeX and allows you to create very complicated documents. 
3. Typesetting has to do with all the style, layout, and formatting that a document might need.
4. LaTeX is a markup language and similar to HTML. Text tags around the content text can be used to indicate how the document should look when rendered into the final state.
5. LaTeX allows you to more easily change how your document is laid out, which can be super beneficial if you need to accommodate different scientific journal requirements. 
6. Although LaTeX is used frequently in computer science, mathematics, statistics, and engineering fields to write technical papers, it can be used for other kinds of documents too!

