## How to write a data driven paper using Curvenote, Jupyterlab, and Overleaf
… a short note and a tutorial (this is version 1, I will continue to update this note over time, please feel free to leave your comments ….)
Curvenote, Jupyterlab, and Overleaf when used in concert solve a major pain point in moving from an analysis, reporting, and publishing in a pipeline. In this paper, I am going to explore the possibilities for not only working personally as a pipeline for productivity, but over and above, we will explore that we can build in commenting and collaboration the process. So, let's take a look at Curvenote, Jupyterlab, and Overleaf in turn.

The process runs as follows:
One way:
- Start with Jupyterlab (self-hosted, hosted on your server, Google Colab, Deepnote, etc)
- Run the analyses
- Save the file as ipynb file
- Upload the ipynb file to Curvenote filespace
- Write the paper in Curvenote by adding paragraphs of text, and citations through DOIs
- Export the blocks or the entire paper into LateX
- Upload LaTeX to Overleaf
- Process Overleaf with addtional referencing, tables etc

These are too many steps for the first time, but if these can be streamlined, it would allow for a productive workflow for not only writing data driven papers and creating a publishing workflow but also help in keeping copies of paper in different spaces and channeling in different creative ways.
That said, it is possible to move the workflow in other ways but usually start with either Curvenote OR Jupyter notebook depending on what you prefer: if your preference is to write a more or less text based paper, then start with Curvenote and finish off in Overleaf. If on the other hand, if you want to work with a data analysis driven paper, then work with Jupyter first, pull the tables and figures in Curvenote, and then push the LaTeX file to Overleaf and finish.
Step 0: Set up accounts
I assume that you have created free accounts in three services, if not, these are step 0
Curvenote: if you have not created an account, you can do so here: https://www.curvenote.com
Jupyter Notebooks with lab: If you want, there are several choices, we will work with Google Colab notebooks: https://colab.research.google.com
Overleaf: you can create free account here: https://www.overleaf.com

Step 1: start with Curvenote
A few concepts of writing with Curvenote deserve mention:
Curvenote works with "Blocks", so we work with blocks
Blocks make up "Articles"
Articles make up a "Project"
When you create an account with Curvenote, you organise in reverse order: so you start with a Project, then start an article within a project, and then within an article, start writing within blocks
Each block is version-able, so you can save different versions of different blocks
You can work in different versions of the blocks and update collaboratively
If you want to copy and paste blocks either within a long article or across articles in the same projects or across articles across projects, you will need to do something like as follows:
Copy the URL of the block
Where you want to place this block, select to import the block
Then, either you can 'remove' or delete the old block or keep the old block depending on your preference

You write in the block using markdown and what you write gets instantly converted to a wysiwyg format in the block itself, which, I find very useful. There are a few things to keep in mind:
You cannot do [description](url) to insert a hyperlink, you will need to use the formatting bar or right click on the app to insert a hyperlink
You cannot do ![description](image url) to insert an image in a block
You will need to insert image as a separate block by directly dragging an image into where you want to insert the image
You cannot insert a markdown table in the block directly, but you can insert a markdown table as a text or code block (I know, not the same thing), but you will need to insert as a block from your ipynb file that you insert in Curvenote. This means you will need to create all tables in Python/R etc.
All citations that you want to insert in Curvenote should have a DOI associated with them. This means you can search by DOIs. You can get the DOI for your article using https://crossref.org if you do not have the DOI of the article for some reason. For the same reason, you will not be able to cite books etc, automatically, but this is why you will need Overleaf for using with your bibtex file

Step II: Use jupyter labs with curvenote
First, install curvenote google chrome add-on: Curvenote has a Jupyter notebook Chrome add-on that will work with Google Chrome, Vivaldi, Brave etc Chromium based browsers. Install this from here:
Jupyter Versioning & Comments - by Curvenote
Add comments, cell and notebook versioning and real-time collaboration to JupyterLab and Notebooks, provided by…chrome.google.com
If you work with your hosted Jupyter lab or JupyterLab in your computer, it will insert several buttons etc into your jupyterlab that you can use for interacting with your Curvenote document.
Note that this extension will not work with Google Colab or Deepnote or Kaggle Workspace etc, i.e., any service that has modified your Jupyter lab environment.
Second, develop your analyses in Jupyter lab. As you analyse or after you complete your analysis, download the ipynb file and upload the file to your project as a separate "article". If you use Google Add-on, you can directly import or save the versions.
At that point, your tables and visualisations that you have prepared in your Jupyter notebooks are all ready to be imported as blocks into Curvenote as separate blocks. However note that such blocks will not be _editable_ within Curvenote. You can only edit them in Jupyter Notebooks/jupyter lab environment.
You are now ready to move from Curvenote to Overleaf. In Curvenote, export the "entire" article as LaTeX; or you can export individual "blocks" as LaTeX documents. The two approaches are somewhat different, hence Overleaf. Here are the differences:
If you export the Article, it will export a zip file which you will need to unzip to use with Overleaf
If you export individual blocks you can use them directly in Overleaf

Step III: from Curvenote to Overleaf
In Overleaf, start a project and give it whatever name you want to give. In that project, create a "blank" document. Now, depending on what you exported, you do one of the two things:
If you exported the entire article and unzipped the zip file, then select ALL the files of the unzipped folder, and
upload the files into the filespace of Overleaf
Set the index.tex file as the main file to process in Overleaf
Edit the various blocks to remove the images folder from the text OR, if you have manually created an image folder in the filespace within Overleaf and moved images there, then, you are all set
At that point, use Overleaf as you will normally do.

The advantage of using Overleaf with Curvenote are:
You will not have to install pandoc or any tool for conversion.
You can do jupyter nbconvert in Jupyter notebook and then upload it to Overleaf but you will see that the code that Curvenote provides you is very clean and intuitive
You can iteratively edit your text and files in Curvenote, and upload in Overleaf; Curvenote's WYSIWYG editor is easier to work with than Overleaf's wysiwyg editor but YMMV.

Endpiece
This is a quick introduction to how to use the three tools in tandem to write a data analysis driven document and publish it. There are several other things to do with this workflow that I will subsequently write about. Give it a try and I am interested to see how you use this workflow.
