# Data-driven storytelling

---

# Stories stories with data

**Storytelling as the Oldest Form of Teaching:**

- Humans have used storytelling to share knowledge for tens of thousands of years, dating back to cave paintings.
- Storytelling is a natural form of education because it helps us process and remember information more effectively.
- Our brains are wired to organize events with a beginning, middle, and end, making stories a relatable and engaging way to learn.
- Stories help us connect with others and build relationships.

**The Evolution of Storytelling:**

- Inventions like the printing press, motion picture camera, and data visualization tools have revolutionized how we tell stories.
- Data visualization transforms data into meaningful stories that people can connect with and understand.

**Data Visualization and Storytelling:**

- Data visualization tools help us create dashboards, which organize information from multiple sources for easy analysis and visualization.
- Dashboard filters allow us to focus on specific data by hiding irrelevant information.
- By using these tools, we can tell data-driven stories that motivate and persuade people to take action.

**Key Takeaways:**

- Storytelling is a powerful tool for teaching and learning.
- Data visualization helps us transform data into compelling stories.
- Dashboards and filters are valuable tools for data analysis and storytelling.

**Definitions:**

- **Data visualization:** The representation and presentation of data to aid understanding.
- **Dashboard:** A tool that organizes information from multiple sources into one central location for tracking, analysis, and visualization.
- **Dashboard filter:** A tool for showing only the data that meets specific criteria while hiding the rest.

---

# Bring ideas to life

[index (50).mp4](Data-driven%20storytelling%2035d6c2d9b9234080901868a50fe4bb4f/index_(50).mp4)

**Key Points:**

- **Data storytelling:** Communicating the meaning of a data set with visuals and a narrative customized for a specific audience.
- **Benefits of data storytelling:**
    - Makes a lasting impression on the audience.
    - Convinces people to take action.
    - Builds customer loyalty.
    - Makes data more engaging and interesting.
- **Three steps of data storytelling:**
    1. **Engage your audience:** Capture and hold their interest and attention.
    2. **Create compelling visuals:** Show the story of your data, not just tell it.
    3. **Tell the story in an interesting narrative:** Organize and concisely connect the data to the project objective and highlight key insights.

**Examples:**

- **Music streaming company:** Year-in-review email highlighting songs listened to and congratulating top fans.
- **Ride-sharing company:** Data visualization showing miles traveled, reduced gas spending, carbon emissions, and time saved.
- **Cosmetic company:** Pie chart illustrating profitability of different stores.

**Additional Notes:**

- The video emphasizes the importance of understanding your audience and tailoring your data story accordingly.
- It highlights the power of visuals in engaging the audience and making data more accessible.
- The video concludes by introducing the concept of word clouds as a simple visualization tool for highlighting key topics in text data.

**Definitions:**

- **Narrative:** A story with a beginning, middle, and end.
- **Visuals:** Images, charts, graphs, and other visual representations of data.
- **Word cloud:** A visualization of text data where words are presented in different sizes based on their frequency.

---

# Effective data stories

# Effective data stories

In data analytics, **data storytelling** is communicating the meaning of a dataset with visuals and a narrative that is customized for a particular audience. In data journalism, journalists engage their audience of readers by combining visualizations, narrative, and context into data-driven articles. It turns out that data analysts and data journalists have a lot in common! As a junior data analyst, you might learn a few things about effective storytelling from data journalism. Read further to explore the role and work of a data journalist in telling a good story.

**Note:** This reading refers to an article published in *The New Yorker*. Non-subscribers may access several free articles each month. If you already reached your monthly limit on free articles, bookmark the article and come back to this reading later.

## Take a tour of a data-driven article

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/5c3ub0SwTumN7m9EsL7peQ_20854051effb4411a8d99606f9bdc037_Screen-Shot-2021-02-26-at-5.09.46-PM.png?expiry=1717027200000&hmac=nYShz0tcZsN4iT-oGQaV75_cIrVix6eqU9bz4WGS6W4)

[Ben Wellington](https://www.newyorker.com/contributors/ben-wellington), a contributing writer for *The New Yorker* and a professor at the Pratt Institute, used New York City’s [open data portal](https://nycopendata.socrata.com/Social-Services/311-Service-Requests-from-2010-to-Present/erm2-nwe9?) to track down noise complaints from logged service requests. He analyzed the data to gain a more quantitative understanding of where the noise was coming from and which neighborhoods were the noisiest. Then, he presented his findings in the [Mapping New York's Noisiest Neighborhoods](https://www.newyorker.com/tech/annals-of-technology/mapping-new-york-noise-complaints) article.

First, click the link above to skim the article  and familiarize yourself with the data visualizations. Then, join the bus tour of the data! You will be directed to three visualizations (tour stops) to observe how each visualization helped strengthen the overall storytelling in the article.

### **Tour stop 1: setting context**

Earlier in the training, you learned how context is important to understand data. **Context** is the condition in which something exists or happens. Based on the categorization of noise complaints, the data journalist set the context in the article by defining what people considered to be noise.

In the article, review the [combo table and bar chart](https://media.newyorker.com/photos/590965cfebe912338a3758c4/master/w_1600%2Cc_limit/Wellington-noise-ComplaintCounts.jpg) that categorizes the noise complaints. Evaluate the visualization:

- **How does the visualization help set the context?**
The combo table and bar chart is effective in summarizing the noise categories as percentages of the logged complaints. This helps set the context by answering the question, “what is noise?” Notice that the data journalist created a combo table and bar chart instead of a pie chart. With 11 noise categories, a list with a bar chart showing relative proportions is an elegant representation. A pie chart with 11 slices would have been harder to read.
- **How does the visualization help clarify the data?**
If you add the percentages in the categories in the combo table and bar chart, the total is ninety-eight percent. There is a difference of two percent that can’t be accounted for in the visualization. So, rather than clarifying the data, the visualization actually causes a little confusion. One lesson is to always make sure that your percentages add up correctly. Sometimes rounding decimal places up or down causes percentages to be off so they don’t add up to 100%.
- **Do you notice a data visualization best practice?** 
You learned that a companion table in Tableau shows data in a different way in case some in your audience prefer tables. It appears that the data journalist had the same idea by using a combo table and bar chart.
**Note:** As a refresher, a companion table in Tableau is displayed right next to a visualization. A companion table displays the same data as the visualization, but in a table format. You may replay the [Getting Creative](https://www.coursera.org/learn/visualize-data/lecture/Eytgs/getting-creative) video which includes an example of a companion table.

### **Tour stop 2: analyzing variables**

After setting the context by identifying the noise categories, the data journalist describes his analysis of the noise data. One interesting analysis is the distribution of noise complaints versus the time of day.

In the article, review the [stacked area chart](https://media.newyorker.com/photos/590965cd1c7a8e33fb38d4ac/master/w_1600%2Cc_limit/Wellington-noise-ComplaintsHours.jpg) for the distribution of noise complaints by hour of the day. Evaluate the visualization:

- **How does the visualization perform against the five-second rule?**
Recall that the five-second rule states that you should understand what is being conveyed within the first five seconds of seeing a chart. We are guessing that this visualization performs quite well! The area charts for loud music and barking dogs help the audience understand that more of these types of noise complaints were made during late night and early morning hours (between 10:00 PM and 2:00 AM). Notice also that the color coding in the legend aligns with the colors in the chart. A chart legend normally has the largest category at the top, but the data journalist chose to order the legend so the largest category, “Loud music or party” appears at the bottom instead. How much time do you think this alignment saved readers?
- **How does the visualization help clarify the data?** 
Unlike the visualization from the previous tour stop, this visualization does a better job of clearly showing that all percentages add up to 100%.
- **Do you notice a data visualization best practice?** 
As a best practice, both the x-axis and y-axis should be labeled. But, the data journalist chose to include % or A.M. and P.M. with each tick on an axis. As a result, labeling the x-axis “Time of Day'' and the y-axis “Percentage of Noise Complaints” isn’t required. This demonstrates that a little creativity with labeling can help you achieve a cleaner chart.

### **Tour stop 3: drawing conclusions**

After describing how the data was analyzed, the data journalist shares which neighborhoods are the noisiest using a variety of visualizations: [combo table and bar chart](https://media.newyorker.com/photos/590965ceebe912338a3758c2/master/w_1600%2Cc_limit/Wellington-noise-ComplaintsNeighborhoods.jpg), [density map](https://media.newyorker.com/photos/590965cfc14b3c606c1067b0/master/w_1600%2Cc_limit/Wellington-noise-complete.jpg), and [neighborhood map](https://media.newyorker.com/photos/590965d0ebe912338a3758c8/master/w_1600%2Cc_limit/Wellington-noise-WilliamsburgDetail.jpg).

In the article, review the [neighborhood map](https://media.newyorker.com/photos/590965d0ebe912338a3758c8/master/w_1600%2Cc_limit/Wellington-noise-WilliamsburgDetail.jpg) for how close a noisy neighborhood is to a quiet neighborhood. Evaluate the visualization:

- **How does the visualization help make a point?**
The data journalist observed that one of the noisiest neighborhoods was right next to one of the quietest neighborhoods. The neighborhood map is effective in emphasizing this observation as a dark blue area versus a white area.
- **How does the visualization help clarify the data?** 
The visualization classifies the data by neighborhood and allows the audience to follow along when the journalist focuses specifically on the Williamsburg, East Williamsburg, and North Side/South Side neighborhoods.
- **Do you notice a data visualization best practice?** 
Each neighborhood is directly labeled so a legend isn’t necessary.

## End of the tour: being inspired

We hope you enjoyed your tour of a data journalist’s work! May this inspire your data storytelling to be as engaging as possible. For additional information about effective data storytelling, read these articles:

- [What is Data Storytelling?](https://www.nugit.co/what-is-data-storytelling/)
- [The Art of Storytelling in Analytics and Data Science | How to Create Data Stories?](https://www.analyticsvidhya.com/blog/2020/05/art-storytelling-analytics-data-science/)
- [Use Data and Analytics to Tell a Story](https://www.gartner.com/smarterwithgartner/use-data-and-analytics-to-tell-a-story/)
- [Tell a Meaningful Story With Data](https://www.thinkwithgoogle.com/marketing-resources/data-measurement/tell-meaningful-stories-with-data/)

---

# Speak to your audience

**Key Points:**

- **Know your audience:** Consider their role, stake in the project, and desired outcomes from the data insights.
- **Choose a clear and direct primary message:** This message should be the central focus of your story.
- **Use spotlighting to identify key insights:** This technique involves scanning data to identify the most important information.
- **Explore the meaning behind the numbers:** Look for patterns, trends, and connections within the data.
- **Keep your message concise and clear:** Avoid overwhelming your audience with excessive information.

**Definitions:**

- **Stakeholder:** An individual or group with an interest in the project's outcome.
- **Spotlighting:** A technique for identifying key insights by scanning data and highlighting important information.
- **Primary message:** The central point of your data story that you want your audience to remember.

**Additional Notes:**

- The video emphasizes the importance of understanding your audience's perspective and tailoring your message accordingly.
- It provides a framework for identifying key insights and crafting a clear and concise message.
- The video acknowledges that audience reactions may vary, but following these steps increases the likelihood of positive outcomes.

---