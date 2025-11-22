# Explore data types, fields, and values - Part 2

---

# Transforming data

## What is data transformation?

- A woman presenting data, a hand holding a medal, two people chatting, a ship's wheel being steered, two people high-fiving each other
- In this reading, you will explore how data is transformed and the differences between wide and long data.
- **Data transformation** is the process of changing the data’s format, structure, or values.
- As a data analyst, there is a good chance you will need to transform data at some point to make it easier for you to analyze it.
- Data transformation usually involves:
    - Adding, copying, or replicating data
    - Deleting fields or records
    - Standardizing the names of variables
    - Renaming, moving, or combining columns in a database
    - Joining one set of data with another
    - Saving a file in a different format. For example, saving a spreadsheet as a comma separated values (.csv) file.

## Why transform data?

- Goals for data transformation might be:
    - Data **organization**: better organized data is easier to use
    - Data **compatibility**: different applications or systems can then use the same data
    - Data **migration**: data with matching formats can be moved from one system to another
    - Data **merging**: data with the same organization can be merged together
    - Data **enhancement**: data can be displayed with more detailed fields
    - Data **comparison**: apples-to-apples comparisons of the data can then be made

## Data transformation example: data merging

- Mario is a plumber who owns a plumbing company. After years in the business, he buys another plumbing company. Mario wants to merge the customer information from his newly acquired company with his own, but the other company uses a different database. So, Mario needs to make the data compatible. To do this, he has to transform the format of the acquired company’s data. Then, he must remove duplicate rows for customers they had in common. When the data is compatible and together, Mario’s plumbing company will have a complete and merged customer database.

## Data transformation example: data organization (long to wide)

- To make it easier to create charts, you may also need to transform long data to wide data. Consider the following example of transforming stock prices (collected as long data) to wide data.
- **Long data** is data where **each row contains a single data point** for a particular item. In the long data example below, individual stock prices (data points) have been collected for Apple (AAPL), Amazon (AMZN), and Google (GOOGL) (particular items) on the given dates.
    - **Long data example: Stock prices**
    
    ![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/dq8jjvDiQgmvI47w4hIJsA_ffb38f9200364ce7862d8848c8147a19_Screen-Shot-2020-11-24-at-5.42.01-PM.png?expiry=1716681600000&hmac=KGH49g1RInEjbxm5ly_PR9bGRXFP84pnTm1poWNnXps)
    

- **Wide data** is data where **each row contains multiple data points** for the particular items identified in the columns.
    - **Wide data example: Stock prices**
        
        ![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/5IiB_OOFR_eIgfzjhVf3VA_5066f31f0192481980d15830caf61b8e_Screen-Shot-2021-03-17-at-3.00.51-PM.png?expiry=1716681600000&hmac=WT6O_Trq35tP3IVz943v_o80of8KaJRNHuN52_0cQHI)
        

- With data transformed to wide data, you can create a chart comparing how each company's stock changed over the same period of time.
- You might notice that all the data included in the long format is also in the wide format. But wide data is easier to read and understand. That is why data analysts typically transform long data to wide data more often than they transform wide data to long data. The following table summarizes when each format is preferred:

| **Wide data is preferred when** | **Long data is preferred when** |
| --- | --- |
| Creating tables and charts with a few variables about each subject | Storing a lot of variables about each subject. For example, 60 years worth of interest rates for each bank |
| Comparing straightforward line graphs | Performing advanced statistical analysis or graphing |

---

# Hands-On Activity: Introduction to Kaggle

## Activity overview

By now, you’ve learned a lot about different data types and data structures. In this activity, you will work with datasets from **Kaggle**, an online community of people passionate about data. To start this activity, you’ll create a Kaggle account, set up a profile, and explore Kaggle notebooks.

Every data analyst has a data community that they rely on for help, support, and inspiration. Kaggle can help you build your own data community.

Kaggle has millions of users in all stages of their data career, from beginners to data scientists with decades of experience. The Kaggle community brings people together to develop their data analysis skills, share datasets and interactive notebooks, and collaborate on solving real-life data problems.

Check out this [brief introductory video](https://www.youtube.com/watch?v=TNzDMOg_zsw) to learn more about Kaggle.

By the time you complete this activity, you will be able to use many of Kaggle’s key features. This will enable you to create notebooks and browse data, which is important for completing and sharing data projects in your career as a data analyst.

# **Step-By-Step Instructions**

Follow the instructions to complete each step of the activity. Then answer the questions at the end of the activity before going to the next course item.

# **Step 1: Create a Kaggle Account**

To get started, follow these steps to create a Kaggle account.

- **Note:** Kaggle frequently updates its user interface. The latest changes may not be reflected in the screenshots, but the principles in this activity remain the same. Adapting to changes in software updates is an essential skill for data analysts, and we encourage you to practice troubleshooting. You can also reach out to your community of learners on the discussion forum for help.

1. Go to [kaggle.com](http://www.kaggle.com/)

2. Click on the **Register** button at the top-right of the Kaggle homepage. You can register with your Google credentials or your personal email address.

[](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/IYyu_v30TLWf1ySw7-3bUA_de88dac3644749549da4d4c53eae76e1_b9qck2lbYKPG6d8c0zc-R0yd374e6hrStIZM7v9SLj9KVrS4PQQeVxt-I4qh6egNmLEKnprM8KeV3Ej0eq_DFRZ5YzwL8TbGn_vtUEjFa17Tq9hBIOtHHDzOTG7zkfs2msKMAEPmAxxr0qK22u3Q1w?expiry=1716681600000&hmac=NF2G-J1sQv_5Lx_epe3nLZgWmWnrDm4BNr_Is69M6Bs)

3. Once you’re registered and logged in to Kaggle, click on the **Account** icon at the top-right of your screen. In the menu that opens, click the **Your Profile** button.

[](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/xlpf1SfJRvaxV_0IXtCB_A_9f6515a5488c47c5bf12d6e3bebcc4e1_4NPP0ViLuk1469y35yaVzGzXPPPigfDDMBU9GJmYzSrgciwFMunFBAFfYD1cLmh76MCIsLTkI9dKZjWZxHeAVCQ2TbsItDTvKatvaaK5iPLMZcxjg_U4lSV5m6kIltg3eVVesPcHtdfQ7jMGS_JMHg?expiry=1716681600000&hmac=IaJo5yZjdnhUjYPXaKlVXZ0m9GHNNin1BuA7HzinfVQ)

4. On your profile page, click on the **Edit Profile** button. Enter any information you’d like to share with the Kaggle community. Your profile will be public, so only enter the information you’re comfortable sharing.

[](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/fMQQQsQiQ5GQX2fJQm4fTA_b218b97c493a4f0dacdb30c196f505e1_ME5YTCPD5TxES7oRqaI6IB7iHnskDZee6PHKtgH3BPb4DhiG4qImp7Z5dvdTzo4i3XjTsjcqR7qjgWCm3zpiPrFojtL3SuqRNIKC7YHtibzpipEOn6ePOhtMyFChxAwf0tf25tEWCmJ4NmLX9ZUQfw?expiry=1716681600000&hmac=-TZoIjltiYlfwYPL_2VP9wi4agTLk4vHu-SJd9OdHdY)

5. If you want some inspiration, check out the profile of [Kaggle’s Community Advocate, Jesse Mostipak](https://www.kaggle.com/jessemostipak)!

# **Step 2: Go to the Code Home Page**

Now that you’ve created an account and set up your profile, you can check out some notebooks on Kaggle. Kagglers use **notebooks** to share datasets and data analyses.

First, go to the **Navigation** bar on the left side of your screen. Then, click on the **Code** icon. This takes you to the Code home page.

[](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/2Im1ehCqTvSb7k_5s_XAfw_a0cc4481944a433ea1844ce623bb8ce1_FnmeSfYhEr6as3uvZv7-aic2Hbr1fySQ_mJNZbUFYbAzMbQO5WYSIFMyZg1GKsH0uA2fhK1gOnkTjQthwKTDUCgoeGTyoLasKtJmZlkoZPIwoZdPRljfmOvP-ibVa8CzMrC-GmKLjWgqfn4orldcPA?expiry=1716681600000&hmac=5x3ACJa6sg4m51bpVrK-iZbr7zkp6UtvQvloGoHVGRc)

# **Step 3: Review Kaggler Contributions**

On the Code home page, you’ll notice links to notebooks created by other Kagglers.

To begin, feel free to scroll through the list and click on notebooks that interest you. As you explore, you may come across unfamiliar terms and new information: That’s fine! Kagglers come from diverse backgrounds and focus on different areas of data analysis, data science, machine learning, and deep learning.

# **Step 4: Narrow Your Search**

Once you’re familiar with the Code home page, you can narrow your search results by typing a word in the search bar or by using the filter feature.

For example, enter **Beginner** in the search bar to show notebooks tagged as beginner-friendly. Or, click on the **Filter** icon, the triangle shape on the right side of the search bar. You can filter results by tags, programming language, output, and other options. Filter to **Datasets** to show notebooks that use one of the tens of thousands of public datasets available on Kaggle.

# **Step 5: Review Suggested Notebooks**

If you’re looking for specific suggestions, check out the following notebooks:

- [gganimatehttps://www.kaggle.com/mrisdal/space-is-the-place](https://www.kaggle.com/mrisdal/space-is-the-place) by Meg Risdal
- [Getting staRted in R](https://www.kaggle.com/rtatman/getting-started-in-r-first-steps) by Rachael Tatman
- [Writing Hamilton Lyrics with TensorFlow/R](https://www.kaggle.com/anasofiauzsoy/writing-hamilton-lyrics-with-tensorflow-r) by Ana Sofia Uzsoy
- [Dive into dplyr (tutorial #1)](https://www.kaggle.com/jessemostipak/dive-into-dplyr-tutorial-1) by Jesse Mostipak

Spend some time checking out a couple of notebooks to get an idea of the work that Kagglers share online—and that you’ll be able to create by the time you’ve finished this course!

# **Step 6: Edit a Notebook**

Now, take a look at a specific notebook: [Dive into dplyr (tutorial #1)](https://www.kaggle.com/jessemostipak/dive-into-dplyr-tutorial-1) by Jesse Mostipak. Follow these steps to learn how to edit notebooks:

1. Click on the link to open up the notebook. It contains the dataset you’ll work with later on.

2. Click on the **Copy and Edit** button at the top-right to make a copy of the notebook in your account. Now, the notebook appears in **Edit** mode. Edit mode lets you make changes to the notebook if you want.

[](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/mmsb_ijpRiyM4loVN02naw_e2ee26f96fd6453393172576bd265ee1_2IwAnhAn2w5o_U_l707YX-LbkOSFZaJ61AtaiNP5URR0TLCXx3yFnHtDZT5fweBsBkMHyGL-rk44FPI7_mQw72e4QnUNCg8Yu2osXsnT_TvFDuMC5GNsVQ_6vfGVpoGcD9MAsfqq2Bj-e9yYRLrU8A?expiry=1716681600000&hmac=VsUd5ygXwU8OcPp8qoDKak9H-dYEALLmTOuG56qP828)

This notebook is private. If you want to share your work, you can choose to make it public. When you copy and edit another Kaggler’s work, always make meaningful changes to the notebook before publishing it. That way, you’re not misrepresenting someone else’s work as your own.

3. Take a moment to explore the Edit mode of the notebook.

Some of this may seem unfamiliar—and that’s just fine. By the end of this course, you’ll know how to create a notebook like this from scratch!

# **Step 7: Work with Datasets in Notebooks**

Now, you can check out the data!

In this notebook, you’ll find the data in a box labeled **Data** at the top-right of your screen. In the box, there’s an input folder with the title: **palmer-archipelago-antarctica-penguin-data**. Follow these instructions to explore the datasets and learn more about the data within them:

1. Click on this title. Two .csv files appear: **penguins_lter.csv** and **penguins_size.csv**. Click on one of them. At the bottom of the notebook, you’ll now find an interactive data table with all the information from the dataset.

[](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/mIZVQr6KSnuuy2C9Vh-c8w_ccb41f21ed38407489071c9db047f6e1_cgokcHkedRl6gSqVubJlcUBZYN3sElSfJ27aWVElp2a0ol0Fnm_8oeyHntg2zIOJhvUfZDPzlZgGtq8eBpyTXTjrVhslAZ9pNV89_xqvsU-L9F5NbXrYIQ1i7Z5WZY8__oKvsHUWv7oF9SLoH2U9KA?expiry=1716681600000&hmac=8giJMKZNgBaNkt8kd3tH00C_mqeaQiAQKCTjF5M7emo)

2. Click on the other .csv file. This opens a second tab with the second dataset.

3. Take a moment to check out each dataset.

4. Sort the data in each column by clicking on the **horizontal bars** to the right of each column name.

5. Click on the button that says **10 of 17 columns** to change the columns that are visible in the table.

In the dropdown menu, there’s a checkmark next to the name of each column that appears in the table. Checking or unchecking one of these boxes will change what data is presented.

Congratulations! You’ve explored several ways to interact with the dataset. This will help you get familiar with the Kaggle interface. You can save the notebook you worked in for future reference. Coming up, you’ll learn more about other ways you can use Kaggle.

---