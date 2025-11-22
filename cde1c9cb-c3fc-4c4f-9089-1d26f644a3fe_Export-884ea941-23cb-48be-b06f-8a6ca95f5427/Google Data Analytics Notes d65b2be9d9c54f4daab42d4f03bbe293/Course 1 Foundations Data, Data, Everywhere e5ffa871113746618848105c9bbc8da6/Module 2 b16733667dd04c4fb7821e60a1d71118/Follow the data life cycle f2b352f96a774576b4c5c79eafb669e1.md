# Follow the data life cycle

---

# Learn about data phases and tools

- How do data analysts bring data to life?
    - It starts with the right data analysis tool. These include spreadsheets, databases, query languages, and visualization software.

---

# Stages of the data life cycle

- The life cycle of data plan is:
    
    ```mermaid
    graph TD
      Plan --> Capture --> Manage --> Analyze --> Archive --> Destroy
    ```
    

## Planning

- This actually happens well before starting an analysis project.
- During planning, a business decides what kind of data it needs, how it will be managed throughout its life cycle, who will be responsible for it, and the ptimal outcomes.
    - For example, let’s say an electricity provider wanted to gain insights into how to save people energy. In the planning phase, they might decide to capture information on how much electricity its customers use each year, what types of buildings are being powered, and what types of devices are being powered inside of them. The electrical company would also decide which team members will be responsible for collecting, storing, and sharing that data.
    - All of this happens during planning, and it helps set up the rest of the project.

## Capture data

- This is where the data is collected from a variety of different sources and brought into the organization.
- With so much data being created everyday, the ways to collect it are truly endless.
- One common method is getting data from outside resources.
    - For example, if yn ou were doing data analysis on weather patterns, you’d probably get data from a publicly available dataset like the National Climatic Data Center.
- Another way to get data is from a company’s own documents and files, which are usually stored inside a database.

> A **database** is a collection of data stored in a computer system.
> 
- In the case of our electricity provider, the business would probably measure data usage among its customers within a database that it owns.
- As a quick note, when you maintain a database of customer information, ensuring data integrity, credibility, and privacy are all important concerns.

## Manage

- How we care for our data, how and where it’s stored, the tools used to keep it safe and secure, and the actions taken to make sure that it’s maintained properly.
- This phase is very important to data cleansing.

## Analyze

- In this phase, the data is used to solve problems, make great decisions, and support business goals.
    - For example, one of our electricity company’s goals might be to find ways to help customers save energy.

## Archiving

> Archiving means storing the data in a place where it is still available, but may not be used again.
> 
- During analysis, analysts handle huge amounts of data. Can you imagine if we had to sort through all off the available data that’s out there, even if it was no longer useful and relevant to our work? It makes more sense to archive it than to keep it around.

## Destroy

- So let's get back to our electricity provider example. They would have data stored on multiple hard drives. To destroy it, the company would use a secure data erasure software. If there were any paper files, they would be shredded too. This is important for protecting a company's private information, as well as private data about its customers.

---

# Variations of the data life cycle

## Recap

1. **Plan:** Decide what kind of data is needed, how it will be managed, and who will be responsible for it.
2. **Capture:** Collect or bring in data from a variety of different sources.
3. **Manage:** Care for and maintain the data. This includes determining how and where it is stored and the tools used to do so.
4. **Analyze:** Use the data to solve problems, make decisions, and support business goals.
5. **Archive:** Keep relevant data stored for long-term and future reference.
6. **Destroy:** Remove data from storage and delete any shared copies of the data.

### Important

**Note:** Be careful not to confuse the six stages of the data life cycle (plan, capture, manage, analyze, archive, and destroy) with the six phases of the data analysis process (ask, prepare, process, analyze, share, and act). They are not interchangeable.

## Examples of variations by different companies

- The data life cycle provides a generic or common framework for how data is managed.
- The rest of this reading provides a glimpse of how government, finance, and education institutions can view data life cycles a little differently.

### US Fish and Wildlife Service

- The US Fish and Wildlife Service uses the following data life cycle
1. Plan 
2. Acquire 
3. Maintain 
4. Access 
5. Evaluate 
6. Archive 

### The U.S. Geological Survey (USGS)

1. Plan 
2. Acquire 
3. Process
4. Analyze
5. Preserve 
6. Publish/Share   
- Several cross-cutting or overarching activities are also performed during each stage of their life cycle:
    - Describe (metadata and documentation)
    - Manage quality
    - Backup and secure

### Financial Institutions

- Financial institutions may take a slightly different approach to the data life cycle
1. Capture
2. Qualify
3. Transform
4. Utilize
5. Report
6. Archive
7. Purge

### Harvard Business School (HBS)

- One final data life cycle informed by Harvard University research has eight stages.
1. Generation
2. Collection
3. Processing
4. Storage
5. Management
6. Analysis
7. Visualization
8. Interpretation

## Key Takeaways

- Understanding the importance of the data life cycle will set you up for success as a data analyst. Individual stages in the data life cycle will vary from company to company or by industry or sector.
- Historical data is important to both the U.S. Fish and Wildlife Service and the USGS, so their data life cycle focuses on archiving and backing up data.
- Harvard's interests are in research and teaching, so its data life cycle includes visualization and interpretation even though these are more often associated with a data analysis life cycle. The HBS data life cycle also doesn't call out a stage for purging or destroying data.
- In contrast, the data life cycle for finance clearly identifies archive and purge stages.
- To sum it up, although data life cycles vary, one data management principle is universal: Govern how data is handled so that it is accurate, secure, and available to meet your organization's needs.