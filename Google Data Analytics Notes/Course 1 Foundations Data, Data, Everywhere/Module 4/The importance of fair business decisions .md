# The importance of fair business decisions

---

# The power of data in business

> An issue is a topic or subject to investigate.
> 

> A question is designed to discover information and a problem is an obstacle or complication that needs to be worked out.
> 
- Coca-Cola had a question about new products. Data analysis gave them insights into new flavors customers already like.
- The City Zoo and Aquarium had a problem with staffing. Data, helped them figure out the best staffing strategy.
- These questions and problems become the foundation for all kinds of business tasks, that you'll help solve as a data analyst.
- A business task is the question or problem data analysis answers for business.
    - This is where you focus a lot of your efforts in the work you'll do for future employers.
    - Let's stick with our zoo example and see if we can imagine what a business task for a zoo might look like. We know the problem, unpredictable weather was making it hard for the zoo to anticipate staffing needs.
    - Maybe the business task could be something like, analyze weather data from the last decade to identify predictable patterns.
    - The data analysts could then plan out the best way to gather, analyze, and present the data needed to solve this task and meet the zoos goals.
    - Then, using data, the zoo would be able to make informed decisions about their daily staffing.
- The simplest way to think about decision-making is that it's a choice between consequences, good, bad, or a combination of both.
    - In our zoo example, the zoo had the data they needed to make an informed decision that solved their problem. But what if they had made this decision without data? Let's say they just relied on observation and memory to track the weather and make staffing schedules.
    - Well, we already know that wouldn't have solve their problem long-term. Data analytics gave them the information they needed to find the best possible solution to their problem. That's the power of data.
- Observation and intuition are powerful tools in decision-making, but they can only take us so far when we make decisions based on just observation and gut feelings, we're only seeing part of the picture.
- Data helps us see the whole thing.
- With data, we have a complete picture of the problem and its causes, which lets us find new and surprising solutions we never would've been able to see before.
- Data analytics helps businesses make better decisions. It all starts with a business task and the question it's trying to answer.

---

# Understand data and fairness

- Data analysts have another important responsibility: making sure that their analyses are fair.
- Now, I know what you're probably thinking, data is based on collected facts, how can it be unfair? Well, that's a good question.
- Let's learn what fairness means when we talk about data analysis and why it's important for you as an analyst to keep in mind.

> Fairness means ensuring that your analysis doesn't create or reinforce bias. In other words, as a data analyst, you want to help create systems that are fair and inclusive to everyone.
> 
- Sounds simple enough? Well, here's the tough part about fairness in data analytics. There isn't one standard definition of it, but hopefully the way we've just described it can give you one way to think about fairness for right now, but it's about to get a bit trickier.
- Sometimes conclusions based on data can be true and unfair.
- What can you do then?
    - Well, let's find out with an example.
    - Let's say we have a company that's kind of notorious for being a boys club. There isn't much representation of other genders.
    - This company wants to see which employees are doing well, so they start gathering data on employee performance and their own company culture.
    - The data shows that men are the only people succeeding at this company. Their conclusion? That they should hire more men.
    - After all, they're doing really well here, right? But that's not a fair conclusion for a couple of reasons.
        - First, it doesn't even consider all of the available data on company culture, so it paints an incomplete picture.
        - Second, it doesn't think about the other surrounding factors that impact the data, or in other words, the conclusion doesn't consider the difficulties that people of different gender identities have trying to navigate a toxic work environment.
        - If the company only looks at this conclusion, they won't acknowledge and address how harmful their culture is and they won't understand why certain people are set up to fail within it.
        - That's why it's important to keep fairness in mind when analyzing data. The conclusion that only men are succeeding at this company is true, but it ignores other systematic factors that are contributing to this problem.
        - But don't worry, there's a way to make a fair conclusion here. An ethical data analyst can look at the data gathered and conclude that the company culture is preventing some employees from succeeding, and the company needs to address those problems to boost performance.
        - See how this conclusion paints a much more complete and fair picture. It recognizes the fact that some people aren't doing as well in this company and factors in why that could be instead of discriminating against a huge number of applicants in the future.
- As a data analyst it's your responsibility to make sure your analysis is fair and factors in the complicated social context that could create bias in your conclusions.
- It's important to think about fairness from the moment you start collecting data for a business task to the time you present your conclusions to your stakeholders.
- For now, let's check out an example of a data analysis that does a good job of considering fairness in its conclusion.
    - A team of Harvard data scientists were developing a mobile platform to track patients at risk of cardiovascular disease in an area of the United States called the Stroke Belt.
    - It's important to call out that there were a variety of reasons people living in this area might be more at risk. With that in mind, these data scientists recognized that fairness needed to be a priority for this project, so they built fairness into their models.
    - The team took several fairness measures to make sure they were being as fair as possible when examining sensitive and potentially biased data.
        - First, they teamed analysts with social scientists who could provide insights on human bias and the social context that created them.
        - They also collected self reported data in a separate system to avoid the potential for racial bias, which might skew the results of their study and unfairly represent patients.
        - To make sure this sample population was representative, they oversampled non-dominant groups to ensure the model was including them.
        - It's clear that the team made fairness a top priority every step of the way. This helped them collect data and create conclusions that didn't negatively impact the communities they were studying.

---

# Consider fairness

- Previously, you learned that part of a data professional’s responsibility is to make certain that their analysis is fair. **Fairness** means ensuring your analysis doesn't create or reinforce bias. This can be challenging, but if the analysis is not objective, the conclusions can be misleading and even harmful. In this reading, you’re going to explore some best practices you can use to guide your work toward a more fair analysis!

- Following are some strategies that support fair analysis:

| **Best practice** | **Explanation** | **Example** |
| --- | --- | --- |
| Consider all of the available data | Part of your job as a data analyst is to determine what data is going to be useful for your analysis. Often there will be data that isn’t relevant to what you’re focusing on or doesn’t seem to align with your expectations. But you can’t just ignore it; it’s critical to consider all of the available data so that your analysis reflects the truth and not just your own expectations. | A state’s Department of Transportation is interested in measuring traffic patterns on holidays. At first, they only include metrics related to traffic volumes and the fact that the days are holidays. But the data team realizes they failed to consider how weather on these holidays might also affect traffic volumes. Considering this additional data helps them gain more complete insights. |
| Identify surrounding factors | As you’ll learn throughout these courses, context is key for you and your stakeholders to understand the final conclusions of any analysis. Similar to considering all of the data, you also must understand surrounding factors that could influence the insights you’re gaining. | A human resources department wants to better plan for employee vacation time in order to anticipate staffing needs. HR uses a list of national bank holidays as a key part of the data-gathering process. But they fail to consider important holidays that aren’t on the bank calendar, which introduces bias against employees who celebrate them. It also gives HR less useful results because bank holidays may not necessarily apply to their actual employee population. |
| Include self-reported data | **Self-reporting** is a data collection technique where participants provide information about themselves. Self-reported data can be a great way to introduce fairness in your data collection process. People bring conscious and unconscious bias to their observations about the world, including about other people. Using self-reporting methods to collect data can help avoid these observer biases. Additionally, separating self-reported data from other data you collect provides important context to your conclusions! | A data analyst is working on a project for a brick-and-mortar retailer. Their goal is to learn more about their customer base. This data analyst knows they need to consider fairness when they collect data; they decide to create a survey so that customers can self-report information about themselves. By doing that, they avoid bias that might be introduced with other demographic data collection methods. For example, if they had sales associates report their observations about customers, they might introduce any unconscious bias the employees had to the data. |
| Use oversampling effectively | When collecting data about a population, it’s important to be aware of the actual makeup of that population. Sometimes, oversampling can help you represent groups in that population that otherwise wouldn’t be represented fairly. **Oversampling** is the process of increasing the sample size of nondominant groups in a population. This can help you better represent them and address imbalanced datasets. | A fitness company is releasing new digital content for users of their equipment. They are interested in designing content that appeals to different users, knowing that different people may interact with their equipment in different ways. For example, part of their user-base is age 70 or older. In order to represent these users, they oversample them in their data. That way, decisions they make about their fitness content will be more inclusive. |
| Think about fairness from beginning to end | To ensure that your analysis and final conclusions are fair, be sure to consider fairness from the earliest stages of a project to when you act on the data insights. This means that data collection, cleaning, processing, and analysis are all performed with fairness in mind. | A data team kicks off a project by including fairness measures in their data-collection process. These measures include oversampling their population and using self-reported data. However, they fail to inform stakeholders about these measures during the presentation. As a result, stakeholders leave with skewed understandings of the data. Learning from this experience, they add key information about fairness considerations to future stakeholder presentations. |

## Key takeaways

- As a data professional, you will need to ensure you always consider fairness. This will allow you to avoid creating or reinforcing bias or accidentally drawing misleading conclusions. Using these best practices can help guide your analysis and make you a better data professional!

---

# Fair and ethical data decisions

- When we talk about data ethics, we think about what is the good and right way of using data?
- What are going to be ways that uses of data are going to be beneficial to people?
- When it comes to data ethics, it's not just about minimizing harm but it's actually this concept of beneficence.
- How do we actually improve the lives of people by using data?
- When we think about data ethics we're thinking about, who's collecting the data? Why are they collecting it? How are they collecting it and for what purpose?
    - Because of the way that organizations have imperatives to make money or to report to somebody or provide some analysis, we also have to keep strongly in mind how this is actually going to benefit people at the end of the day. Are the people represented in this data going to be benefited by this?