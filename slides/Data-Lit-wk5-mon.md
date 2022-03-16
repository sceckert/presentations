
## Agenda



## What is text encoding



### What is a tag?

There are three kinds of tags:

+ opening, or beginning, tags: `<title>`
+  closing, or end, tags: `</title>`
+  empty tags: `<pagebreak/> `or `<pb/>`

Note:
Once material is transferred to a computer text editor, the text is encoded by placing tags around portions of the text. These tags identify characteristics of the material and determine how it will display and function on the Internet. Tags may indicate where a title is located, that a passage is rendered italics, that a word is misspelled, where a table or image is placed, where links are located, and so forth.



### What is an element?

Example:

`<title>The Souls of Black Folk</title>` 


Example:

`<title>The Souls of Black Folk<subtitle>Essays and Sketches </subtitle> </title>`

Note:
An element refers to a section of text bound by a pair of opening and closing tags.



### What is an attribute ?

Example:

`<title rend="italic">The Souls of Black Folk</title>`

The rend="italic" attribute signifies that the title should be rendered in italics: *The Souls of Black Folk*

Note:
An attribute modifies or further describes an element and appears only in the beginning tag.



## What is HTML?

<section>
  <pre><code><script type="text/template">
	<!DOCTYPE html>
	<html>
	<body>
	<h1> This is header </h1>
	<p> This is a paragraph </p>
	<p> Paragraph with a <a href="https://sceckert.github.io/Data-and-Literary-Study-Spring2022/">link.</a></p>
 	</body>
	</html> 
  </script></code></pre>
</section>



## What is XML? What is Text Encoding?

XML = eXtensible Markup Language


The Text Encoding Initiative(TEI) set out standards for encoding machine-readable texts of interest in the humanities and social sciences.

XML files encoded according to these standard look like this:

<section>
  <pre><code><script type="text/template">
<TEI version="3.3.0" xmlns="http://www.tei-c.org/ns/1.0">
 <teiHeader>
  <fileDesc>
   <titleStmt>
    <title>The Souls of Black Folk</title>
   </titleStmt>
	<docAuthor>W. E. BURGHARDT DU BOIS</docAuthor>
	<pubPlace>CHICAGO</pubPlace>
	<publisher>A. C. McCLURG & CO.</publisher>
	<docDate>1903</docDate>
  </fileDesc>
 </teiHeader>
 <text>
  <front>
   <div1 type="forethought">
	<head> The Forethought</head>
	<p>HEREIN lie buried many things which if read with patience may show the strange meaning ..... 
	</p>
  </front>
<body>
</body>
 </text>
</TEI>
</script></code></pre>
</section>


Note:
Text encoding is a process whereby documents are transferred to an electronically searchable format for scholarly research.

TEI includes tags that are specific to a particular genre - drama, poetry, prose.



### Exercise: Encoding Du Bois's epigraphs

Open up the following Jupyter notebook:
https://mybinder.org/v2/gh/sceckert/Data-and-Literary-Study-Spring2022/main?urlpath=lab/tree/_week5/in-class-practicum-mon-wk5.ipynb


https://www.loc.gov/pictures/search/?st=grid&co=anedub

Ex image: https://www.loc.gov/pictures/resource/ppmsca.33884/?co=anedub

https://www.loc.gov/resource/rbc0001.2013gen06011/?sp=5&r=-1.224,-0.006,3.449,1.517,0