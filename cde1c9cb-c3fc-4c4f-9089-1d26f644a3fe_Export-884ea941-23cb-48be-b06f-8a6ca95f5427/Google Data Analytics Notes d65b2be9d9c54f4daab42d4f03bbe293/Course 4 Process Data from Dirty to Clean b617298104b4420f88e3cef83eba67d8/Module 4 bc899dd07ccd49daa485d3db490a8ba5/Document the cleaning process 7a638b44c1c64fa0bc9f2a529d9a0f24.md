# Document the cleaning process

---

# Capture cleaning changes

**Key Points:**

- **Importance of Documentation:**
    - Tracks changes, additions, deletions, and errors.
    - Allows for recovery of data-cleaning errors.
    - Informs other users of changes made.
    - Helps determine the quality of data for analysis.
- **Changelogs:**
    - Chronologically ordered list of modifications made to a project.
    - Can be accessed in spreadsheets and SQL.
- **Spreadsheet Changelogs:**
    - Use Sheet's version history to track changes.
    - View changes by individual cells or the entire worksheet.
    - Assign permission for others to browse the history.
- **SQL Changelogs:**
    - Method depends on the software program used.
    - Specify what you did and why when committing a query.
    - Add comments while cleaning data to construct a changelog later.
    - Use query history to track and revert to previous versions.
- **Benefits of Changelogs:**
    - Keep yourself on track.
    - Provide real-time updates to your team.
    - Facilitate communication and collaboration.

**Definitions:**

- **Changelog:** A file containing a chronologically ordered list of modifications made to a project.
- **Data Cleaning:** The process of identifying and correcting errors, inconsistencies, and missing values in a dataset.
- **Documentation:** The process of recording and tracking changes made to data during the cleaning process.
- **Query History:** A list of all the queries you have run in SQL, allowing you to revert to previous versions or find changes made.
- **Version History:** A feature in spreadsheets that tracks all changes made to the document, including who made them and when.

---

# Embrace changelogs

What do engineers, writers, and data analysts have in common? Change.

Engineers use **engineering change orders** (ECOs) to keep track of new product design details and proposed changes to existing products. Writers use **document revision histories** to keep track of changes to document flow and edits. And data analysts use **changelogs** to keep track of data transformation and cleaning. Here are some examples of these:

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/EctYxYsJQ0qiBJ7Q5V9f4g_166033fe62dd42f9bd0b23c8269161f1_Screenshot-2023-11-17-2.46.37-PM.png?expiry=1716854400000&hmac=wcWjH8Wc3QGcy2pW4v4kK4v02Ha66iASS1Z-__4jGSg)

## Automated version control takes you most of the way

Most software applications have a kind of history tracking built in. For example, in Google sheets, you can check the version history of an entire sheet or an individual cell and go back to an earlier version. In Microsoft Excel, you can use a feature called **Track Changes**. And in BigQuery, you can view the history to check what has changed.

Here’s how it works:

| Google Sheets | 1. Right-click the cell and select **Show edit history**.
2. Click the left-arrow < or right arrow > to move backward and forward in the history as needed. |
| --- | --- |
| Microsoft Excel | 1. If Track Changes has been enabled for the spreadsheet: click **Review**. ****
2. Under **Track Changes**, click the **Accept/Reject Changes** option to accept or reject any change made. |
| BigQuery | Bring up a previous version (without reverting to it) and figure out what changed by comparing it to the current version. |

## Changelogs take you down the last mile

A **changelog** can build on your automated version history by giving you an even more detailed record of your work. This is where data analysts record all the changes they make to the data. Here is another way of looking at it. Version histories record *what* was done in a data change for a project, but don't tell us *why*. Changelogs are super useful for helping us understand the reasons changes have been made. Changelogs have no set format and you can even make your entries in a blank document. But if you are using a shared changelog, it is best to agree with other data analysts on the format of all your log entries.

Typically, a changelog records:

- Data, file, formula, query, or any other component that changed
- Description of what changed
- Date of the change
- Person who made the change
- Person who approved the change
- Version number
- Reason for the change

Let’s say you made a change to a formula in a spreadsheet because you observed it in another report and you wanted your data to match and be consistent. If you found out later that the report was actually using the wrong formula, an automated version history would help you *undo* the change. But if you also recorded the reason for the change in a changelog, you could go back to the creators of the report and let them know about the incorrect formula. If the change happened a while ago, you might not remember who to follow up with. Fortunately, your changelog would have that information ready for you! By following up, you would ensure data integrity outside your project. You would also be showing personal integrity as someone who can be trusted with data. That is the power of a changelog!

Finally, a changelog is important for when lots of changes to a spreadsheet or query have been made. Imagine an analyst made four changes and the change they want to revert to is change #2. Instead of clicking the undo feature three times to undo change #2 (and losing changes #3 and #4), the analyst can undo just change #2 and keep all the other changes. Now, our example was for just 4 changes, but try to think about how important that changelog would be if there were hundreds of changes to keep track of.

## Bonus tip

If an analyst is making changes to an existing SQL query that is shared across the company, the company most likely uses what is called a **version control system**. An example might be a query that pulls daily revenue to build a dashboard for senior management.

Here's how a version control system affects a change to a query:

1. A company has official versions of important queries in their **version control system**.
2. An analyst makes sure the most up-to-date version of the query is the one they will change. This is called **syncing**
3. The analyst makes a change to the query.
4. The analyst might ask someone to review this change. This is called a **code review** and can be informally or formally done. An informal review could be as simple as asking a senior analyst to take a look at the change.
5. After a reviewer approves the change, the analyst submits the updated version of the query to a repository in the company's version control system. This is called a **code commit**. A best practice is to document exactly what the change was and why it was made in a comments area. Going back to our example of a query that pulls daily revenue, a comment might be: *Updated revenue to include revenue coming from the new product, Calypso*.
6. After the change is **submitted**, everyone else in the company will be able to access and use this new query when they **sync** to the most up-to-date queries stored in the version control system.
7. If the query has a problem or business needs change, the analyst can ***undo*** the change to the query using the version control system. The analyst can look at a chronological list of all changes made to the query and who made each change. Then, after finding their own change, the analyst can **revert** to the previous version.
8. The query is back to what it was before the analyst made the change. And everyone at the company sees this reverted, original query, too.

## **Key takeaways**

Engineers, writers, and data analysts use different methods to keep track of changes they make to their work. Automated version control, changelogs, and version control systems are all common tools used to track changes. Changelogs are particularly useful, as they can be used to record the reasons for changes made to data. This can help to ensure data integrity and consistency. Version control systems are most commonly used when making changes to shared queries. They enable analysts to track any changes made and revert to previous versions if necessary.

---

# Creating a changelog

 

In previous activities, you’ve reviewed the different types of questions to ask before exploring data, the importance of pre-cleaning data, the basic functions of SQL, how to clean data with spreadsheets, and more. As a junior data analyst, most of your projects will consist of these activities. As you have experienced, each of these tasks follows a complicated process. Therefore, consistent and accurate record-keeping is essential to keeping you on track.

A **changelog** is a document used to record the notable changes made to a project over its lifetime across all of its tasks. It is typically curated so that the changes it records are listed chronologically across all versions of the project.

The major benefit to using changelogs is that contributors and users connected with the project get a specific list of what important alterations have been made, when they were made, and sometimes, what version they were released for. It is an invaluable tool for communicating how the project has evolved over time to coworkers, management, and stakeholders.

# **Step 2: Follow best practices for changelogs**

A changelog for a personal project may take any form desired. However, in a professional setting and while collaborating with others, readability is important. These guiding principles help to make a changelog accessible to others:

- Changelogs are for humans, not machines, so write legibly.
- Every version should have its own entry.
- Each change should have its own line.
- Group the same types of changes. For example, *Fixed* should be grouped separately from *Added*.
- Versions should be ordered chronologically starting with the latest.
- The release date of each version should be noted.

All the changes for each category should be grouped together. Types of changes usually fall into one of the following categories:

- Added: new features introduced
- Changed: changes in existing functionality
- Deprecated: features about to be removed
- Removed: features that have been removed
- Fixed: bug fixes
- Security: lowering vulnerabilities

# **Step 3: Examine a sample changelog**

Examine the figure below for an example of a changelog. Note that the following example is written in [Markdown](https://docs.github.com/en/free-pro-team@latest/github/writing-on-github/basic-writing-and-formatting-syntax), as it is common to keep changelogs as a readme file in a code repository.

![Untitled](Document%20the%20cleaning%20process%207a638b44c1c64fa0bc9f2a529d9a0f24/Untitled.png)

# **Step 4: Consider what to record in a changelog**

Now that you're familiar with the example, consider what changes you need to record in a changelog. To start, you record the various changes, additions, and fixes that were discussed above. Arrange them using bullets or numbering with one change per line. Group similar changes together with a label describing the change immediately above them.

Use different version numbers for each milestone reached in your project. Within each version, place the logged changes that were made since the previous version (milestone). Dates are not generally necessary for each change, but they are recommended for each version.

In an upcoming course, you will have the opportunity to complete a capstone project. This will be a great chance to demonstrate your ability to organize a project like a professional data analyst by keeping your own changelog.

You can do this using a simple text file or spreadsheet and include your changelog with the project write-up. It will help you stay organized and collaborate with others. Keep this in mind when you reach the capstone project in an upcoming course, and don’t be afraid to revisit this lesson if you have questions.

---

# Why documentation is important

- **Data cleaning is like a crime drama:** We've gathered the evidence (dirty data), cleaned it, verified it, and cleaned it again. Now it's time to present our findings.
- **Documentation is crucial:** Track every step of the data cleaning process, including changes, additions, deletions, and errors. This will save you time and build credibility.
- **Changlogs provide a real-time account of modifications:** They are essential for stakeholders who can't directly view your work.
- **Present your findings clearly and concisely:** Explain what you did, how you did it, and the impact of your work.
- **Be transparent about your process:** This builds trust and shows that you are accountable.

**Definitions:**

- **Data cleaning:** The process of identifying and correcting errors in data.
- **Verification:** The process of confirming that data is accurate and complete.
- **Documentation:** The process of tracking changes, additions, deletions, and errors in data.
- **Changelog:** A record of all changes made to data.
- **Stakeholders:** Individuals or groups who have an interest in the outcome of a project.

**Example:**

In the video, we saw an example of how to document the process of removing a duplicate membership record from a database. The documentation included the following information:

- The date and time the change was made.
- The name of the person who made the change.
- The reason for the change.
- The impact of the change.

---

# Feedback and cleaning

**Key Points:**

- **Importance of Verification and Reporting:**
    - Provides proof to stakeholders that data is accurate and reliable.
    - Demonstrates well-executed and documented data cleaning efforts.
    - Enables feedback and improvement of data collection processes.
- **Benefits of Clean Data:**
    - Supports accurate insights and decision-making.
    - Reduces errors and inefficiencies in data collection.
    - Increases business value and bottom line.
- **Data Cleaning Insights:**
    - Reveals the nature and severity of error-generating processes.
    - Identifies patterns in data collection and entry procedures.
    - Informs improvements to data collection and quality control.
- **Reporting and Feedback:**
    - Schedule meetings with data engineers or data owners to ensure proper data intake.
    - Use feedback to address errors and improve data collection processes.
    - Communicate cleaning results and insights to stakeholders.

**Definitions:**

- **Verification:** The process of confirming that data is accurate and reliable.
- **Reporting:** The process of documenting and communicating data cleaning results and insights.
- **Stakeholders:** Individuals or groups who have an interest in the data and its use.
- **Data Engineer:** A professional responsible for designing and building data pipelines and infrastructure.
- **Data Owner:** A person responsible for the quality and integrity of a specific dataset.
- **Quality Control:** The process of ensuring that data meets the required standards for accuracy, completeness, and consistency.

**Additional Notes:**

- The video emphasizes the importance of using data cleaning insights to improve data collection processes and ultimately business development.
- Consistent documentation and reporting are crucial for identifying error patterns and implementing effective solutions.
- By addressing errors and inefficiencies, companies can increase the value and reliability of their data, leading to better decision-making and improved outcomes.

---