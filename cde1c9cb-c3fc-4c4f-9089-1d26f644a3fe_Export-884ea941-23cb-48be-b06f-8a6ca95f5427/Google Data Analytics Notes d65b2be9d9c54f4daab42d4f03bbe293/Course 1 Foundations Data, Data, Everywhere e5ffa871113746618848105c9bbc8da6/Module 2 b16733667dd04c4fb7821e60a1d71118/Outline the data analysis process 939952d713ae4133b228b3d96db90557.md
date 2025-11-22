# Outline the data analysis process

---

# The phases of data analysis and this program

- Now that you understand all the phases of the data life cycle, it’s time to move on to the phases of **data analysis**. They sound similar, but are two different things. Data analysis isn’t a life cycle. It is the process of analyzing data.

- Let's start with the first step in data analysis, the ask phase. In this phase, we do two things. We define the problem to be solved and we make sure that we fully understand stakeholder expectations. Stakeholders hold a stake in the project. They are people who have invested time and resources into a project and are interested in the outcome.
    - First, defining a problem means you look at the current state and identify how it's different from the ideal state. Usually there's an obstacle we need to get rid of or something wrong that needs to be fixed. For instance, a sports arena might want to reduce the time fans spend waiting in the ticket line. The obstacle is figuring out how to get the customers to their seats more quickly.
    - Another important part of the ask phase is understanding stakeholder expectations. The first step here is to determine who the stakeholders are. That may include your manager, an executive sponsor, or your sales partners. There can be lots of stakeholders. But what they all have in common is that they help make decisions, influence actions and strategies, and have specific goals they want to meet. They also care about the project and that's why it's so important to understand their expectations. For instance, if your manager assigns you a data analysis project related to business risk, it would be smart to confirm whether they want to include all types of risks that could affect the company, or just risks related to weather such as hurricanes and tornadoes.
- Communicating with your stakeholders is key in making sure you stay engaged and on track throughout the project. So as a data analyst, developing strong communication strategies is very important. This part of the ask phase helps you keep focused on the problem itself, not just its symptoms. As you learned earlier, the five whys are extremely helpful here. In an upcoming course, you'll learn how to ask effective questions and define the problem by working with stakeholders. You'll also cover strategies that can help you share what you discover in a way that keeps people interested.

- After that, we'll move on to the prepare step of the data analysis process. This is where data analysts collect and store data they'll use for the upcoming analysis process.
    - You'll learn more about the different types of data and how to identify which kinds of data are most useful for solving a particular problem.
    - You'll also discover why it's so important that your data and results are objective and unbiased. In other words, any decisions made from your analysis should always be based on facts and be fair and impartial. Next is the process step.
    - Here, data analysts find and eliminate any errors and inaccuracies that can get in the way of results. This usually means cleaning data, transforming it into a more useful format, combining two or more datasets to make information more complete and removing outliers, which are any data points that could skew the information.
    - After that, you'll learn how to check the data you prepare to make sure it's complete and correct. This phase is all about getting the details right. So you'll also fix typos, inconsistencies, or missing and inaccurate data.
    - To top it off, you'll gain strategies for verifying and sharing your data cleansing with stakeholders.
- Then it's time to analyze. Analyzing the data you've collected involves using tools to transform and organize that information so that you can draw useful conclusions, make predictions, and drive informed decision-making.
    - There are lots of powerful tools data analysts use in their work and in this course you'll learn about two of them, spreadsheets and structured query language, or SQL
- The next course is based on the share phase. Here you'll learn how data analysts interpret results and share them with others to help stakeholders make effective data-driven decisions.
    - In the share phase, visualization is a data analyst's best friend. So this course will highlight why visualization is essential to getting others to understand what your data is telling you.
    - With the right visuals, facts and figures become so much easier to see and complex concepts become easier to understand. We'll explore different kinds of visuals and some great data visualization tools. You'll also practice your own presentation skills by creating compelling slideshows and learning how to be fully prepared to answer questions.
    - Then we'll take a break from the data analysis process to show you all of the really cool things you can do with the programming language R. You don't need to be familiar with R or programming languages in general. Just know that R is a popular tool for data manipulation, calculation, and visualization.
- For our final data analysis phase, we have act. This is the exciting moment when the business takes all of the insights you, the data analyst, have provided and puts them to work in order to solve the original business problem and will be acting on what you've learned throughout this program.

---

# Example of the data analysis process

- Regardless of what type of data analysis you're conducting, the process is generally the same.
- The example that I'll walk through is that of our employee engagement survey, but you could imagine that this process applies to just about any data analysis that you're going to conduct as an analyst.
    - The first thing you want to do is ask. You want to ask all of the right questions at the beginning of the engagement so that you better understand what your leaders and stakeholders need from this analysis.
        - The types of questions that I generally ask are around, what is the problem that we're trying to solve?
        - What is the purpose of this analysis?
        - What are we hoping to learn from it?
    - After you've asked all the right questions and you've wrapped your arms around the scope of the analysis you need to conduct, the next step is to prepare.
        - We need to be thinking about what type of data we need to answer those key questions.
        - This could be anything from quantitative data or qualitative data.
        - It could be cross-sectional or points in time versus longitudinal over a long period of time.
        - We need to be thinking about the type of data we need in order to answer the questions that we've set out to answer based on what we learned when we asked the right questions.
        - We also need to be thinking about how we're going to collect that data or if we need to collect that data. It may be the case that we need to collect this data brand-new.
        - So we need to think about what type of data we're going to be collecting and how. F
        - For our employee engagement survey, we do that via survey of both quantitative and qualitative questions.
        - But it may actually be the case that for many analyses, the data that you're looking for already exists. Then it's a question of working with those data owners to make sure that you are able to leverage that data and use it responsibly.
    - After you've done all the hard work to collect your data, now you need to process that data. It begins with cleaning. We can think of it as the initial introduction or the handshake, hello, to your data.
        - This is where you get a chance to understand its structure, its quirks, its nuances, and you really get a chance to understand deeply what type of data you're going to be working with and understanding what potential that data has to answer all of your questions.
        - This is such an important part, too, where we're running through all of our quality assurance checks.
        - For example, do we have all of the data that we anticipated we would have? Are we missing data at random or is it missing in a systematic way such that maybe something went wrong with our data collection effort? If needed, did we code all of our data the right way? Are there any outliers that we need to treat differently?
        - This is the part where we spend a lot of time really digging deeply into the structure and nuance of the data to make sure that you're able to analyze it appropriately and responsibly.
    - After cleaning our data and running all of our quality assurance checks, now is the point where we analyze our data, making sure to do so in as objective and unbiased a way as possible.
        - To do this, the first thing we do is run through a series of analyses that we've already planned ahead of time based on the questions that we know we want to answer from the very, very beginning of the process.
        - One thing that's probably the hardest about this particular process, the hardest thing about analyzing data, is that we as analysts are trained to look for patterns.
        - Over time as we become better and better at our jobs, what we'll often find is that we can start to intuit what we might see in the data. We might have a sneaking suspicion as to what the data are going to tell us.
        - This is the point where we have to take a step back and let the data speak for itself. As data analysts, we are storytellers, but we also have to keep in mind that it is not our story to tell. That story belongs to the data, and it is our job as analysts to amplify and tell that story in as unbiased and objective a way as possible.
    - The next step is to share all of the data and insights that you've generated from your analyses.
        - Now typically for employee engagement survey, we start by sharing the high-level findings with our executive team. We want them to have a landscape view of how the organization is feeling, and we want to make sure that there aren't any surprises as they dig deeper and deeper into the data to understand how teams are feeling and how individual employees are feeling.
        - All of this work from asking the right questions to collecting your data, to analyzing and sharing, doesn't mean much of anything if we aren't taking action on what we've just learned.
        - This to me is the most critical part, especially of our employee engagement survey. I like to say that the survey is actually the easy part, and acting on the results is really where the real work begins.
        - This is where we use all of those data-driven insights to decide what types of interventions we want to introduce, not only at the organizational level, but also at the team level as well.
        - We might find, for example, that the organization is working on a series of interventions to help improve part of the employee experience, whereas individual teams have additional roles, responsibilities to play, to either bolster some of those efforts or to introduce new ones to better meet their team where their strengths and opportunity areas are.
- The data analysis process is rigorous, but it is lengthy. I can completely appreciate that we as data analysts, get so excited about just diving right into the data and doing what we do best.
- The challenge is that if we don't work through the process in its entirety, if we try to skip steps, we're not going to be able to elicit the insights that we're looking for.

---