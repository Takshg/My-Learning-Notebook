# Learn programming using RStudio

---

### Test your knowledge on programming langauage

[index (61).mp4](Learn%20programming%20using%20RStudio%2011c2f4d424f843289ae37b761b31607f/index_(61).mp4)

---

# Hands-On Activity: Cloud access to RStudio

## Activity overview

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/UWFf-U9hTzKhX_lPYX8yBw_8c2e9cd211e3479a89816c7b1816ab07_image4.png?expiry=1717113600000&hmac=Gqe4LwaNIT8ElDkyxG__403kaOWYPbqS1QQg4FxF9VQ)

By now, you’ve learned about RStudio, an integrated development environment that allows you to more efficiently create and manage projects using R. In this activity, you will learn how to access the cloud version of RStudio.

Upon completing this activity, you will be more familiar with the RStudio interface and comfortable using its basic tools . This is a foundational step that will prepare you for upcoming RStudio  activities during this course. This hands-on activity, and the future RStudio activities you will complete, are essential to developing job-ready R programming skills.

## Access RStudio Cloud

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/TOqxzuNFR2eqsc7jRVdnKg_a3c6611d874f403a923e10406b4f38a9_image4.png?expiry=1717113600000&hmac=SA5ye_kHuZTlHoboPmvdTdy-HIGyy4bNDQ20XzTGB98)

**RStudio Cloud** (now called **Posit Cloud**) is the primary tool you will use for this course. In order to use RStudio Cloud, you need stable internet access. It won’t matter what operating system you have because it works in your browser.

You can also install a desktop version, which you can download based on instructions provided in the next (optional) activity. This is a good alternative if you want to be able to work with R offline.

In order to access RStudio Cloud, follow these steps:

1. Sign up for an account at the [RStudio Cloud sign-up page](https://rstudio.cloud/plans/free).

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/W_p167qFTiq6deu6hd4qcQ_b731483850ad4d0aaaf8e1730b3ac718_Screenshot-2021-03-10-7.20.08-PM---Display-2.png?expiry=1717113600000&hmac=VZGNTzE_57QXU7OAa57zL2k4BXRkCo7BMs9mu2_ZkhI)

Here, you will find more information about RStudio Cloud, including the pricing plans. You will use the free version throughout this course, but it does have a few limitations. You can only have up to 15 projects on your free account, and can only use 15 project hours per month. You might consider upgrading later on if you find yourself using RStudio a lot.

2. For now, click the **Sign Up** button on the bottom-right to start with the free version.

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/lXDdhDLSRpOw3YQy0uaTyQ_1cfdc750e8b64b3181555fbbeecb117e_Screenshot-2021-03-10-7.22.18-PM---Display-2.png?expiry=1717113600000&hmac=eWZLWZaRg7KuINdqko7LFXaRMBm7eHOLID-3qSm7YKQ)

3. Input your email, a password, as well as your first and last name.

4. Once you have signed up, open RStudio Cloud for the first time.

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/LKG-siapQXOhvrImqUFz3Q_d18cdbd9f60e49229eccbb5eef236ae2_Screenshot-2021-03-10-7.24.44-PM---Display-2.png?expiry=1717113600000&hmac=sEyBfnh-hJ2EeDJ6eAVqNlCHPSwbCzoKcpejaFfvL58)

5. Click **New Project** to create a new project workspace and open the RStudio Cloud console.

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/znxMEXv8T2m8TBF7_N9pKA_97d24251fe604d87a9e5d461ed53cfff_Screenshot-2021-03-10-7.26.12-PM---Display-2.png?expiry=1717113600000&hmac=OStr09Edi4ZSVcyaqiar8qmA-v1Y2e2tpLhRi9fqKYo)

## Install and load packages

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/TOqxzuNFR2eqsc7jRVdnKg_a3c6611d874f403a923e10406b4f38a9_image4.png?expiry=1717113600000&hmac=SA5ye_kHuZTlHoboPmvdTdy-HIGyy4bNDQ20XzTGB98)

Once you have opened a new project in your console, you can install packages to RStudio Cloud.

**Packages** are ****units of reproducible R code. ****Members of the R community create packages to keep track of the R functions that they write and reuse. Packages offer a helpful combination of code, reusable R functions, descriptive documentation, tests for checking your code, and sample data sets.

The lubridate package that you are about to install is part of the **tidyverse**. The tidyverse ****is a collection of packages in R with a common design philosophy for data manipulation, exploration, and visualization. For a lot of data analysts, the tidyverse is an essential tool. You will learn more about the tidyverse later on in this course.

To install the core tidyverse packages and load them, follow these steps:

1. In the bottom of the console, type **install.packages("tidyverse")** and press **Enter** (Windows) or **Return** (Mac).

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/vCcs9_32QJ-nLPf99hCf5g_a32a8b6ec85941c8a0a40dc1badaaff1_Screenshot-2021-07-01-11.41.05-PM.png?expiry=1717113600000&hmac=pX5vzRybgmPzYYxW6A6fTyDgYRaex8BzqP1FUf3c1Fk)

This may take a while. You can tell if the process is still running by checking the red **Stop** icon in the upper right of the console. You can click this icon to interrupt the running code and cancel the command.

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/epRMQ8RORAyUTEPEToQMQA_876d538430214da6a1a707c6db48a4f1_stop.png?expiry=1717113600000&hmac=j6gQOAMsyEZfeU-gPjjXof4rZScy2loCyO-JKkXtpeE)

You can tell that the process is complete when the cursor reappears in the bottom of the console.

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/V07S4BQAT0SO0uAUAI9EKw_b8a764d5ea57479fa5e908b91672d1f1_done.png?expiry=1717113600000&hmac=Kj6lt-_TQN-XffRS33-fBQT39NYSIKPKuyhhEk0Kxto)

2. Load the tidyverse library with the **library()** function. To load the core tidyverse, type **library(tidyverse)** and press **Enter** (Windows) or **Return** (Mac)**.**

You only need to install a package once, but you need to reload it every time you start a new session.

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/cPxI9BU4Qb28SPQVOGG9Eg_f9437acd96b9430890762d21203e2af1_Screenshot-2021-07-01-11.45.56-PM.png?expiry=1717113600000&hmac=y6HbIGKIzzsqMv3yvlrP9H72UFVMOVy_rW7SuDZTYWA)

3. Load the lubridate package. Since this is already part of the tidyverse package, there is no need to re-install. However, the library will need to be loaded. Type **library(lubridate**) into the console pane and press **Enter** (Windows) or **Return** (Mac).

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/CTOR0VJSTUSzkdFSUp1EuA_28151d646f0642ce87f2c727012a65f1_Screenshot-2021-07-01-11.47.18-PM.png?expiry=1717113600000&hmac=cVdoa6WOq89YYvLV5ol5AhyQQtoJKDDvnTx73t6Ixh0)

After you complete these steps, you can exit RStudio. Feel free to explore RStudio Cloud on your own to get more familiar with the tools and practice what you are learning in this course.

---

# When to use RStudio

As a data analyst, you will have plenty of tools to work with in each phase of your analysis. Sometimes, you will be able to meet your objectives by working in a spreadsheet program or using SQL with a database. In this reading, you will go through some examples of when working in R and RStudio might be your better option instead.

## Why RStudio?

One of your core tasks as an analyst will be converting raw data into insights that are accurate, useful, and interesting. That can be tricky to do when the raw data is complex. R and RStudio are designed to handle large data sets, which spreadsheets might not be able to handle as well. RStudio also makes it easy to reproduce your work on different datasets. When you input your code, it's simple to just load a new dataset and run your scripts again. You can also create more detailed visualizations using RStudio.

## When RStudio truly shines

When the data is spread across multiple categories or groups, it can be challenging to manage your analysis, visualize trends, and build graphics. And the more groups of data that you need to work with, the harder those tasks become. That’s where RStudio comes in.

For example, imagine you are analyzing sales data for every city across an entire country. That is a lot of data from a lot of different groups–in this case, each city has its own group of data.

Here are a few ways RStudio could help in this situation:

- Using RStudio makes it easy to take a specific analysis step and perform it for each group using basic code. In this example, you could calculate the yearly average sales data for every city.
- RStudio also allows for flexible data visualization. You can visualize differences across the cities effectively using plotting features like facets–which you’ll learn more about later on.
- You can also use RStudio to automatically create an output of summary stats—or even your visualized plots—for each group.

As you learn more about R and RStudio moving forward in this program, you’ll get a better understanding of when RStudio should be your data analysis tool of choice.

## For more information

- [**The Advantages of RStudio**](https://www.theanalysisfactor.com/the-advantages-of-rstudio/): This web page explains some of the reasons why RStudio is many analysts’ preferred choice for interfacing with R. You’ll learn about the advantages of using RStudio for data analysis, from ease of use to accessibility of graphics and more.
- [**Data analysis and R programming**](https://lgatto.github.io/2017_11_09_Rcourse_Jena/before-we-start.html): This online introduction to data analysis and R programming is a good starting point for R and RStudio users. It also includes a list of detailed explanations about the advantages of using R and RStudio. You’ll also find a helpful guide for getting set up with RStudio.

---

# Connecting with other analysts in the R community

R is a powerful tool in your data analysis toolkit–and it also has a powerful community of users who are excited to share, collaborate, and connect with others. This reading will give you a few places where you can start to connect, online and in-person, with other analysts in the R community.

## Online communities

Online communities allow you to connect with other R users no matter where you live. This list includes forums and discussion channels where you can join the conversation. It also includes social media tags you can use on your existing social media platforms to connect with other data analysts.

- [**RStudio Community:**](https://community.rstudio.com/) The RStudio Community forum is a great place to get help and find solutions to challenges you have with R–and maybe help someone else out, too!
- [**r/RLanguage**](https://www.reddit.com/r/Rlanguage/): The R language subreddit is an active online community on the social media platform Reddit, where R users go to discuss R, ask questions, and share tips.
- [**rOpenSci**](https://discuss.ropensci.org/): rOpenSci has a community forum where R users can ask questions and search for solutions. It also includes links to their Best Practices guide and support pages.
- [**R4DS Online Learning Community and Slack channel:**](https://www.rfordatasci.com/) This is a community with another Slack channel where R learners and mentors can gather and connect. This is a great place to chat about using R for data science.
- [**Twitter #rstats**](https://twitter.com/hashtag/rstats?lang=en): If you use Twitter, you can connect with other R users using the hashtag #rstats; a lot of R developers and analysts are active on Twitter.

## Meetups

Many organizations host both in-person and online meetups for R users; you should always practice caution and be safe whenever attending meetups in-person.

- [**Local Data Analytics meetups:**](https://www.meetup.com/topics/data-analytics/) These meetups are a great way to meet other people who are interested in data analytics and build your network. These meetups are location-based, so you can connect with other data analysts in your area.
- [**R User Groups:](https://jumpingrivers.github.io/meetingsR/r-user-groups.html)** This list contains links to regional R communities, including subreddits and meetup groups. This is a useful resource if you are interested in finding R users in your area.
- [**RLadies Meetups:**](https://www.meetup.com/pro/rladies) These are in-person and virtual meetups specifically for R enthusiasts who identify as underrepresented or marginalized. These meetups are also location-based and can help you connect with other data analysts in your area.

R can be tricky to learn, but luckily there is a strong community of R users who are interested in working together and helping each other out. These resources are a good starting point if you want to begin connecting with the larger data analyst community, so take advantage of them!

---