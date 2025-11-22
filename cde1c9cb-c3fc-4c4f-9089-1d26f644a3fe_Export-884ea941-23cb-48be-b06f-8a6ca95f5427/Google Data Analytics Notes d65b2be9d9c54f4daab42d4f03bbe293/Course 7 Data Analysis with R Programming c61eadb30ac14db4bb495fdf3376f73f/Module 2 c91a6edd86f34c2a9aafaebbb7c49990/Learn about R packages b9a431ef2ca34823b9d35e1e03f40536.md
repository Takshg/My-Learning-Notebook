# Learn about R packages

---

# The gift that keeps on giving

[index (65).mp4](Learn%20about%20R%20packages%20b9a431ef2ca34823b9d35e1e03f40536/index_(65).mp4)

**What are packages?**

- Packages are units of reusable R code that make it easier to manage and share code.
- They are created by the R community to share functions, datasets, and documentation.
- Packages help you avoid writing the same code repeatedly and provide access to specialized functions for various tasks.

**Types of packages:**

- **Base R packages:** These are pre-installed and loaded by default in RStudio. They provide essential functions for basic data analysis.
- **Recommended packages:** These are installed but not loaded by default. You need to use the `library()` function to load them before using their functions.
- **User-installed packages:** These are not included in R by default and need to be installed from online repositories like CRAN (Comprehensive R Archive Network).

**Key points:**

- Packages make R more powerful and versatile by providing access to a vast library of functions.
- You can check the list of installed packages using the `installed.packages()` function.
- To load a package, use the `library()` function followed by the package name.
- You can find more information about a package using the `help()` function or by clicking on its name in the Packages tab.
- CRAN is a valuable resource for finding and installing R packages.

**Definitions:**

- **Function:** A block of code that performs a specific task.
- **Dataset:** A collection of data organized in a specific format.
- **Documentation:** Information about a package, including its functions, datasets, and usage instructions.
- **CRAN:** Comprehensive R Archive Network, an online repository of R packages.

---

# Available R packages

To make the most of R for your data analysis, you will need to install packages. **Packages** are units of reproducible R code that you can use to add more functionality to R. The best part is that the R community creates and shares packages so that other users can access them! In this reading, you will learn more about widely used packages and where to find them.

Packages can be found in repositories, which are collections of useful packages that are ready to install. You can find repositories on [**Bioconductor**](http://bioconductor.org/), [**R-Forge**](https://r-forge.r-project.org/), [**rOpenSci**](https://ropensci.org/), or [**GitHub**](https://github.com/), but the most commonly used repository is the Comprehensive R Archive Network or [**CRAN**](https://cran.r-project.org/). CRAN stores code and documentation so that you can install packages into your own RStudio space.

## Package documentation

Packages will not only include the code itself, but also documentation that explains the package’s author, function, and any other packages that you will need to download. When you are using CRAN, you can find the package documentation in the DESCRIPTION file.

Check out Karl Broman's [**R Package Primer](https://kbroman.org/pkg_primer/)** to learn more.

## Choosing the right packages

With so many packages out there, it can be hard to know which ones will be the most useful for your library or directory of installed packages. Luckily, there are some great resources out there:

- [**Tidyverse**](https://www.tidyverse.org/): the tidyverse is a collection of R packages specifically designed for working with data. It’s a standard library for most data analysts, but you can also download the packages individually.
- [**Quick list of useful R packages**](https://support.rstudio.com/hc/en-us/articles/201057987-Quick-list-of-useful-R-packages): this is RStudio Support’s list of useful packages with installation instructions and functionality descriptions.
- [**CRAN Task Views**](https://cran.r-project.org/web/views/): this is an index of CRAN packages sorted by task. You can search for the type of task you need to perform and it will pull up a page with packages related to that task for you to explore.

You will discover more packages throughout this course and as you use R more often, but this is a great starting point for building your own library.

---

# Welcome to the tidyverse

[index (66).mp4](Learn%20about%20R%20packages%20b9a431ef2ca34823b9d35e1e03f40536/index_(66).mp4)

This video covers the installation and loading of the tidyverse package in R. Here's a detailed summary with key points and definitions:

**Key Points:**

- **Tidyverse:** A collection of R packages designed for data manipulation, exploration, and visualization.
- **CRAN:** The Comprehensive R Archive Network, a repository for R packages.
- **Installation:** Using the `install.packages()` function with the package name in quotes.
- **Loading:** Using the `library()` function with the package name.
- **Conflicts:** When packages have functions with the same names, the last loaded package takes precedence.
- **Updating Packages:** Use `update.packages()` or `install.packages()` with the package name to update individual packages.
- **Messages:** The console may display warnings or error messages, which can be addressed using the help tab.

**Definitions:**

- **Package:** A collection of R functions, data, and documentation.
- **Base R:** The core set of packages included with R.
- **GitHub:** A platform for hosting and collaborating on code.
- **ggplot2:** A package for creating visualizations in R.
- **tibble:** A package for working with data frames.
- **tidyr:** A package for data manipulation.
- **readr:** A package for importing data.
- **purrr:** A package for functional programming.
- **dplyr:** A package for data manipulation.
- **stringr:** A package for working with strings.
- **forcats:** A package for working with factors.

**Additional Notes:**

- The video emphasizes the importance of tidyverse for data analysis in R.
- It demonstrates how to install and load the tidyverse package.
- It explains the concept of conflicts and how to address them.
- It provides information on updating packages and interpreting console messages.
- The video encourages learners to explore the tidyverse packages and their functionalities.

**Further Resources:**

- Tidyverse documentation: https://www.tidyverse.org/
- CRAN: https://cran.r-project.org/
- RStudio documentation: https://www.rstudio.com/resources/cheatsheets/

---

# Installing and loading tidyverse

## Activity overview

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/UWFf-U9hTzKhX_lPYX8yBw_8c2e9cd211e3479a89816c7b1816ab07_image4.png?expiry=1717113600000&hmac=Gqe4LwaNIT8ElDkyxG__403kaOWYPbqS1QQg4FxF9VQ)

In the last activity, you explored the R sandbox and used some R packages such as the tidyverse. In this activity, you’ll explore further with the tidyverse collection of packages and learn about them using the browseVignettes function.

By the end of this activity, you will know how to easily load vignettes. Moving forward, you can use the browseVignettes function to access and review included documentation to better understand each R package you will use.

## Install the tidyverse

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/TOqxzuNFR2eqsc7jRVdnKg_a3c6611d874f403a923e10406b4f38a9_image4.png?expiry=1717113600000&hmac=SA5ye_kHuZTlHoboPmvdTdy-HIGyy4bNDQ20XzTGB98)

If you have not yet installed the tidyverse, open RStudio.

Log in, navigate to the console, type **install.packages("tidyverse")**, and press **Enter** (Windows) or **Return** (Mac).

Then wait as RStudio installs the tidyverse packages (be patient, this can take a little bit). You’ll receive a message that the install is done.

- 
    
    ![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/QsD4Eh1fSNaA-BIdX-jWBg_5bc00d790de243f0813863f14d3316d7_image4.png?expiry=1717113600000&hmac=ZtOsdNvVm8k3e_DaeQCcgRfNJd8rMCiNXe8K9LtNxak)
    
    - installing *binary* package 'tidyverse'
    *DONE (tidyverse)
    The downloaded source packages are in '/tmp/RtmpUCbADH/downloaded_packages'
    >

## Load the tidyverse

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/TOqxzuNFR2eqsc7jRVdnKg_a3c6611d874f403a923e10406b4f38a9_image4.png?expiry=1717113600000&hmac=SA5ye_kHuZTlHoboPmvdTdy-HIGyy4bNDQ20XzTGB98)

Once the tidyverse packages have been installed, load them so that they are available in your current R session. Load the core tidyverse with the **library** command. The core tidyverse contains the main packages that work together to make your data analysis smooth and efficient.

To load the core tidyverse, type **library(tidyverse)** and press **Enter** (Windows) or **Return** (Mac)**.**

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/dlM07c_4TOqTNO3P-PzqzA_8ecc92c75a8a42f6a17932d13ba6d636_Screenshot-2021-03-10-4.40.11-PM---Display-2.png?expiry=1717113600000&hmac=Fo8RLKTKbJCZr459JRDfCAR67XkFxzWwgpVsKBAf4b8)

The output in the console indicates that you have loaded the core tidyverse. Each of the core packages has a green check next to it.

The output also lists conflicts. Conflicts report which objects have the same name in two or more places within your session. This usually happens because an object in your workspace or a package you installed is masking a system object of the same name.

Since you most recently loaded the tidyverse packages, they will be the default packages for your current session.

## Read tidyverse vignettes

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/TOqxzuNFR2eqsc7jRVdnKg_a3c6611d874f403a923e10406b4f38a9_image4.png?expiry=1717113600000&hmac=SA5ye_kHuZTlHoboPmvdTdy-HIGyy4bNDQ20XzTGB98)

A **vignette** is documentation that acts as a guide to an R package. A vignette shares details about the problem that the package is designed to solve and how the included functions can help you solve it. The **browseVignettes** function allows you to read through vignettes of a loaded package.

To check out vignettes for one specific package, type **browseVignettes(“packagename”)** and press **Enter** (Windows) or **Return** (Mac)**.** Remember that functions are case-sensitive in R, so “Vignettes” must have a capital V.

For example if you execute the **browseVignettes()** function on ggplot2, **browseVignettes(“ggplot2”)**, you will have the following outcome:

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/AiQ0Bm9QS6CkNAZvUIugHA_24d6d5e17de943278395ffd8ca5e8230_Screenshot-2021-03-10-4.49.33-PM---Display-2.png?expiry=1717113600000&hmac=WBnKOkrxGwe6mPE6RbM5mb_3rdqvCzE61BI2xM0EmEA)

If you are using RStudio (Posit) Cloud, running this function on the Posit Cloud server may lead to a page where the linked contents do not exist. If this is the case, downloading the RStudio Desktop version and running the same **browseVignette()** functions as above will open a new browser tab with the *HTML, source, and R code* links leading to the vignettes, and these vignette description pages will be functional.

---