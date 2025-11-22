# Understand code chunks

---

# Code chunks

[index (87).mp4](Understand%20code%20chunks%20496074b9e4a648b1be31baf21abec590/index_(87).mp4)

**Key Points:**

- **Code chunks are the heart of R Markdown files.** They allow you to embed code directly into your document and display its output.
- **Code chunks are essential for:**
    - **Documenting your analysis:** Code chunks provide evidence for your findings and share your sources.
    - **Creating interactive reports:** Stakeholders can see the code behind your analysis and understand your process.
    - **Sharing your work with others:** Code chunks make it easy for others to reproduce your results.
- **Creating a code chunk:**
    - Use the code menu in RStudio or the keyboard shortcuts (Ctrl+Alt+I on PC/Chromebook, Cmd+Option+I on Mac).
    - Label your code chunk for easy identification.
    - Add your code between the delimiters (```{r}).
    - Run the code directly in the file to check for errors.
- **Code chunk options:**
    - Change the output format.
    - Turn off warnings and messages.
    - Control what information is displayed in the final report.

**Definitions:**

- **R Markdown:** A file format that combines R code, text, and output into a single document.
- **Code chunk:** A section of code embedded in an R Markdown file.
- **Delimiter:** A character that indicates the beginning or end of a data item (e.g., ```).
- **Output:** The result of running the code in a code chunk.
- **Stakeholder:** An individual or group with an interest in the results of your analysis.

---

# Hands On Activity: Adding code chunks to R Markdown notebooks

## Overview

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/TOqxzuNFR2eqsc7jRVdnKg_a3c6611d874f403a923e10406b4f38a9_image4.png?expiry=1717200000000&hmac=OB7LVwPbT3kQVCn21rKPfKCUU17B6iuI-upb7lbmN-8)

Earlier in this course, you created a visualization using the ggplot() function. You also learned how to create an R Markdown notebook. In this activity, you will combine and apply your knowledge by adding the code you used to create a visualization to a RMarkdown notebook.

By the time you complete this activity, you will be able to make and format an .rmd file containing the visualizations you created using ggplot2. This will allow you to track and share analysis and also share the R code you use to create visualizations. This will prove useful if you want to give other data analysts an interactive way to test out your code and better communicate findings to your stakeholders and colleagues.

## Add code chunks to your RMarkdown notebook

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/TOqxzuNFR2eqsc7jRVdnKg_a3c6611d874f403a923e10406b4f38a9_image4.png?expiry=1717200000000&hmac=OB7LVwPbT3kQVCn21rKPfKCUU17B6iuI-upb7lbmN-8)

1. To start, log in to your RStudio Cloud account.

2. Next, open a new R Markdown notebook and create a code block section. Notebook chunks can be inserted quickly using the keyboard shortcut **Ctrl + Alt + I** (Windows) or **Cmd + Option + I** (Mac). Code chunks can also be added using the Insert menu in the editor toolbar.

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/HvFR6i52TKixUeoudsyoww_d8a5c11acd854498ad061285ec8e30b8_image3.png?expiry=1717200000000&hmac=m0X_OwdvdIBlVnJOHMZIi8FBxKdjRdiIo1cwIt-Fzp8)

Code chunks are designated in R Markdown with **delimiters*.*** A delimiter is a character that indicates the beginning or end of a data item. In this case, the code chunk is marked using three ticks followed by a curly bracket, descriptive text, and a closed curly bracket. You then have an empty space to add the appropriate code. Here is the general syntax:

**```{r}**

**```**

When creating code chunks, it is useful to keep in mind that the output of the code chunk will appear immediately after the chunk when it is executed. Because of that, it is good practice to split chunks that produce multiple outputs into two or more chunks. That way, each code chunk only produces one output, which can be easier for users to execute and explore.

3. Using the code from your ggplot() visualization, create two new chunks. Type the following in the first code chunk to call the required libraries, load the penguins data, and return a view of the penguins data:

**```{r ggplot for penguin data}**

**library(ggplot2)**

**library(palmerpenguins)**

**data(penguins)**

**View(penguins)**

**```**

Note that the only output from the code chunk is a tabular view of your data as result of the View function.

4. Then, type the following in the second code chunk to create the visualization:

**```{r ggplot for penguin data visualization}**

**ggplot(data = penguins) +**

**geom_point(mapping = aes(x = flipper_length_mm, y = body_mass_g))**

**```**

5. Finally, run each code chunk to examine the results. You might recognize this visualization from a [previous activity](https://www.coursera.org/learn/data-analysis-r/item/fmyHH).

Congratulations! You can now add your visualizations to an R Markdown notebook. Code chunks are a great way to explain your data analysis process and allow other users to explore your work. Try adding as many code chunks to your R Markdown notebook as possible to make your notebook an interactive experience.

---

# Exporting documentation

[index (88).mp4](Understand%20code%20chunks%20496074b9e4a648b1be31baf21abec590/index_(88).mp4)

**Key Points:**

- R Markdown files can be converted to different output types, including HTML, PDF, and Word documents.
- The Knit button in RStudio allows you to convert your file to any of these types.
- It's good practice to wait to convert to a PDF or Word document until you are finished working on your report.
- You can create a template for reports that you need to create regularly.
- R Markdown is a great way to wrap up the data analytics process in R and RStudio.

**Definitions:**

- **R Markdown:** A file format that allows you to combine code, text, and output into a single document.
- **Knit button:** A button in RStudio that allows you to convert your R Markdown file to different output types.
- **YAML:** A file format that is used to store metadata about an R Markdown file.
- **Template:** A pre-formatted R Markdown file that you can use to create reports.

**Summary:**

The video begins by discussing the different output types that R Markdown files can be converted to. It is important to note that you should wait to convert to a PDF or Word document until you are finished working on your report. This is because HTML does not have page breaks, so you can focus on generating content for your report without worrying about its appearance.

The video then goes on to discuss the Knit button in RStudio. The Knit button allows you to convert your R Markdown file to any of the available output types. You can also use the YAML file to change your metadata or incorporate more details.

Finally, the video discusses the concept of templates. Templates are pre-formatted R Markdown files that you can use to create reports. This can be helpful if you need to create a certain type of document over and over again.

---

# Output formats in R Markdown

*You can save this reading for future reference. Feel free to download a PDF version of this reading below:*

[Output-formats-available-in-RMarkdown.pdf](../HMmvfrAKSl6Jr36wCjpejg_f7ff98b532974cfca3bdea0be6731e4f_Output-formats-available-in-RMarkdown.pdf)

This reading will explore the different types of output formats you can produce with R Markdown.

## Setting the output of an R Markdown document

When working in RStudio, you can set the output of a document in R Markdown by changing the YAML header.

For example, the following code creates an HTML document:

- --

title: "Demo"

output: html_document

- --

And the following code creates a PDF document:

- --

title: "Demo"

output: pdf_document

- --

The **Knit** button in the RStudio source editor renders a file to the first format listed in its output field (HTML is the default). You can render a file to additional formats by clicking the dropdown menu next to the knit button.

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/1anMb9A5THqpzG_QORx6yw_149323e0e3ff44cf9ac91c53000167ff_Screen-Shot-2021-02-02-at-9.53.11-AM.png?expiry=1717200000000&hmac=FP1tcRhdFQI-cHeA6aUH6hEEWs5x_6Jwu2Pf2uSt0n4)

## Available document outputs

In addition to the default HTML output (**html_document**), you can create other types of documents in R Markdown using the following output settings:

- **pdf_document** – This creates a PDF file with LaTeX (an open source document layout system). If you don’t already have LaTeX, RStudio will automatically prompt you to install it.
- **word_document** – This creates a Microsoft Word document (.docx).
- **odt_document** – This creates an OpenDocument Text document (.odt).
- **rtf_document** – This creates a Rich Text Format document (.rtf).
- **md_document** – This creates a Markdown document (which strictly conforms to the original Markdown specification)
- **github_document** – This creates a GitHub document which is a customized version of a Markdown document designed for sharing on GitHub.

For a detailed guide to creating different types of R Markdown documents, check out the [Documents](https://bookdown.org/yihui/rmarkdown/documents.html) chapter in *R Markdown: The Definitive Guide*.

### **Notebooks**

A **notebook** (html_notebook) is a variation on an HTML document (html_document). Overall, the output formats are similar; the main difference between them is that the rendered output of a notebook always includes an embedded copy of the source code.

Notebooks and HTML documents also have different purposes. HTML documents are good for communicating with stakeholders. Notebooks are better for collaborating with other data analysts or data scientists.

To learn more, check out the section on [Notebooks](https://rmarkdown.rstudio.com/lesson-10.html) in the R Markdown documentation.

### **Presentations**

You can also use R Markdown to produce presentations. Automatically inserting the results of your R code into a presentation can save you lots of time.

R Markdown renders files to specific presentation formats when you use the following output settings:

- **beamer_presentation** – for PDF presentations with beamer
- **ioslides_presentation** – for HTML presentations with ioslides
- **slidy_presentation** – for HTML presentations with Slidy
- **powerpoint_presentation** – for PowerPoint presentations
- **revealjs : : revealjs_presentation** – for HTML presentations with reveal.js (a framework for creating HTML presentations that requires the reveal.js package)

To learn more, check out the section on [Slide Presentations](https://rmarkdown.rstudio.com/lesson-11.html) in the R Markdown documentation.

### **Dashboards**

Dashboards are a useful way to quickly communicate a lot of information. The ****[flexdashboard](https://github.com/rstudio/flexdashboard) package lets you publish a group of related data visualizations as a dashboard. Flexdashboard also provides tools for creating sidebars, tabsets, value boxes, and gauges.

To learn more, visit the [flexdashboard for R](https://rmarkdown.rstudio.com/flexdashboard/) page and the [Dashboards](https://rmarkdown.rstudio.com/lesson-12.html) section in the R Markdown documentation.

### **Shiny**

**Shiny** is an R package that lets you build interactive web apps using R code. You can embed your apps in R Markdown documents or host them on a webpage.

To call Shiny code from an R Markdown document, add  runtime: shiny to the YAML header:

- --

title: "Shiny Web App"

output: html_document

runtime: shiny

- --

To learn more about Shiny and how to use R code to add interactive components to an R Markdown document, check out the [Shiny](https://shiny.rstudio.com/tutorial/) tutorial from RStudio.

### **Other formats**

Other packages provide even more output formats:

- The [bookdown](https://github.com/rstudio/bookdown) package is helpful for writing books and long-form articles.
- The [prettydoc](https://github.com/yixuan/prettydoc/) package provides a range of attractive themes for R Markdown documents.
- The ****[rticles](https://github.com/rstudio/rticles) ****package provides templates for various journals and publishers.

Visit the [RStudio Formats](https://rmarkdown.rstudio.com/formats.html) page in the R Markdown documentation for a more comprehensive list of output formats and packages.

## Additional resources

For more information, check out these additional resources:

- The [R Markdown gallery](https://rmarkdown.rstudio.com/gallery.html) from RStudio has tons of examples of the outputs you can create with R Markdown.
- The [R Markdown Formats](https://r4ds.had.co.nz/r-markdown-formats.html) chapter in the *R for Data Science* book provides more details about the output formats introduced in this reading. This reading was compiled from information in this book.

---

# Hands On Activity: Exporting your R Markdown notebook

## Activity overview

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/TOqxzuNFR2eqsc7jRVdnKg_a3c6611d874f403a923e10406b4f38a9_image4.png?expiry=1717200000000&hmac=OB7LVwPbT3kQVCn21rKPfKCUU17B6iuI-upb7lbmN-8)

In the last activity, you created a draft of your R Markdown notebook. Now, you will export and share it.

By the time you complete this activity, you will be able to export an R notebook as two different outputs: html and pdf. This will enable you to easily share your work with others to get feedback and demonstrate your R skills.

## Export your R Markdown notebook

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/TOqxzuNFR2eqsc7jRVdnKg_a3c6611d874f403a923e10406b4f38a9_image4.png?expiry=1717200000000&hmac=OB7LVwPbT3kQVCn21rKPfKCUU17B6iuI-upb7lbmN-8)

For this activity, you will export a notebook you created in previous activities as both an html document and a pdf.

You will use the **Knit** option to export your work. This will allow you to convert the Rmd file to another file type that is more readable and useful to other users.

To begin, follow these steps:

1. Open a document in [RStudio](https://rstudio.cloud/). Then, find the **Knit** button on the toolbar at the top of your document window. Click it to open a dropdown menu with a few export options.

2. Click on the option that matches the file type you want to export your notebook as. Begin with html. Once you click **Knit to HTML**, your console might take a moment to process. When it is finished, it will automatically open your new file.

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/xWf5XcLKSHmn-V3Cymh5Ww_3272194bab8e4d12852b3c53bdf7adfd_Screenshot-2021-02-19-11.02.28-AM.png?expiry=1717200000000&hmac=4oo6cvggmfHQrZErauKHSKZGjZunhC7BzVZLUSKxK3M)

3. Now, repeat Step 2 but select **Knit to PDF**. Explore how these file formats are different from your original Rmd file.

4. To download the files you exported, find them in the Files explorer in the bottom-right of the screen.

5. Check the boxes of the file(s) you want to download and click the **More** dropdown.

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/RE38u1I4RPeN_LtSOJT3_Q_1ac0121d16f54dbf82723e7a8cdb42f1_Export.png?expiry=1717200000000&hmac=F4nQS4c6eZY3bjLwNTs9avbvWICZJOUu2gtn8c-SFII)

6. Click **Export…** and name the file by a title that will help you find it later. Click **Download**. Now your exported file will be downloaded to your computer.

![Untitled](Understand%20code%20chunks%20496074b9e4a648b1be31baf21abec590/Untitled.png)

After you have successfully exported and downloaded your R Markdown notebook, you can share it with a friend, colleague, or the discussion forums to get feedback. After you have gotten their feedback, you can make revisions and continue to share your work to refine your notebook even more.

Sharing your R Markdown notebook is a great way to give other users insights into your data analysis. R Markdown comes with a lot of different options for exporting notebooks, so you can choose the best file type for your needs.

Understanding how to export your R Markdown notebooks will make documenting and sharing your data analysis process easier. Now that you are familiar with this process, you can export your own notebooks for future projects.

---