# Annotate and save visualizations

---

# Annotation layer

[index (81).mp4](Annotate%20and%20save%20visualizations%20280134cf93dc4a4fa02d664d73c61c85/index_(81).mp4)

**Key Points:**

- **Labels:** Used to add informative text outside the plot grid, such as titles, subtitles, and captions.
- **Annotations:** Used to add text inside the plot grid to highlight specific data points.
- **Label Function:**
    - Syntax: `label(title = "Title Text", subtitle = "Subtitle Text", caption = "Caption Text")`
    - Adds titles, subtitles, and captions to the plot.
- **Annotate Function:**
    - Syntax: `annotate(geom = "text", x = x_coordinate, y = y_coordinate, label = "Text Label")`
    - Adds text labels to specific data points.
- **Customization Options:**
    - **Color:** `color = "color_name"`
    - **Font:** `fontface = "font_name", size = font_size`
    - **Angle:** `angle = angle_in_degrees`

**Definitions:**

- **ggplot2:** A popular R package for creating statistical graphics.
- **Label:** Text added outside the plot grid to provide context and information.
- **Annotation:** Text added inside the plot grid to highlight specific data points.
- **Title:** Text at the top of the plot indicating its purpose.
- **Subtitle:** Text below the title providing additional information.
- **Caption:** Text at the bottom of the plot indicating the data source.
- **Geom:** Geometric object representing the data points.
- **X-coordinate:** Horizontal position of the text label.
- **Y-coordinate:** Vertical position of the text label.

**Real-Life Example:**

Imagine you are analyzing data on penguin body mass and flipper length. You can use labels to add a title, subtitle, and caption to your plot, and annotations to highlight the data points for the Gentoo penguin species. This will help your audience understand the plot and its key findings.

**Additional Resources:**

- [ggplot2 Documentation](https://ggplot2.tidyverse.org/)
- [RStudio ggplot2 Tutorial](https://r4ds.had.co.nz/data-visualisation.html)

---

# Adding annotations in R

Annotations are a useful way to add notes to your plot. They help you explain the plot’s purpose, highlight important data points, or comment on any data trends or findings the plot illustrates. You have already learned how to add notes as labels, titles, subtitles, and captions. You can also draw arrows or add shapes to your plot to create more emphasis. Usually you add these kinds of annotations in your presentation application after you have saved the visualizations. But, you can now add lines, arrows, and shapes to your plots using **ggplot2**.

## Resources

Check out these resources to learn more:

- [**Create an annotation layer**](https://ggplot2.tidyverse.org/reference/annotate.html): This guide explains how to add an annotation layer with ggplot2. It includes sample code and data visualizations with annotations created in ggplot2.
- [**How to annotate a plot in ggplot2](https://www.r-graph-gallery.com/233-add-annotations-on-ggplot2-chart.html):** This resource includes explanations about how to add different kinds of annotations to your ggplot2 plots, and is a great reference if you need to quickly look up a specific kind of annotation.
- [**Annotations](https://ggplot2-book.org/annotations.html):** Chapter eight of the online ggplot2 textbook is focused entirely on annotations. It provides in-depth explanations of the different types of annotations, how they are used, and detailed examples.
- [**How to annotate a plot](https://www.r-bloggers.com/2017/02/how-to-annotate-a-plot-in-ggplot2/):** This R-Bloggers article includes explanations about how to annotate plots in ggplot2. It starts with basic concepts and covers more complicated information the further on you read.
- [**Text Annotations](https://viz-ggplot2.rsquaredacademy.com/textann.html):** This resource focuses specifically on adding text annotations and labels to ggplot2 visualizations.

---

# Saving your visualizations

[index (82).mp4](Annotate%20and%20save%20visualizations%20280134cf93dc4a4fa02d664d73c61c85/index_(82).mp4)

**Key Points:**

- Saving your plots is crucial for accessing and sharing your work later.
- This allows for collaboration, reproducibility, and feedback.
- Two methods for saving plots are covered:
    - **Export option in RStudio:**
        - Saves plots as image or PDF files.
        - Offers various image formats like PNG and JPEG.
        - Requires naming the file and clicking "Save."
    - **ggsave function:**
        - Saves the last displayed plot by default.
        - Uses the size of the current graphics device.
        - Requires specifying the filename and file type within the function.

**Definitions:**

- **ggplot2:** A powerful R package for creating complex and customizable visualizations.
- **PNG:** A lossless image format that preserves image quality.
- **JPEG:** A lossy image format that compresses images, potentially sacrificing some quality.
- **Graphics device:** The output destination for R graphics, such as the screen or a file.

**Additional Notes:**

- The video emphasizes the importance of saving plots for future reference and collaboration.
- It demonstrates both methods for saving plots, providing clear instructions for each.
- The video concludes by encouraging learners to practice and explore ggplot2 further.

---

# Saving images without ggsave()

In most cases, **ggsave()** is the simplest way to save your plot. But there are situations when it might be best to save your plot by writing it directly to a graphics device. This reading will cover some of the different ways you can save images and plots without ggsave(), and includes additional resources to check out if you want to learn more.

A graphics device allows a plot to appear on your computer. Examples include:

- A window on your computer (screen device)
- A PDF, PNG, or JPEG file (file device)
- An SVG, or scalable vector graphics file (file device)

When you make a plot in R, it has to be “sent” to a specific graphics device. To save images without using ggsave(), you can open an R graphics device like **png()** or **pdf()**; these will allow you to save your plot as a .png or .pdf file. You can also choose to print the plot and then close the device using **dev.off()**.

| **Example of using png()** | **Example of using pdf()** |
| --- | --- |
| **png(file = "exampleplot.png", bg = "transparent")
plot(1:10)
rect(1, 5, 3, 7, col = "white")
dev.off()** | **pdf(file = "/Users/username/Desktop/example.pdf",    
       width = 4,     
       height = 4) 
plot(x = 1:10,     
        y = 1:10)
abline(v = 0)
text(x = 0, y = 1, labels = "Random text")
dev.off()** |

To learn more about the different processes for saving images, check out these resources:

- [**Saving images without ggsave()**](https://ggplot2.tidyverse.org/reference/ggsave.html#saving-images-without-ggsave-): This resource is pulled directly from the ggplot2 documentation at [**tidyverse.org**](https://www.tidyverse.org/). It explores the tools you can use to save images in R, and includes several examples to follow along with and learn how to save images in your own R workspace.
- [**How to save a ggplot**](https://www.datanovia.com/en/blog/how-to-save-a-ggplot/): This resource covers multiple different methods for saving ggplots. It also includes copyable code with explanations about how each function is being used so that you can better understand each step in the process.
- [**Saving a plot in R:**](https://www.datamentor.io/r-programming/saving-plot/) This guide covers multiple file formats that you can use to save your plots in R. Each section includes an example with an actual plot that you can copy and use for practice in your own R workspace.

---

# Hands On Activity: Annotating and saving visualizations

## Activity overview

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/UWFf-U9hTzKhX_lPYX8yBw_8c2e9cd211e3479a89816c7b1816ab07_image4.png?expiry=1717113600000&hmac=Gqe4LwaNIT8ElDkyxG__403kaOWYPbqS1QQg4FxF9VQ)

So far, you have used ggplot2 to create different kinds of visualizations. In this activity, you’ll follow through a scenario and add annotations to a data visualization with ggplot2. You will also learn how to save images from ggplot2 visualizations.

By the end of this activity, you will be able to enhance a visualization with annotations and save it as an image so that you can add it directly to a presentation. This will enable you to demonstrate your findings more clearly and better explain your insights in your career as a data analyst.

## Working in RStudio Cloud

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/TOqxzuNFR2eqsc7jRVdnKg_a3c6611d874f403a923e10406b4f38a9_image4.png?expiry=1717113600000&hmac=SA5ye_kHuZTlHoboPmvdTdy-HIGyy4bNDQ20XzTGB98)

To start, log into your RStudio Cloud account. Open the project you will work on in the activity with [this link](https://posit.cloud/content/6208304), which opens in a new tab. If you haven't gone through this process already, at the top right portion of the screen you will see a "red stamp" indicating this project as a Temporary Copy. Click on the adjacent button, **Save a Permanent Copy**, and the project will be saved in your main dashboard for use with future lessons. Once that is completed,  navigate to the file explorer in the bottom right and click the following: **Course 7 -> Week 4 -> Lesson4_Annotations.Rmd**.

The .csv file that you will need, hotel_bookings.csv, is also located in this folder.

If you’re having trouble finding the correct activity, check out this [step-by-step guide](https://scribehow.com/shared/Access_and_Install_Course_Material_for_Lesson_3__JGhlL8PLSxuqtK2KRWZkJw) on how to navigate in RStudio Cloud. Make sure to select the correct R markdown (Rmd) file. The other Rmd files will be used in different activities.

If you are using RStudio Desktop, you can download the Rmd file and the data for this activity directly here:

[Lesson4_Annotations.txt](../All%20Lessons%20within%20RStudio%20eee207139d0e44b08808f644117b4284/G3plpxrcQTK6Zaca3KEyCA_41465a9595734b999b08b15ecae710f1_Lesson4_Annotations.txt)

[hotel_bookings (6).csv](../All%20Lessons%20within%20RStudio%20eee207139d0e44b08808f644117b4284/GL0bk8O2Sja9G5PDtko2uQ_31e445d7ca64417eb45aeaa08ec90bf1_hotel_bookings_(6).csv)

You can also find the Rmd file with the solutions for this activity here:

[Lesson4_Annotations_Solutions.txt](../All%20Lessons%20within%20RStudio%20eee207139d0e44b08808f644117b4284/vHkzTo-IQYW5M06PiIGFlQ_5e2103c4431642d79b048badb43dfff1_Lesson4_Annotations_Solutions.txt)

Carefully read the instructions in the comments of the Rmd file and complete each step. Some steps may be as simple as running pre-written code, while others may require you to write your own functions. After you finish the steps in the Rmd file, return here to confirm that your work is complete.