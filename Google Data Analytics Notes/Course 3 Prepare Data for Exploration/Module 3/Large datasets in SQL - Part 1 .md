# Large datasets in SQL - Part 1.

---

# Get to know BigQuery, including sandbox and billing options

- Now we're going to explore the different account that Big Query offers, so you know how to choose the right one for your needs and how you can access them. Big Query's offer to you at no charge.
- There are paid options available, but we won't need them for the activities in this course. Instead, we're going to talk about two account types, sandbox and free trial.
    - A sandbox account is available at no charge and anyone with a Google account can log in and use it. There are a couple of limitations to this account type. For example, you get a maximum of 12 projects at a time. This means that if you want to make a 13th project, you'll have to delete one of your original 12.
    - It also doesn't allow you to insert new records to a database or update the field values of existing records. These Data Manipulation Language or DML operations aren't supported in the sandbox. However, you won't need to do this in course activities, You can read more about the limitations of a sandbox account in the Big Query documentation.
    - This is the account type we'll use for most of our activities. Before that though, we should talk about the other way to use Big Query without charges, the Google Cloud Free trial. The free trial gives you access to more of what Big Query has to offer with fewer overall limitations.
- The free trial offers 300 dollars in credit for use in Google Cloud during the first 90 days. You won't get anywhere near that spending limit if you just use the Big Query console to practice SQL queries.
- After you spend the 300 dollars credit or after 90 days, your free trial will expire and you will need to personally select to upgrade to a paid account to keep working in Google Cloud. Your method of payment will not be automatically charged after your free trial ends. The free trial does require that you set up a payment option with Google Cloud, but unless you choose to opt in for an account upgrade, it won't charge you. However, it does require you to enter a payment type, so we understand if you don't feel comfortable with this option.
- This is one reason the Big Query sandbox account exists, so you don't have to enter any payment information. With either type of account, you can upgrade to a paid account at any time and retain all of your existing projects. If you set up a free trial account, but choose not to upgrade to a paid account when your trial period ends, you can set up a free sandbox account at that time.

---

# Set up your BigQuery account

As you’ve been learning, BigQuery is a database you can use to access, explore, and analyze data from many sources. Now, you’ll begin using BigQuery, which will help you gain SQL knowledge by typing out commands and troubleshooting errors. This reading will guide you through the process of setting up your very own BigQuery account.

**Note:** Working with BigQuery is not a requirement of this program. Additional resources for other SQL database platforms are also provided at the end of this reading if you choose to use them instead.

## BigQuery account options

BigQuery offers a variety of account tiers to cater to various user needs and has two free-of-charge entry points, a sandbox account and a free-of-charge trial account. These options allow you to explore the program before selecting the best choice to suit your needs. A sandbox account allows you to practice writing queries and to explore public datasets free of charge, but it has [quotas and limits](https://cloud.google.com/bigquery/quotas), as well as some additional [restrictions](https://cloud.google.com/bigquery/docs/sandbox#limits). If you prefer to use BigQuery with the standard limits, you can set up a free-of-charge trial account instead. The free-of-charge trial is a trial period prior to paying for a subscription. In this instance, there is no automatic charge, but you will be asked for payment information when you create the account.

This reading provides instructions for setting up either account type.  An effective first step is to begin with a sandbox account and switch to a free-of-charge trial account when needed to run the SQL presented upcoming courses.

### **Sandbox account**

The sandbox account is available at no cost, and anyone with a Google account can use it. However, it does have some limitations. For instance, you are limited to a maximum of 12 projects at a time. This means that, to create a 13th project, you'll need to delete one of your existing 12 projects. Additionally, the sandbox account doesn't support all operations you’ll do in this program. For example, there are limits on the amount of data you can process and you can’t insert new records into a database or update the values of existing records. However, a sandbox account is perfect for most program activities, including all of the activities in this course. Additionally, you can convert your sandbox account into a free-of-charge trial account at any time.

**Set up your sandbox account**

To set up a sandbox account:

1. Visit the [BigQuery sandbox documentation](https://cloud.google.com/bigquery/docs/sandbox#limits) page.
2. Log in to your preferred Google account by selecting the profile icon in the BigQuery menu bar.
3. Select the **Go to BigQuery** button on the documentation page.
4. You'll be prompted to select your country and read the terms of service agreement.
5. This will bring you to the **SQL Workspace**, where you'll be conducting upcoming activities. By default, BigQuery creates a project for you.

After you set up your account, the name of the project will be in the banner in your BigQuery console.

### **Free-of-charge trial**

If you wish to explore more of BigQuery's capabilities with fewer limitations, consider the Google Cloud Free Trial. It provides you with $300 in credit for Google Cloud usage during the first 90 days. If you're primarily using BigQuery for SQL queries, you're unlikely to come close to this spending limit. After you've used up the $300 credit or after 90 days, your free trial will expire, and you will only be able to use this account if you pay to do so. Google won't automatically charge your payment method when the trial ends. However, you'll need to set up a payment option with Google Cloud. This means that you’ll need to enter your financial information. Rest assured, it won't charge you unless you consciously opt to upgrade to a paid account. If you're uncomfortable providing payment information, don't worry; you can use the BigQuery sandbox account instead.

**Set up your free-of-charge trial**

1. Go to the [BigQuery](https://cloud.google.com/bigquery) page.
2. Select **Try BigQuery free**.
3. Log in using your Google email, or create an account free of charge if you don't have one. [Click here](https://cloud.google.com/bigquery?utm_source=google&utm_medium=cpc&utm_campaign=na-US-all-en-dr-bkws-all-all-trial-e-dr-1605212&utm_content=text-ad-none-any-DEV_c-CRE_665665924750-ADGP_Hybrid+%7C+BKWS+-+MIX+%7C+Txt_BigQuery-KWID_43700077225652770-kwd-274188433361&utm_term=KW_bigquery%20account-ST_bigquery+account&gclid=CjwKCAjwkNOpBhBEEiwAb3MvvYQXjIQ4TRnkITJoSXz7DFez4T-XKPG5IpfKmxUg2iHPEmiJBNQByhoCLVgQAvD_BwE&gclsrc=aw.ds) to create an account.
4. Select your country, a description of your organization or needs, and the checkbox to accept the terms of service, Then select **CONTINUE**.
5. Enter your billing information and select **START MY FREE TRIAL**.

After you set up your account, your first project, titled **My First Project** will be in the banner.

[](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/nPKEbQPYTmip--sRPjtdTg_abb38e9bd5184c819f281c1e9b158ee1_TxbPN1aMvNB0uHj9f_VPMKaR92Jc2lj-imVMbn1PGPp0Ul2RUg4NxoXnZEuatKnd9XcFgJbsAim6C3tFK2vcJFYDhvQzeDCZw3GBtKJ6PGi4hCzxjeOnoVQwro9swBy_cU9fFUuM1Acw7uN-UULx4Lc?expiry=1716768000000&hmac=eunRay1IGeXwqLRUwaNOTbAh9s2l7XBsiTZnzj6rxgo)

### **Transferring between BigQuery accounts**

With either a sandbox or free-of-charge trial account, you have the flexibility to upgrade to a paid account at any time. If you upgrade, all your existing projects will be retained and transferred to your new account. If you started with a free-of-charge trial, but choose not to upgrade when it ends, you can switch to a sandbox account. However, note that projects from your trial won't transfer to your sandbox. Essentially, creating a sandbox is like starting from scratch.

## Get started with other databases (if not using BigQuery)

It’s easiest to follow along with the course activities if you use BigQuery, but you may use other SQL platforms, if you prefer. If you decide to practice SQL queries on other database platforms, here are some resources to get started:

- [Getting Started with MySQL](https://dev.mysql.com/doc/mysql-getting-started/en/)
- [Getting Started with Microsoft SQL Server](https://docs.microsoft.com/en-us/sql/relational-databases/tutorial-getting-started-with-the-database-engine?view=sql-server-ver15)
- [Getting Started with PostgreSQL](https://www.postgresql.org/docs/10/tutorial-start.html)
- [Getting Started with SQLite](https://www.sqlite.org/quickstart.html)

## Key takeaways

BigQuery offers multiple account options. Keep the following in mind when you choose an account type:

- **Account tiers:** BigQuery provides various account tiers to cater to a wide range of user requirements. Whether you're starting with a sandbox account or exploring a paid account with the free-of-charge trial option, BigQuery offers flexibility to choose the option that aligns best with your needs and budget.
- **Sandbox limitations:** While a sandbox account is a great starting point, it comes with some limitations, such as a cap on the number of projects and restrictions on data manipulation operations like inserting or updating records, which you will encounter later in this program. Be aware of these limitations if you choose to work through this course using a sandbox account.
- **Easy setup and upgrades:** Getting started with any BigQuery account type is quick and easy. And if your needs evolve, you have the flexibility to modify your account status at any time. Additionally, projects can be retained even when transitioning between account types.

Choose the right BigQuery account type to match your specific needs and adapt as your requirements change!

---

# Get started with BigQuery

BigQuery is a data warehouse on the Google Cloud Platform used to query and filter large datasets, aggregate results, and perform complex operations. Throughout this program, you’re going to use BigQuery to practice your SQL skills and collect, prepare, and analyze data. At this point, you have set up your own account. Now, explore some of the important elements of the SQL workspace. This will prepare you for the upcoming activities in which you will use BigQuery. Note that BigQuery updates its interface frequently, so your console might be slightly different from what is described in this reading. That’s okay; use your troubleshooting skills to find what you need!

## Log in to BigQuery

When you log in to BigQuery using the landing page, you will automatically open your project space. This is a high-level overview of your project, including the project information and the current resources being used. From here, you can check your recent activity.

[](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/zSYVq72kR0y7WzL1pgNc6A_6d488f739f76484db684f7e9eab65df1_0SQ2qZhV9Uve0ublmVbbrNTl-s-kh53u4jOMLUrGSLLEf2XpUoXa1zw25R7t_OYoOdLGrdHOuQxrK0E7CJd0S_XsrLRRfISCDEWA_Gd35TCHCPeVl2vQPhVR4T1Xq7xLmahZlsSC7H6YQ0HlV3lt2A?expiry=1716768000000&hmac=PRpCSOAIrB0GggbmWibkZfIQsss70VNrkvt_oQGoco8)

Navigate to your project’s BigQuery Studio by selecting BigQuery from the navigation menu and BigQuery Studio from the dropdown menu.

[](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/-MXZRs1VSlaYQoNdSuaEeQ_7c326ba811b94494b3765af0665e48f1_aOUMY9S3wkh6BQGfj6qTt8IoNUoYjdiOwCxQnabM55gQxjYOC5ZgMfTEBEfbmdb_tPb7wB7OcYwL4YTpmQm1j9Q5ad_PXXHkMKwXnsRLrd_pw_wfjaS338JKUDRRTQD_QghTMWCL-XB5rx4lnkpgeA?expiry=1716768000000&hmac=j6qtFy564DxSKAaaSwONQBICe5Rmqf6eO1c-VXpQ7t0)

## BiqQuery Studio components

Once you have navigated to BigQuery from the project space, most of the major components of the BigQuery console will be present: the **Navigation** pane, the **Explorer** pane, and the **SQL Workspace**.

[](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/nE2ZdMl1SnK7TI96C948Bw_6e0e1784f33f4d45a95be098a97e55f1_VUTfKOpAyhpnBNwq5gIvSY1XeRI9uIGdnFtSMneBLi_ee26vDJiMawU6WaGXNKUGQgP2ZF0O0vAffbfyLSTwjsHirfKaOGVoRwiseloEoEC8KHJCKcpH-RG4aH76Bn_Dbbv9ORkOcVUQxE6gJp3pEw?expiry=1716768000000&hmac=USSyEQk2-zVYQ13Kk1VMh_-mxok0_RknfWUX3voga_w)

### The Navigation pane

On the console page, find the **Navigation** pane. This is how you navigate from the project space to the BigQuery tool. This menu also contains a list of other Google Cloud Project (GCP) data tools. During this program, you will focus on BigQuery, but it’s useful to understand that the GCP has a collection of connected tools data professionals use every day.

### The Explorer pane

The **Explorer** pane lists your current projects and any starred projects you have added to your console. It’s also where you’ll find the **+ ADD** button, which you can use to add datasets.

[](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/Ad6Ow3GIQyaQHxHwUBk95w_09178209a91c424ca34335868575c7f1_AcVuKsC0sM954ZbLaGfh3JFTTDUzV9CpWHkPo9NeVV-LD_pNqPCMRGPdN0cHtTyq-LS1rJw8u8rRHcFtA017adW25jxmjnSOXpZBw0SYx7nZKDoOyL_bB8j_9OhPn8tptxHQldEChmurTDzPPoOhWQ?expiry=1716768000000&hmac=1k2UjPYNptHhMe6opF6aQI7YmCnJ8qOi3x7f2rQuHq4)

This button opens the **Add** dialog that allows you to open or import a variety of datasets.

[](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/xHBnGi22RP6GMwl-i5u5Cg_e9a99caf7b5d4a3da024a6e05495a3f1_qUqHKMnIzsLQgZ0mp8ED9t5L20O3h5x3yqY_FrJmSmNBL_uYpM8Za5zb443dXlQKQP-CQjDUhskGQ8001xVu0b5A70AATT7K0C8yrBTr95Jgq1LJjQVYPrtEeZ-QUqDmhBw-IL_u9N_nr3cO1FE94Q?expiry=1716768000000&hmac=1FBYBiV0exg_GGja6llYKHQciS-ENy2CUiEwfuk0lWc)

### Add Public Datasets

BigQuery offers a variety of public datasets from the Google Cloud Public Dataset Program. Scroll down the **Add** dialog to the **Public Datasets** option.

[](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/tIxke21GTxyJ5zTtDVmklw_480308b97ab84ce19b3224a1df3912f1_f6FWP_Ot9vqu6v_mTpQv5Pc6z8ZfbG6ozjPCwHTp3a1gAoIa6_lI7FBubP85kcpbvWRkItc9xryUgEoWbaf10rYX5EPUNB4BraLuh3cXsZpF-UlhMQEfzGJjzb6mJQ-uSNPpqvNB1Lq1ZZjLdagBEw?expiry=1716768000000&hmac=-yO8fj5KrYAZ_Kn5LvsF9A5a8tJs-clM-Q2ehfyvDKE)

Select **Public Datasets**. This takes you to the **Public Datasets Marketplace**, where you can search for and select public datasets to add to your BigQuery console. For example, search for the "noaa lightning" dataset in the Marketplace search bar. When you search for this dataset, you will find NOAA’s Cloud-to-Ground Lightning Strikes data.

[](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/EaJe6zbsTWm26hpoHSZmiw_92eda1f23f8d4bbb97197316fc4173f1_yw9cFdwcM-Vw9K68QMNfPzDFnxsuObE4a4S85aXmO3O2ODPdl4hKwq_r0s7H47lpi588qDHjaLnMEXgHBPeo1oVbkwAaZNT8MBO0JI8pab81Wgw8dB--VvTPGVEeJSBQ6pbHHse22FcbQ88Lw5l4Ow?expiry=1716768000000&hmac=le9oFALJChMk07cEm4xjFhTnteJedKAJhITIDO6v4lo)

Select the dataset to read its description. Select **View dataset** to create a tab of the dataset’s information within the SQL workspace.

The Explorer Pane lists the noaa_lightning and other public datasets.

[](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/NxcREvGtRT-hKcyMTwegGw_95a1788086aa4b0f8286ab250683d5f1_zy1RC8p_TOnwP-UdCWeVJhk6XcjefHtJx1XgS7mVJP4aBnLgtiVAJw3whnI8wsXN2uwOF11rVbgrQkpRyQBSQ7LtNog15ml2C2fQJxLRyx6DIZPXrne75GekTOMfKGeCU_QyI5DqJFY6iG4vh_uHrQ?expiry=1716768000000&hmac=1qIh5kZKkIHJEBYkW9XaYVGNV452R90bfV1vVwzDyhA)

### Star and examine Public Datasets

You added the public noaa_lightning dataset to your BigQuery Workspace, so the **Explorer** pane displays the noaa_lightning dataset, along with the list of other public datasets. These datasets are nested under bigquery-public-data. Star bigquery-public-data by navigating to the top of the **Explorer** pane and selecting the star next to bigquery-public-data.

[](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/Vb38hh2PTMO7f5hWoOclmg_e875ba2198f247d9b50244e2c22f00f1_uSOwc1spWVztuBd3zACofaTQAJug_1pLUbZuGIPCDikeGGm1j0fTAVfddN5KpFeSkALs6Y0azBj1PA56mdAcfyt9lhxLkYj6hu3cg0hPoTg00MejHJd7WpjFE-0sf8scbIj9e7NNN8MLLXV64xcjMQ?expiry=1716768000000&hmac=33sfaEsJ-dAfUFAZYOIFnzD_HNDpRua9oIURHT374b4)

Starring bigquery-public-data will enable you to search for and add public datasets by scrolling in the **Explorer** pane or by searching for them in the **Explorer** search bar.

For example, you might want to select a different public dataset. If you select the second dataset, "austin_311," it will expand to list the table stored in it, “311_service_requests.”

The Explorer pane with the “bigquery-public data” and “austin_311” datasets expanded, revealing the “311_service_requests” table

[](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/ULNat2-ZTOOOILGo-_T04g_e4c3b3b84c064932b1bcddcc44c081f1_iY8pt2y3FVj9n70uXoTPgenZoBnBD-CB3iqI1B9U_Q-xOVPLDHGVuTda2SF1w0R7RTMOU59MnIn0VqpeL-B81enUpfXxjL8k3G9BdxeFwRDUQlSZTlM2ysDWrnStHOLxWDk9r8Cb_tXVPAV_zxYmEg?expiry=1716768000000&hmac=iZXWrESaGGM7vlOQpgL46IZOW3YbgxWHiTiyKnenbwI)

When you select a table, its information is displayed in the SQL Workspace. Select the 311_service_requests table to examine several tabs that describe it, including:

- **Schema**, which displays the column names in the dataset
- **Details**, which contains additional metadata, such as the creation date of the dataset
- **Preview**, which shows the first rows from the dataset

[](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/qE13RxJNToOy6wR47z2r9Q_a80a3276da3b4b1c9e404b02d1a8faf1_vgfiDeBifjMZ7WhLdo6bDALvpeMTqcjmvvucEljOAeiPypKqIwB5qBNYQp3O3rH3QYpS2W-cBHzzsMwZAxRCavITHl_R8pEqFkF9yNHSSTWmiguvaABcckK2av0lydHR5g_1rZynrv5D-YW3v7WPDQ?expiry=1716768000000&hmac=jlF_ZEjMYj7kAonc8IKQggwjJZcm_8TmBZNw7acpNno)

Additionally, you can select the **Query** button from the menu bar in the SQL Workspace to query this table.

### The SQL Workspace

The final menu pane in your console is the SQL Workspace. This is where you will actually write and execute queries in BigQuery.

[](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/816UKsT-Q4-UYz-i8Z01eA_f6a774eacc06448ea8b599d975338df1_AVYekXAnrQhzN7Mpgy289kYI_YgK32S2rALCiiey74FlRJwXoEoL7wjcwq7OL8Q8regbHulTdwdX1zQfA_sI04B5F1AbqNecgYTPPWnv344_Ow1VesE1zrOfDb1HNiCroQMDYENDd2lWe2onXVo0Rw?expiry=1716768000000&hmac=xL9jj1k8q9TULqTPceeIXmglunUbhzfVK9AKQaldaj0)

The SQL Workspace also gives you access to your personal and project history, which stores a record of the queries you’ve run. This can be useful if you want to return to a query to run it again or use part of it in another query.

## Upload your data

In addition to offering access to public datasets, BigQuery also gives you the ability to upload your own data directly into your workspace. Access this feature by opening the **+ ADD** menu again or by clicking the three vertical dots next to your project’s name in the Explorer pane. This will give you the option to create your own dataset and upload your own tables. You will have the opportunity to upload your own data in an upcoming activity to practice using this feature!

## Key takeaways

BigQuery's SQL workspace allows you to search for public datasets, run SQL queries, and even upload your own data for analysis. Whether you're working with public datasets, running SQL queries, or uploading your own data, BigQuery’s SQL workspace offers a range of features to support all kinds of data analysis tasks. Throughout this program, you will be using BigQuery to practice your SQL skills, so being familiar with the major components of your BigQuery console will help you navigate it effectively in the future!

---

# Step-by-Step: BigQuery in action

This reading provides you with the steps the instructor performs in the following video, [BigQuery in action](https://www.coursera.org/learn/data-preparation/lecture/H877e/bigquery-in-action). The video focuses on how to create a query to view a small section of data from a large dataset.

Keep this guide open as you watch the video. It can serve as a helpful reference if you need additional context or clarification while following the video steps. This is not a graded activity, but you can complete these steps to practice the skills demonstrated in the video.

## What you'll need

To follow along with the examples in this video, log in to your BigQuery account and follow the instructions to star **bigquery-public-data** in **The Explorer pane** section of the previous reading, [Get Started with BigQuery](https://www.coursera.org/learn/data-preparation/supplement/7ctZ8/get-started-with-bigquery).

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/BZoPGCbqS32aDxgm6mt9kg_bfbeb57eeb1743938a5041c2251e2ff0_line-y.png?expiry=1716768000000&hmac=SwwvN04jNbx_RUJgwdZiqPahKT70LMxudzjX21sLCvU)

## Example 1: Preview a section from a table viewer

A database is a collection of data stored in a computer system. Query languages such as SQL enable communication between databases and data analysts. You discovered earlier that a relational database is made up of several tables that may be joined together to create relationships. Primary and foreign keys serve as representations of these relationships. To extract data from these tables, data analysts use queries. To learn more about that, explore BigQuery in action:

1. Log in to [BigQuery](https://console.cloud.google.com/bigquery) and go to your console. You should find the **Welcome to your SQL Workspace!** landing page open. Select **COMPOSE A NEW QUERY** In the Bigquery console. Make sure that no tabs are open so that the entire workspace is displayed, including the **Explorer** pane.
2. Enter **sunroof** in the search bar. In the search results, expand **sunroof_solar** and then select the **solar_potential_by_postal_code** dataset.
3. Observe the **Schema tab** of the **Explorer** pane to explore the table fields.
4. Select the **Preview** tab to view the regions, states, yearly sunlight, and more.

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/ThjXwvDfS7iKuIFqJl1law_9400d10233664d95909d65e3628294e1_C3M3L5_BigQuery-in-Action---Interface.png?expiry=1716768000000&hmac=ssK0EH27ztlt9avt4hV1QQ65cHHeCmICKy8qWnQdwvE)

## Example 2: Writing a query

In order to view the entire dataset, you will need to write a query.

1. The first step is finding out the complete, correct path to the table you want to work with. Select the **ellipses** (three vertical dots) by the dataset **solar_potential_by_postal_code**, then select **Query**. A new tab will populate on your screen. Select the tab. The path to the table should be written inside two backticks.
2. Select the full path by highlighting the text including the backticks and copy it. (**Note:** You can also get the full path to the project, database, and table directly by clicking the ellipses next to the table's name in the **Explorer** panel on the left and selecting **Copy ID**.)
3. Now, click on the **plus sign** to create a new query. Notice that BigQuery doesn’t automatically generate a **SELECT** statement in this window. Enter **SELECT** and add a space after it.
4. Put an asterisk **** after **SELECT** to indicate you want to return the entire dataset. The asterisk lets the database know to include all columns. Without this shortcut, you would have to manually enter every column name!
5. Next, press the **Enter/Return** key and enter **FROM** on the second line. **FROM** indicates where the data is coming from. After **FROM**, add another space.
6. Paste in the path to the table that you copied earlier. It will read **`bigquery-public-data.sunroof_solar.solar_potential_by_postal_code`**
7. Execute the query by selecting the **RUN** button.

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/rYUm3T87RdGKoCmagUNS2Q_e3e66f46b4754729be3e5e02e4d7bde1_C3M3L5_BigQuery-in-Action---select-query.png?expiry=1716768000000&hmac=GphWRvQ3_IV5w8-p_1nCwtzclJGQCMbIS9ZjLdXoapg)

**Important!**

Many of the public databases on BigQuery are living records and, as such, are periodically updated with new data. Throughout this course (and others in this certificate program), if your results differ from those you encounter in videos or screenshots, there's a good chance it is due to a data refresh. You can verify when a table has been refreshed by selecting it from the **Explorer** panel and clicking **Details**. You'll find the date the table was created, when it was last modified, as well as other useful information.

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/MOWPw5e-Scm9IajeMKUSrQ_072a88649e6d4112b421e871848da6f1_DA_C3M3L5_BigQuery_in_action_details_view.png?expiry=1716768000000&hmac=QFcw7KrCsMvJtvb3jK94iowK9uXiIIxuASsVEIo5FD4)

## Example 3: Use SQL to view a piece of data

If the project doesn’t require every field to be completed, you can use SQL to see a particular piece, or pieces, of data. To do this, specify a certain column name in the query.

1. For example, you might only need data from Pennsylvania. You’d begin your query the same way you just did in the previous examples: Click on the **plus sign**, enter **SELECT**, add a space, an asterisk (****), and then press **Enter/Return**.
2. Enter **FROM** and then paste **`bigquery-public-data.sunroof_solar.solar_potential_by_postal_code`**. Press **Enter/Return**.
3. This time, add **WHERE**. It will be on the same line as the **FROM** statement. Add a space and enter **state_name** with a space before state and a space after name. **state_name** is a column name in the table.
4. Because you only want data from Pennsylvania, add **=** and **'Pennsylvania'** on the same line as **state_name**. In SQL, single quotes represent the beginning and ending of a string.
5. Execute the query with the **RUN** button.
6. Review the data on solar potential for Pennsylvania. Scroll through the query results.

Keep in mind that SQL queries can be written in a lot of different ways and still return the same results. You might discover other ways to write these queries!

## Video guide

[index.mp4](Large%20datasets%20in%20SQL%20-%20Part%201%205c83b0d45dca4d52b5e38b590457f345/index.mp4)

---

# Hands-on activity: Intro to BigQuery

## Activity overview

You have recently been introduced to BigQuery, a data warehouse on Google Cloud that data analysts use to query, filter large datasets, aggregate results, and perform complex operations. In this activity, you will explore the BigQuery interface; upload public data to your console; and write some simple SQL queries using **SELECT**, **FROM**, and **WHERE**.

By the time you complete this activity, you will be more familiar with writing queries in the BigQuery interface. This will enable you to practice SQL, which is important for working with databases in your career as a data analyst.

# **Step-By-Step Instructions**

Follow the instructions to complete each step of the activity. Then answer the questions at the end of the activity before going to the next course item.

# **Step 1: Get a BigQuery account**

For this activity, you will need a BigQuery account. If you haven’t made one already, follow the instructions from the [Using BigQuery](https://www.coursera.org/learn/data-preparation/supplement/DYOQK/using-bigquery) reading.

Once you have your account, start exploring!

# **Step 2: Open your BigQuery console**

1. Log in to [BigQuery](https://cloud.google.com/bigquery).

2. Select the **Go to console** button on the BigQuery homepage. This will open a new tab with your console.

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/0VOTqd2RS4aCEC-vuXEqag_0528281344b3421d9a884a6729b19de1_C3M3L5_A_02_Graphic01.png?expiry=1716768000000&hmac=Wnu4yIDE6u78uk404iceDm1v1m-DkaYbueX0XrD8XcY)

3. Take a moment to explore your console. The **Explorer** menu includes a search bar you can use to find resources, pinned projects, and the **+ ADD** button for adding data. The Editor welcome page is where you will navigate to a query editor, try sample data, add local data files, add Google cloud storage, or add other external connections. You can also find your job history, query history, and saved queries here.

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/6R7hrNZXSBKVuRKJGBGZqQ_25137ce3894b44e0bb3c41a0a06fbde1_C3M3L5_A_02_Graphic02.png?expiry=1716768000000&hmac=T6VPUz1xOmEuWW27xop6Dgn_YcBUY7AsMDui5CSB_Ww)

## 

# **Step 3: Access public data in BigQuery**

In order to start writing queries, you will need some data to work with. Once you’re familiar with the BigQuery interface, you can access a public dataset directly from your console.

1. Select the search bar in the **Explorer** pane.

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/tD3l7u2KT_K23DfUwAPc4g_e656c21d01de498ba827e3e5fd1e7be1_C3M3L5_A_02_Graphic03.png?expiry=1716768000000&hmac=0jXQsw-AdUyXql4tVqMH6D3YO_AJLvi41XXNFC_nFCU)

2. Enter “london bicycle” in the search box and press enter; this will return the **london_bicycles** database from the Greater London Authority. Select the database for more details. If you cannot find it, make sure you're searching in all projects. The **london_bicycles** database is in the **bigquery-public-data** project.

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/sAfL_5_PTnSVGoWkdF_Gzg_a50ff730ec97430f9da3cb65e85b46e1_C3M3L5_A_02_Graphic04.png?expiry=1716768000000&hmac=9cfEHVwzMLbp_8jB8AkLvAvl7uAmGyWuZkRuQhsQ-Vc)

3. Select the arrow to the left of the **london_bicycles** database name. This expands the dataset to reveal two table names: **cycle_hire** and **cycle_stations**. Select the **cycle_hire** table name within the **Explorer** pane.

Screenshot of BigQuery. The titles cycle_hire and cycle_stations are shown beneath london_bicycles in the explorer pane. Cycle_hire is selected.

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/mBSw6_dARki7phmB5OBifA_e7ffd456c1b7444fb7af0c25fed3f1e1_C3M3L5_A_02_Graphic05.png?expiry=1716768000000&hmac=rsI0E5JZilvRH-LQgyeYhVgLn5igxgFPz8deLrCYADE)

This will pull the **cycle_hire** schema into the console. Take a moment to explore the field names and the associated information.

4. Now, select the **PREVIEW** tab to find a sample of the data that you’ll be working with.

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/h3L6Qu2XReKSvWIhuUDv5g_03370e5f5bc3486d822009465d28d2e1_C3M3L5_A_02_Graphic06.png?expiry=1716768000000&hmac=_dVAf9AuFluvaxqRco3Ft6hKf3zi7YNb5R6Yeh7aK_0)

Once you have finished previewing the data, write a query!

## 

# **Step 4: Review basic parts of a query**

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/D_w9YrY-QNa8PWK2PmDW6g_b8b9c2559de24ddc9ce059766c5ff7b6_line-y.png?expiry=1716768000000&hmac=3lavKdz16IjkalrjQ8L6x7VhT2z8ghd3tSZl4vkYh_A)

So far, you’ve learned three basic parts of a query: **SELECT**, **FROM**, and **WHERE**. As a refresher:

- **SELECT** is the section of a query that indicates what data you want SQL to return to you.
- **FROM** is the section of a query that indicates which table the desired data comes from. You must provide a full path to the table. The path includes the project name, database name, and table name, each separated by a period.
- **WHERE** is the section of a query that indicates any filters you’d like to apply to your table.

# **Step 5: Write a basic query**

Now, construct a simple command using the basic parts of a query you have already learned! For example, you can select a specific column from the **cycle_hire** table, such as the **end_station_name** column.

1. Select the **Blue +** button or **QUERY - In new tab** to start a new query.

2. Start your query with a **SELECT** clause, and indicate which column you want to select from the table; in this case, you’ll input **end_station_name**.

3. After you have indicated which column you are selecting, write your **FROM** clause. Specify the table you are querying from by inputting the following location: **`bigquery-public-data.london_bicycles.cycle_hire`;**

The completed query should appear like this:

![Untitled](Large%20datasets%20in%20SQL%20-%20Part%201%205c83b0d45dca4d52b5e38b590457f345/Untitled.png)

4. Run your completed query by selecting the blue **RUN** button.

This query may take a few seconds to execute. Once it has finished, you will find the list of station names you requested under the **Query Results** console pane.

# **Step 6: Write a query to answer a question**

After running the first basic query, try answering a specific question about the data. For example, how many bike trips lasted for 20 minutes or longer?

1. Select the **Blue +** button or **QUERY - In new tab** to start a new query. Start with your **SELECT** statement again. This time, include the two columns **duration** **and **start_station_name** in the query. The data in these columns will tell where the trip started and the duration of the trip. Be sure to separate each column name with a **comma**.

2. Next, add your **FROM** statement. You will be using the same table as the previous query: **FROM `bigquery-public-data.london_bicycles.cycle_hire`;**. **Note:** The backticks around the table in this line of code are optional.

3. Finally, add a **WHERE** statement to specify that you want to filter for only bike rides 20 minutes or longer. If you check the preview of this data, you might notice that the **duration** is recorded in seconds, so you’ll specify 1200 seconds in your query. Write that as **WHERE duration >= 1200;**

Your completed query should be written like this:

![Untitled](Large%20datasets%20in%20SQL%20-%20Part%201%205c83b0d45dca4d52b5e38b590457f345/Untitled%201.png)

4. Run your completed query by clicking the **RUN** button.

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/gisJ6DMeSgC3ISZ9DxYK9w_4e4c6781870743ffb94ac08a8bc191e1_C3M3L5_A_02_Graphic07.jpg?expiry=1716768000000&hmac=bviwmvR0jMZ9bKxjuMytJHinycUUY4M2ojEGM2uFeCo)

This query may take a few seconds to execute. Once it has finished, you will find a list of rides from this table that fit your criteria. There are millions of rows with bike trips that are 20 minutes or longer!

# **Optional Step 7: Up for a challenge?**

If you’re comfortable using queries to answer questions, try creating and running queries to complete the tasks below:

- What is the name of the station whose **start_station_id** is 111?
- Return all the **rental_id**s, station IDs, and station names that **bike_id** 1710 started from.
- What is the **bike_model** of **bike_id** 58782?

# **Step 8: Check your work**

Use the solutions doc to check your work: [Intro to BigQuery Solutions](https://docs.google.com/document/d/1Rw8gXT0E4Smo4huoOcahX5ZQqV_pV8zgES8Oltatr-Y/template/preview)

Or download the file directly here:

[Intro-to-BigQuery-solutions.docx](Large%20datasets%20in%20SQL%20-%20Part%201%205c83b0d45dca4d52b5e38b590457f345/9KElwgWaT2yuZqs_AcEbpQ_a6e50e18806a49979215819d1a80f8f1_Intro-to-BigQuery-solutions.docx)

---