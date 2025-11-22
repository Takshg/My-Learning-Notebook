# Develop documentation and reports in RStudio

---

# Documentation and reports

**Key Points:**

- **What is R Markdown?**
    - A file format for creating dynamic documents with R.
    - Combines code, text, and output for a comprehensive report.
    - Useful for sharing and reproducing analysis.
- **Benefits of R Markdown:**
    - Improves collaboration by providing a shared language for data analysis.
    - Enhances consistency and reproducibility of analysis.
    - Facilitates knowledge sharing through reports.
- **Components of an R Markdown Document:**
    - Code chunks: sections of code that can be executed and displayed.
    - Comments: explanations and notes about the code and analysis.
    - Text: narrative and explanations of the findings.
- **Creating an R Markdown Document:**
    - Use the `rmarkdown::render()` function to create the report.
    - Choose the desired output format (e.g., HTML, PDF).
- **Exporting the Report:**
    - Export the report to various formats for sharing and distribution.
    - Options include HTML, PDF, Word, and more.

**Definitions:**

- **R Markdown:** A file format that combines code, text, and output for creating dynamic reports.
- **Code Chunk:** A section of code within an R Markdown document that can be executed and displayed.
- **Collaboration:** Working together on a project or task.
- **Reproducibility:** The ability to recreate the results of an analysis.
- **Knowledge Sharing:** The process of sharing information and expertise with others.

**Additional Notes:**

- R Markdown is a valuable tool for data analysts and anyone who wants to share their analysis in a clear and concise way.
- The video provides a good overview of the basics of R Markdown, but there are many more features and capabilities to explore.
- For further learning, you can refer to the R Markdown documentation and other online resources.

**Real-Life Example:**

Imagine you are a data analyst working for a marketing team. You have conducted an analysis of customer data to understand their purchasing behavior. You can use R Markdown to create a report that summarizes your findings and includes visualizations of the data. This report can be shared with your team and stakeholders to inform decision-making.

---

# Overview of R Markdown

[index (83).mp4](Develop%20documentation%20and%20reports%20in%20RStudio%20e02c06a1f0bd4eaab19f090fbebaf411/index_(83).mp4)

**Key Points:**

- **Importance of Documentation:** As a data analyst, documenting your work is crucial for sharing your analysis with others and ensuring its reproducibility.
- **R Markdown:** A file format for creating dynamic documents with R, combining code and reports to share every step of your analysis.
- **Benefits of R Markdown:**
    - **Easy to use:** No need to leave RStudio to create reports.
    - **Improved understanding:** Stakeholders and team members can easily understand your analysis and conclusions.
    - **Feedback and improvement:** Feedback from others can help you improve your analysis.
    - **Multiple output formats:** Convert R Markdown documents to HTML, PDF, Word, slide presentations, and dashboards.
- **Markdown Syntax:** A simple formatting language for plain text files, making it easy to write and format text.
- **R Notebook:** An interactive option within R Markdown that allows users to run your code and view the resulting graphs and charts.
- **Alternatives to R Markdown:** Jupyter, Kaggle, and Google Colab notebooks offer similar functionalities.

**Definitions:**

- **Data Analyst:** A professional who collects, analyzes, and interprets data to extract meaningful insights and inform decision-making.
- **Stakeholder:** An individual or group with an interest in the outcome of a project or analysis.
- **Markdown:** A lightweight markup language for formatting text on the web.
- **HTML:** HyperText Markup Language, the code used to create web pages.
- **Notebook:** An interactive document that combines code, results, and visualizations.

---

# R Markdown resources

**R Markdown** is a useful tool that allows you to save and execute code, and generate shareable reports for stakeholders. As you learn more about how to use it, it can be helpful to bookmark some resources to refer to later.

This reading explores some great online resources that will help you learn more about R Markdown and how to use it to document your analysis.

## R Markdown documentation

RStudio's [R Markdown documentation](https://rmarkdown.rstudio.com/lesson-1.html) includes a series of tutorials that will help you learn about the main features of R Markdown, including code chunks, output formats, notebooks, interactive documents, and more. The tutorials include online lessons that you can complete directly in your RStudio Cloud workspace.

## R Markdown reference materials

RStudio has developed a reference guide and a cheat sheet that you can bookmark and use whenever you practice writing R Markdown files.

- The [R Markdown Reference Guide](https://rstudio.com/wp-content/uploads/2015/03/rmarkdown-reference.pdf?_ga=2.49295910.1034302809.1602760608-739985330.1601281773) contains three sections: Markdown syntax, knitr chunk options, and Pandoc options. The guide is super detailed and includes tons of examples and explanations so that you can easily find the exact information you need to customize your R Markdown documents.
- The [R Markdown Cheat Sheet](https://rmarkdown.rstudio.com/lesson-15.html) is a convenient summary of the different steps and workflow processes for R. It also includes sections with abbreviated explanations of knitr and pandoc chunk options, and other useful information to review or look up while you work.

## R for Data Science book

For a well-organized introduction to the basics of R Markdown, check out the [Communicate](https://r4ds.had.co.nz/communicate-intro.html) section of the **R for Data Science** book. It covers the main features and functions of R Markdown, the various output formats, and the workflow for combining text and code to create an analysis notebook.

## R Markdown: The Definitive Guide

If you want to really explore the capabilities of R Markdown in a systematic way, [R Markdown: The Definitive Guide](https://bookdown.org/yihui/rmarkdown/) provides a comprehensive guide to the R Markdown ecosystem. This book contains four main parts:

1. [Part I](https://bookdown.org/yihui/rmarkdown/installation.html) explains how to install the relevant packages and offers an overview of R Markdown, including the syntax for Markdown and code chunks.
2. [Part II](https://bookdown.org/yihui/rmarkdown/documents.html) provides detailed documentation of the built-in output formats included in R Markdown, like document formats and presentation formats.
3. [Part III](https://bookdown.org/yihui/rmarkdown/dashboards.html) shares several R Markdown extension packages that allow you to build different applications or generate output documents with different styles.
4. [Part IV](https://bookdown.org/yihui/rmarkdown/parameterized-reports.html) covers advanced topics in R Markdown.

---

# Jupyter notebooks

**Jupyter notebooks** are documents that contain computer code and rich text elements – such as comments, links, or descriptions of your analysis and results. You will find them used in a variety of online tools, including Project Jupyter, Kaggle, and Google Colaboratory ("Colab" for short). These notebooks can be executable documents that you can run to perform an analysis.

Jupyter notebooks can come in handy with everything from data cleaning and transformation, to statistical modeling and visualizations. They are compatible with R, so you can consider them as an alternative to R Markdown. And just like R Markdown documents, you can easily share Jupyter notebooks with team members and stakeholders.

## Jupyter notebooks in Kaggle

If you are working in Kaggle, there are two types of notebooks available: Jupyter notebooks and scripts (including R Markdown scripts). For more information, refer to the [How to Use Kaggle Notebooks](https://www.kaggle.com/docs/notebooks) page.

## Jupyter notebooks in Google Colab

Google Colab is a product from Google Research. Colab is a hosted Jupyter notebook service that requires no setup to use.  For more information, refer to the [Welcome to Colaboratory](https://colab.research.google.com/notebooks/intro.ipynb) page.

## Additional resources

To learn more about Jupyter notebooks, check out these resources:

- [**Project Jupyter**](https://jupyter.org/): This is the home of Jupyter notebooks, as well as JupyterLab – the web-based interactive development environment for Jupyter notebooks, code, and data.
- [**Jupyter Notebook: An Introduction**](https://realpython.com/jupyter-notebook-introduction/): This detailed introduction of Jupyter notebooks comes from the people at Real Python, a tutorial-based site devoted to all things Python. You can take a video course or follow the written tutorial to get started with Jupyter notebooks and learn about its features and capabilities.

And, just like R Markdown, Jupyter notebooks include basic formatting tools and rules that will help you keep your work organized and user-friendly. In fact, Jupyter uses R Markdown as its language for writing and formatting text in a notebook.

To learn about basic formatting in Jupyter notebooks, check out these resources:

- [**The Jupyter** **Notebook](https://jupyter-notebook.readthedocs.io/en/stable/notebook.html):** This resource provides an overview of Jupyter notebooks, including information about the structure of the user interface and notebook document. You’ll also learn about the basic workflow for using a notebook document, along with information about keyboard shortcuts and other features that will help you format your work.
- [**Using Jupyter Notebook for Writing](https://gtribello.github.io/mathNET/assets/notebook-writing.html):** This resource focuses on how to use Markdown to format your writing in a Jupyter notebook. Use this as a guide to manage the syntax of your writing, including making titles and subtitles and adding links.
- [**The Jupyter Notebook Formatting Guide**](https://medium.com/analytics-vidhya/the-jupyter-notebook-formatting-guide-873ab39f765e): This resource includes a wide variety of formatting options for Jupyter notebooks. You’ll learn about the basics as well as some more advanced options, like embedding PDF documents and videos.

After you know how to apply basic formatting to your notebooks, you can start exploring more advanced options.

---

# Using R Markdown in RStudio

[index (84).mp4](Develop%20documentation%20and%20reports%20in%20RStudio%20e02c06a1f0bd4eaab19f090fbebaf411/index_(84).mp4)

**Key Points:**

- R Markdown is a tool for documenting your data analysis at any stage, especially when you've completed a project.
- It allows you to combine code, text, and results in a single document.
- You can use R Markdown to create reports that are easy to share with others, even if they don't have experience with R.

**Definitions:**

- **R Markdown:** A file format that combines R code, text, and results into a single document.
- **Knitting:** The process of converting an R Markdown file into a report.
- **HTML:** A markup language used to create web pages.

**Steps for Using R Markdown:**

1. Install the R Markdown package.
2. Create a new R Markdown file.
3. Add your code, text, and results to the file.
4. Knit the file to create a report.

**Benefits of Using R Markdown:**

- **Improved documentation:** R Markdown makes it easy to document your analysis, including your code, results, and conclusions.
- **Increased reproducibility:** R Markdown files can be easily shared and reproduced, making it easier for others to understand and verify your work.
- **Enhanced communication:** R Markdown reports are easy to read and understand, even for people who don't have experience with R.

**Additional Notes:**

- The video lecture also covers how to use R Markdown to create more complex reports, including reports with multiple sections and figures.
- There are many resources available online for learning more about R Markdown.

**Real-Life Examples:**

- A data analyst could use R Markdown to document their analysis of a customer satisfaction survey.
- A researcher could use R Markdown to create a report on their findings from a clinical trial.
- A student could use R Markdown to create a presentation for their statistics class.

---

# Hands On Activity: Your R Markdown notebook

## Activity overview

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/TOqxzuNFR2eqsc7jRVdnKg_a3c6611d874f403a923e10406b4f38a9_image4.png?expiry=1717200000000&hmac=OB7LVwPbT3kQVCn21rKPfKCUU17B6iuI-upb7lbmN-8)

Earlier in this course, you worked on activities that were presented in an R Markdown (Rmd) file format. Data analysts use this file format to make dynamic documents—called notebooks—with R. In this activity, you’ll copy the analysis you did in a past activity into your own R Markdown notebook.

By the time you complete this activity, you will know how to create R Markdown documents to record your analysis in R. This will allow you to keep track of your data analysis process and share your work  with others.

## Get started with R Markdown

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/TOqxzuNFR2eqsc7jRVdnKg_a3c6611d874f403a923e10406b4f38a9_image4.png?expiry=1717200000000&hmac=OB7LVwPbT3kQVCn21rKPfKCUU17B6iuI-upb7lbmN-8)

R Markdown is a file format for making dynamic documents with R. These documents, also known as notebooks, are records of analysis that help you, your team members, and stakeholders understand what you did in your analysis to reach your conclusions. You can publish a notebook as an html, pdf, or Word file, or in another format like a slideshow.

At any point during this activity, you can consult the [R Markdown Cheat Sheet](https://rstudio.com/wp-content/uploads/2015/02/rmarkdown-cheatsheet.pdf). This resource is a reference guide for all things R Markdown: from opening a file to publishing a final report of your analysis.

## Select and review your analysis

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/TOqxzuNFR2eqsc7jRVdnKg_a3c6611d874f403a923e10406b4f38a9_image4.png?expiry=1717200000000&hmac=OB7LVwPbT3kQVCn21rKPfKCUU17B6iuI-upb7lbmN-8)

In this course, you’ve had the chance to practice and save files of your analysis in RStudio. To get started, open up an analysis that you have saved.

You can use **Open File** in the **File** menu:

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/JgIuf9hvQKWCLn_YbwCltQ_596b59d217374f7386914b53503ce504_Screenshot-2021-03-10-7.47.46-PM---Display-2.png?expiry=1717200000000&hmac=oNi24iBjRCgk2t2SrI8_eaJq8kQ23YwjRcvKlAHuEKI)

Now, review the file you opened. Examine the data you pulled from and the functions you used to analyze it.

When you create an R Markdown notebook, you want to be able to share it with others so they can understand your process and conclusions. You may also want to keep it for your own records as a way to keep track of your progress using R for analysis.

## Open an Rmd file

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/TOqxzuNFR2eqsc7jRVdnKg_a3c6611d874f403a923e10406b4f38a9_image4.png?expiry=1717200000000&hmac=OB7LVwPbT3kQVCn21rKPfKCUU17B6iuI-upb7lbmN-8)

Now, you’ll transfer the code from the file you opened to a new R Markdown file so that you can write your own explanation of the steps you took. By doing this, you can create a more complete record of your overall thought process so that others will be able to understand it.

1. Open a new R Markdown (Rmd) file to begin building the basic structure of your notebook. Select **File** -> **New File** -> **R Markdown**.

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/fgmuRsa3Re-JrkbGtzXv7Q_f079db26f46a4345a8ebb99f716625ba_Screenshot-2021-03-10-7.50.54-PM---Display-2.png?expiry=1717200000000&hmac=sctS6G4iTztv4k9eZ_uxmSd3a_hLgXK0f0-aM2vByes)

2. In the dialog box that opens, add a title for your notebook. Name it something that will help you easily recognize what your analysis is about (e.g., “Penguins Plots”).

3. Type your name in the Author field.

4. For now, leave the file in the recommended html output format. When you render the file later, it will appear as an html report. You can always change it to a pdf or Word file later.

5. Click **OK.** An R Markdown file will appear in a new tab in the script viewer pane. You should now have two tabs: one for the new Rmd file and one for your analysis. You can toggle back and forth between them when you need to by clicking on the tab you want to access.

## Format your notebook

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/TOqxzuNFR2eqsc7jRVdnKg_a3c6611d874f403a923e10406b4f38a9_image4.png?expiry=1717200000000&hmac=OB7LVwPbT3kQVCn21rKPfKCUU17B6iuI-upb7lbmN-8)

The first part of your notebook is the YAML header section. YAML is a language used in data files to improve human readability, and the YAML header section exists to provide information about a document to the humans reading it. RStudio automatically populates this section with the information you provide and other general information, such as the date you create the file.

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/1hhWKyfhSNaYVisn4bjWuA_bed45ecd7a9b47f1bf8a21a1db13c4d5_Screenshot-2021-02-26-4.01.09-PM.png?expiry=1717200000000&hmac=b_Y9WI4dElmzpi0PARzB9369jDimIM23adJp27teyM4)

You can change the information in this section at any time by adding text or by typing over the current text. Notice that each line has a number associated with it. That makes it easy to reference a location in the notebook and also for you to track where you make changes in the notebook.

The next section with the gray background is a code chunk. You encountered these each time you ran a chunk of code during the activities in this course.

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/p-8hY-HQRlevIWPh0OZXfw_714d2a8da1c949c3bdc84fa221bc8a29_Screenshot-2021-03-10-7.52.32-PM---Display-2.png?expiry=1717200000000&hmac=3dGaArqhDYjtshHcy5r6Ci6kDwVGPd6Wa9e97ULjUD4)

Again, RStudio automatically populates the notebook with this formatted default code chunk. This chunk basically means that your code will be shown in your final report when you’re ready to render it.

All code chunks begin and end with delimiters. To start a code chunk, you can type three tick marks followed by a lowercase “r” in curly brackets: **```{r}**

To end it, type just the three tick marks: **```**

There are two shortcuts to adding code. On your keyboard, you can press **Ctrl** + **Alt** + **I** (PC) or **Cmd** + **Option** + **I** (Mac). Or you can click the **Add Chunk** command in the editor toolbar:

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/F_1SaX9PSDG9Uml_T7gxwg_dd380c2b87ea4dfab8bf5254a82a8c32_Screenshot-2021-03-10-7.53.57-PM---Display-2.png?expiry=1717200000000&hmac=-8cjC1hvayOzjEoVPGQad9uWdTKTQKKiYvLfxkjIpQY)

To add a code chunk to your Rmd file, follow these steps:

1. Click the end of the last line of your Rmd file. Use either of the previously-mentioned shortcuts to create a code chunk.

2. Press **Enter** (Windows) or **Return** (Mac) two or three times after the default code chunk to create space between the existing code chunk and the next code chunk you will add.

3. Copy the code from the analysis file you opened earlier and paste it in the gray area between the beginning and ending delimiters.

4. Select the rest of the template content in the file and delete it. This gives you a blank space to work in to help avoid potential errors from mixing your own comments and code with the pre-existing ones in the template.

The white background is where you will type plain text with markdown syntax. As you learned earlier in this course, markdown is a syntax for formatting plain text files. Using markdown makes it easier to write and format text in your notebook.

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/SLXsoIcbReK17KCHG-Xiyw_fe5492e9221a46cd8275c9e299be6498_pasted-image-0-1-.png?expiry=1717200000000&hmac=z6pAHdmyyoht-hB4OPXQib7rJoZkyNOISardo08glIk)

Here are some basic formatting options:

- To start a new paragraph, end a line with two spaces
- To apply italics to a word or phrase, place an asterisk at the beginning and at the end of the word or phrase, for example, *italics works*
- To apply bold to a word or phrase, place two asterisks at the beginning and at the end of the word or phrase, for example, **bold is useful**
- To create a header, type a hashtag (#) followed by a space and your text for example: # Getting Started with R Markdown

When creating headers keep the following in mind:

- Headers will appear in blue
- A single hashtag is the largest header
- The more hashtags you add (up to six), the smaller the header

To format comments in your notebook, follow these steps:

1. Click in a line above the code chunk you added but below the YAML section.

2. Type a main header for your report using a single hashtag. You might want to restate the title in the YAML in a different way or add to it with a short description.

3. Add a smaller header below that to label the first part of your programming. Follow that with a description of the code chunk that you added.

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/9puENBerT_KbhDQXq4_yJQ_a083f6f5a4cd45aeb562fdb3a2b45c96_unnamed-11-.png?expiry=1717200000000&hmac=FjBJV1_PHjf8dQ4IYTneTpK9D2eFILUZK8WhsIuYwGc)

Tick marks format the text to appear as code even though the text is not in a code chunk. The tick marks in the code above create a gray background behind “tidyverse” and “palmerpenguins.”

## Continue formatting

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/TOqxzuNFR2eqsc7jRVdnKg_a3c6611d874f403a923e10406b4f38a9_image4.png?expiry=1717200000000&hmac=OB7LVwPbT3kQVCn21rKPfKCUU17B6iuI-upb7lbmN-8)

Keep working on your formatting until you have at least three levels of headers and more descriptions for your analysis. At any point, you can click **Knit** in the script pane to render the file.

When you render your file, you can preview how it will look in the format you selected when you opened the file. In this example, you will preview an html file.

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/Ji0HrtWzTNStB67Vs_zUIA_0d18df6973914369b433cef25d7fc08d_Screenshot-2021-03-02-11.02.05-AM.png?expiry=1717200000000&hmac=7cl0jMHEp26DKBdCqQzu0RtMVkXvk5zdSMs_FE38sz0)

Rendering a file also automatically runs the code chunks to show the output. In this example, it shows that tidyverse was loaded using the library() function.

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/Sl3PQYmCTnedz0GJgm53NQ_44a20db2fd0a4195b203352acad2faba_Screenshot-2021-03-02-11.07.25-AM.png?expiry=1717200000000&hmac=nSnKWwhKQuW9NH87T9G2LU-zHnL44r-OPJGtBNzWhTA)

---