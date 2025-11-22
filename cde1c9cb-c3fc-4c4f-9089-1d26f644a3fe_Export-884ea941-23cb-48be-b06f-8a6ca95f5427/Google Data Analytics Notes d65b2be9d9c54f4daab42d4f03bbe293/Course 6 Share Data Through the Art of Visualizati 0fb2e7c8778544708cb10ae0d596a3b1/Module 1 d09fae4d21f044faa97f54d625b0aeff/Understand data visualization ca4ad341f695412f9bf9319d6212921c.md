# Understand data visualization

---

# Why data visualization matters

[index (37).mp4](Understand%20data%20visualization%20ca4ad341f695412f9bf9319d6212921c/index_(37).mp4)

**Key Points:**

- **Data visualization:** The graphic representation and presentation of data. It makes information easier to understand by putting it into an image.
- **History of data visualization:** Began with maps, which are the visual representation of geographic data. Evolved with the development of new technologies and the increasing amount of data available.
- **Importance of data visualization:** Helps analysts understand and draw conclusions about data, and communicate those conclusions to others.
- **Key elements of a data visualization:**
    - **Information/Data:** The raw data being visualized.
    - **Story/Concept:** The meaning and context of the data.
    - **Goal/Function:** The purpose of the visualization.
    - **Visual Form:** The way the data is presented visually.
- **Creating effective data visualizations:**
    - **Structure and organize your thoughts:** Identify the key elements of your findings and how they fit together.
    - **Combine all four key elements:** Information, story, goal, and visual form.
    - **Consider your audience:** Make sure your visualization is clear, easy to follow, and tells a compelling story.

**Definitions:**

- **Data visualization:** The graphic representation and presentation of data.
- **Map:** A visual representation of geographic data.
- **Bar graph:** A chart that uses bars to represent data.
- **Data analysis:** The process of examining and interpreting data to draw conclusions.
- **Data storytelling:** The art of using data to tell a compelling story.

---

# Effective data visualizations

It can be difficult to understand data insights by examining individual data points or a table of information. Often, insights become more obvious when presented in an effective visual format. You can use data visualization (often called  “data viz”) techniques to help your audience interpret data in a concise, visual manner.

When creating data visualizations, you must strike a balance between presenting enough information for your audience to understand the meaning of the visualization and not overwhelming them with too much detail. In this reading, you’ll learn tips and techniques for crafting visualizations that are both impactful and effective. You’ll explore:

- Two frameworks for organizing data
- Pre-attentive attributes

## Frameworks for organizing your thoughts about visualization

Frameworks help organize your thoughts about data visualization and give you a useful checklist to reference as you plan and evaluate your data visualization. Here are two frameworks that employ slightly different techniques. Both are intended to improve the quality of your visuals.

[The McCandless method](https://www.informationisbeautiful.net/visualizations/what-makes-a-good-data-visualization/)

You learned about the David McCandless method earlier in the course; as a refresher, the McCandless method lists four elements of good data visualization:

1. **Information:** the data with which you’re working
2. **Story:** a clear and compelling narrative or concept
3. **Goal:** a specific objective or function for the visual
4. **Visual form:** an effective use of metaphor or visual expression

The McCandless method provides terminology that isolates the specific elements of a graphic, allowing the person making a visual the ability to evaluate how well those criteria have been met. The aim when crafting a visualization is to incorporate all four elements effectively. Visualizations that fail to incorporate all four elements can be ineffective at communicating insights in various ways. For example, visual form without a goal, story, or data could be a sketch or even art. Data in visual form without a goal or function is just a pretty picture. Data with a goal but no story or visual form can be boring. All four elements need to be present to create an effective visual.

[Kaiser Fung’s Junk Charts trifecta checkup](https://junkcharts.typepad.com/junk_charts/junk-charts-trifecta-checkup-the-definitive-guide.html)

This approach is a set of questions that can help consumers of data visualization critique what they are consuming and determine how effective it is. You can also use these questions to determine if your data visualization is effective:

1. What is the practical question?
2. What does the data say?
3. What does the visual say?

Each of these questions offers an opportunity to investigate a given problem with a slightly different context. A well-designed visual effectively answers all three of those questions at once. Moreover, this framework helps you think about your data viz from the perspective of your audience.

## Pre-attentive attributes

In addition to the frameworks mentioned above, several standard building blocks can help you construct your data visualizations. Creating effective visuals means leveraging what is known about how the brain works, and then using specific visual elements to communicate the information effectively. Pre-attentive attributes are the elements of a data visualization that people recognize automatically and without conscious effort. The essential, basic building blocks that make visuals immediately understandable are called marks and channels.

### Marks

**Marks** are basic visual objects such as points, lines, and shapes. Every mark can be broken down into four qualities:

1. **Position:** Where is a specific mark in space relative to a scale or to other marks?

For example, if you’re looking at two different trends, position allows you to compare the pattern of one element relative to another.

[](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/w13YHmt8QaiMlhM_FMoQnA_20fa0b545f3d43779dad888c4eab81f1_PoHaiHktPbMb89eEc9Vpp-UE_BTfwzjST1tLbw1_3HOQ7m0bSk9A2t7Bv-w7nM_57RH4dUH92FkOsuNe0RN6mlu15J8WF1WP3NuoToX7QUOd2UCGjzosjgeeaPnG_gaVxJm4rOoCc5r-ApSOG6ZdPiw?expiry=1717027200000&hmac=noVHL37V9OF5uLN8aZ_9NJ6t5o03S_q37z0OPBkOz3U)

2. **Size:** How big, small, long, or tall is a mark?

The comparison of object sizes can be an easy visual interpretation for humans. This can be very useful for conveying the relationship between categories or data points. However, this also presents a potential problem: The human eye can inadvertently interpret comparisons that aren’t intended to convey meaning. For example, sometimes objects that appear to be the same size when they are not. Controlling the scale of a visual is important even when comparative sizes are not intended to offer information.

[](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/G1By0iKbT6S20RyOJOLakw_8e3b96d8d62b41dab3a0e9b037da2cf1_GODjKcAHrADKXJsRxDT2itjTl9NO4ism_dt63kvp6YzrO7aIUOhVjyUscltPeyX2XNlXJwyEOGz1ibCd7JZXTnAlcjVB3Wvtfjcszugj1WSA4XWqoGP-UHGlrlC54ZNksUkdKtXHlg6Wg7AD_HJMgZU?expiry=1717027200000&hmac=CpC9zLIysA4H93lhKqT7Geq5SUsqkjFJKQev6L7LQsU)

3. **Shape:** Does the shape of a specific object communicate something about it?

Rather than using simple dots or lines, a bit of creativity can enhance how quickly people are able to interpret a visual by using shapes that align with a given application. In the example below, it is immediately obvious that numbers of people are represented because the bars are person-shaped.

[](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/vIWV0cFASZG52lgye2TkcA_32e7afe4ba304c8db5d3dd396a1e5ff1__mfHWWDLd73KXZcCE8V0tPKY1iltunaMx63y5jMoIXySA0-d1Hx40MZctiQIlt2yZNTr_r0wp3NRjDA7L8mrPRJPZls-ta5RPIeDbYssZMDiLrfWolXOXKF5kkY67YPr8WfkgMzxZK-WNlB53g-_rIU?expiry=1717027200000&hmac=xuZNgd_wRiwNfC2O83nkaAAM-6B_nocFUl_uihkBhMA)

4. **Color:** What color is a mark?

Colors can be used both as a simple differentiator of groupings or as a way to communicate other concepts such as profitable versus unprofitable, or hot versus cold.

[](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/i6Lpsc88RzeYrF-r61-lkA_c9ee968f09d24a33849524397a00a7f1_uWZn95j6KM0A4os33IazLDL0nNrpIix7WMtlZ_4sb9HafOB0G4kVuQ7vR0oXEhn9WVnLkCKj8sAMffZKaZHSN7z6gkgcLfK1plWtwxXdaFWB5mnMii8lgVewDtq6DRmzDad_9yzAFpQ1kFoGm12aWE8?expiry=1717027200000&hmac=OXIynnyohDvMoOaGPhNpjw3HM7pQmRgsKDrrRWQqf74)

### Channels

**Channels** are visual aspects or variables that represent characteristics of the data in a visualization. They are basically specialized marks that have been used to visualize data. It’s important to understand that channels vary in terms of how effective they are at communicating data based on three elements:

1. **Accuracy:** Are the channels helpful in accurately estimating the values being represented?

For example, color is very accurate when communicating categorical differences, such as apples and oranges. But it is much less effective when distinguishing quantitative data, such as 5 from 5.5.

[](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/Wf6s1QnXRXSjIqWek_8Sag_d7aefd5069c34982bb9e2b6ee00083f1_eddRCinr1PXCxLOOT7ouF1uWgWXoPJsomsNUfjno7rJ4AT4IDk10Elhyvr8HX8wIfxIj2Xj0ATEHcGv26wenha8PMqjkWo3UnZOToCze3iWgzhZx9_a6Zth5fSPHR7wC6fKxY0B4ICh9jHbLyB4L0QI?expiry=1717027200000&hmac=qKLT70i9yRWxTE7XkOyZzuVgtfe5EdX2ol_hpFQNbrM)

2. **Popout:** How easy is it to distinguish certain values from others?

There are many ways of drawing attention to specific parts of a visual, and lots of them leverage pre-attentive attributes including line length, size, line width, shape, enclosure, hue, and intensity.

[](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/sxYBbaJKSsuP4_7UcjOeew_d8c55324fda24a5c9f4d53f59c393df1_9V9JqTSQJKOQ5Gn-fkp-ZmJILLWBHwvKOJGFXhrBXs2Vo2mOVUENTLqJbs9nQucXedmVprZ_EhmZz2JBTYTVpfWtSGDqfUaEOxP0Bm8TUwbKYLwjPwd4zpbL2AFUQJZ3xKKfrNqDoY8ofGqkPvqaI3Y?expiry=1717027200000&hmac=W9U2s14ptLqOJRw5hVimmkw6nbOMpiItXPHgDtW3b4U)

3. **Grouping:** How effective is a channel at communicating groups that exist in the data?

Consider the proximity, similarity, enclosure, connectedness, and continuity of the channel.

[](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/YVCqvj29RueUw-qbXakeiQ_55494966d85946208cb20fa514cddcf1_clRwSjOaDIJfbIETWvYtnENapMqisUqPNl6ZOpdVKMyD8UwKbulM6NodwVe3N_ePiuwzGm9qbaWSS10vHgnhAeICBrN5j4sDpO931SkKSriacYXA8OHcb3XYkyZzsrV5jD1x-CMXSxQ0ps1cOD0oEv8?expiry=1717027200000&hmac=ZzH4mO6Bao_smUomwsru4bl3VXcVhr5LEnO4ccQERHw)

But, remember: The more you emphasize one single thing, the more that counts. Emphasis diminishes with each item you emphasize because the items begin to compete with one another.

## Key takeaways

Throughout your career as an analyst, you will use different techniques and types of data visualizations to present data and insights in a concise, impactful manner. This will include organizing your data, selecting the right type of data visualizations, and designing them  in such a way that they are easy to understand and highly communicative while avoiding any visuals that are misleading or inaccurate.

Keep in mind that data visualization is an art form, and it takes time to develop these skills. Over your career as a data analyst, you will  learn how to design and evaluate data visualizations. Use these tips to think critically about data visualization—both as a creator and as an audience member.

## Resources

- [The beauty of data visualization](https://www.ted.com/talks/david_mccandless_the_beauty_of_data_visualization?language=en#t-150183): In this video, David McCandless explains the need for design to not just be beautiful, but for it to be meaningful as well. Data visualization must be able to balance function and form for it to be relevant to your audience.
- [‘The McCandless Method’ of data presentation](https://artscience.blog/home/the-mccandless-method-of-data-presentation): At first glance, this blog appears to be written by a David McCandless fan, and it is. However, it contains very useful information and provides an in-depth look at the 5-step process that McCandless uses to present his data.
- [Information is beautiful](https://informationisbeautiful.net/): Founded by McCandless himself, this site serves as a hub of sample visualizations that make use of the McCandless method. Explore data from the news, science, the economy, and so much more and learn how to make visual decisions based on facts from all kinds of sources.
- [Beautiful news](https://informationisbeautiful.net/beautifulnews/): In this McCandless collection, explore uplifting trends and statistics that are beautifully visualized for your creative enjoyment. A new chart is released every day so be sure to visit often to absorb the amazing things happening all over the world.
- [The Wall Street Journal Guide to Information Graphics: The Dos and Don'ts of Presenting Data, Facts, and Figures](https://www.amazon.com/Street-Journal-Guide-Information-Graphics/dp/0393072959): This is a comprehensive guide to data visualization, including chapters on basic data visualization principles and how to create useful data visualizations even when you find yourself in a tricky situation. This is a useful book to add to your data visualization library, and you can reference it over and over again.

---

# Connect images with data

[index (38).mp4](Understand%20data%20visualization%20ca4ad341f695412f9bf9319d6212921c/index_(38).mp4)

**Importance of Data Visualization:**

- Helps analysts and stakeholders understand data better.
- Makes complex data easier to digest and interpret.
- Facilitates decision-making based on data insights.

**Connecting Data and Images:**

- Visualizations help bridge the gap between data and its meaning.
- Different types of visualizations are used for different purposes.

**Examples of Data Visualizations:**

- **Bar graphs:** Compare values across categories using bars of varying heights.
- **Line graphs:** Track changes in data over time using lines.
- **Pie charts:** Show proportions of a whole using slices of a pie.
- **Maps:** Display geographically-based data using color-coded regions.

**Misleading Visualizations:**

- **Truncated bar charts:** Starting the y-axis above zero can distort data proportions.
- **Pie charts with overlapping categories:** Can make it difficult to compare proportions accurately.

**Key Takeaways:**

- Choose the right visualization for the type of data you want to communicate.
- Be mindful of potential biases and distortions in visualizations.
- Ensure your visualizations are clear, accurate, and easy to understand.

---

# The beauty of visualizing

You will find that organizing your data and communicating your results are significant parts of a data analyst’s role. In this reading, you are going to navigate different resources for effective data visualization that will allow you to choose the best model to present your data.

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/1AeyDenyQaaHsg3p8lGmqA_b2198c7046b948b9a13e6c12b845aed4_Screen-Shot-2021-02-22-at-5.05.08-PM.png?expiry=1717027200000&hmac=kStMwzW4KImOzdtcN9hB3_MR6Zg5KQE8GrAcjJw4BM0)

## Inspiration is in the air

**Data visualization** is the graphical representation of data. But why should data analysts care about data visualization? Well your audience won’t always have the ability to interpret or understand the complex information that you relay to them so your job is to inform them of your analysis in a way that is meaningful, engaging, and easy to understand. Part of why data visualization is so effective is because people’s eyes are drawn to colors, shapes, and patterns, which makes those visual elements perfect for telling a story that goes beyond just the numbers.

Of course, one of the best ways to understand the importance of data visualization is to go through different examples of it. As a junior data analyst, you want to have several visualization options for your creative process whenever you need. Below is a list of resources that can inspire your next data-driven decisions, as well as teach you how to make your data more accessible to your audience:

- [The data visualization catalogue](https://datavizcatalogue.com/#google_vignette): Not sure where to start with data visualization? This catalogue features a range of different diagrams, charts, and graphs to help you find the best fit for your project. As you navigate each category, you will get a detailed description of each visualization as well as its function and a list of similar visuals.
- [The 25 best data visualizations](https://visme.co/blog/best-data-visualizations/): In this collection of images, explore the best examples of data that gets made into a stunning visual. Simply click on the link below each image to get an in-depth view of each project, and learn why making data visually appealing is so important.
- [10 data visualization blogs](https://www.tableau.com/learn/articles/best-data-visualization-blogs): Each link will lead you to a blog that is a fountain of information on everything from data storytelling to graphic data. Get your next great idea or just browse through some visual inspiration.
- [Information is beautiful](https://informationisbeautiful.net/wdvp/gallery-2019/): Founded by David McCandless, this gallery is dedicated to helping you make clearer, more informed visual decisions based on facts and data. These projects are made by students, designers, and even data analysts to help you gain insight into how they have taken their own data and turned it into visual storytelling.
- [Data studio gallery](https://datastudio.google.com/gallery?category=visualization): Information is vital, but information presented in a digestible way is even more useful. Browse through this interactive gallery and find examples of different types of data communicated visually. You can even use the data studio tool to create your own data-driven visual.

## Engage your audience

Remember: an important component of being a data analyst is the ability to communicate your findings in a way that will appeal to your audience. Data visualization has the ability to make complex (and even monotonous) information easily understood, and knowing how to utilize data visualization is a valuable skill to have. Your goal is always to help the audience have a conversation with the data so your visuals draw them into the conversation. This is especially true when you have to help your audience engage with a large amount of data, such as the flow of goods from one country to other parts of the world.

---

# A recipe for a powerful visualization

[index (39).mp4](Understand%20data%20visualization%20ca4ad341f695412f9bf9319d6212921c/index_(39).mp4)

**Key Points:**

- **Focus on relevant data:** Only show the data your audience needs to understand your findings. Avoid overwhelming them with unnecessary information.
- **Visualize change over time:** Use time series charts to show how data changes over a period of time.
- **Show data distribution:** Use histograms to show how data is distributed across different ranges.
- **Rank data:** Use bar charts with horizontal bars to show ranked data.
- **Use correlation charts with caution:** Correlation does not imply causation. Be careful not to mislead your audience.
- **Choose the right visualization for your data:** Different types of visualizations are effective for different types of data and analyses.

**Definitions:**

- **Time series chart:** A chart that shows how data changes over time.
- **Histogram:** A chart that shows how data is distributed across different ranges.
- **Ranked bar chart:** A bar chart with horizontal bars that shows data ranked in ascending or descending order.
- **Correlation chart:** A chart that shows the relationship between two variables.
- **Causation:** A cause-effect relationship between two variables.

---

# Correlation and causation

In this reading, you will examine correlation and causation in more detail. Let’s review the definitions of these terms:

- **Correlation** in statistics is the measure of the degree to which two variables move in relationship to each other. An example of correlation is the idea that “As the temperature goes up, ice cream sales also go up.” It is important to remember that correlation doesn’t mean that one event causes another. But, it does indicate that they have a pattern with or a relationship to each other. If one variable goes up and the other variable also goes up, it is a positive correlation. If one variable goes up and the other variable goes down, it is a negative or inverse correlation. If one variable goes up and the other variable stays about the same, there is no correlation.
- **Causation** refers to the idea that an event leads to a specific outcome. For example, when lightning strikes, we hear the thunder (sound wave) caused by the air heating and cooling from the lightning strike. Lightning causes thunder.

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/vSdSBR13Sk6nUgUdd8pO_A_21e08b21d16f4bc6b28a7db5f1d58115_Screen-Shot-2021-02-26-at-5.54.00-PM.png?expiry=1717027200000&hmac=-EnVh0XccVyu8zRhFjDf_sVGvVsKakTFcY8jH-JSsNE)

## Why is differentiating between correlation and causation important?

When you make conclusions from data analysis, you need to make sure that you don’t assume a causal relationship between elements of your data when there is only a correlation. When your data shows that outdoor temperature and ice cream consumption both go up at the same time, it might be tempting to conclude that hot weather **causes** people to eat ice cream. But, a closer examination of the data would reveal that every change in temperature doesn’t lead to a change in ice cream purchases. In addition, there might have been a sale on ice cream at the same time that the data was collected, which might not have been considered in your analysis.

Knowing the difference between correlation and causation is important when you make conclusions from your data since the stakes could be high. The next two examples illustrate the high stakes to health and human services.

### **Cause of disease**

For example, pellagra is a disease with symptoms of dizziness, sores, vomiting, and diarrhea. In the early 1900s, people thought that the disease was caused by unsanitary living conditions. Most people who got pellagra also lived in unsanitary environments. But, a closer examination of the data showed that pellagra was the result of a lack of niacin (Vitamin B3). Unsanitary conditions were related to pellagra because most people who couldn’t afford to purchase niacin-rich foods also couldn’t afford to live in more sanitary conditions. But, dirty living conditions turned out to be a correlation only.

### **Distribution of aid**

Here is another example. Suppose you are working for a government agency that provides SNAP benefits. You noticed from the agency’s Google Analytics that people who qualify for the benefits are browsing the official website, but they are leaving the site without signing up for benefits. You think that the people visiting the site are leaving because they aren’t finding the information they need to sign up for SNAP benefits. Google Analytics can help you find clues (correlations), like the same people coming back many times or how quickly people leave the page. One of those correlations might lead you to the actual cause, but you will need to collect additional data, like in a survey, to know exactly why people coming to the site aren’t signing up for SNAP benefits. Only then can you figure out how to increase the sign-up rate.

## Key takeaways

In your data analysis, remember to:

- Critically analyze any correlations that you find
- Examine the data’s context to determine if a causation makes sense (and can be supported by all of the data)
- Understand the limitations of the tools that you use for analysis

## Further information

You can explore the following article and training for more information about correlation and causation:

- [**Correlation is not causation](https://towardsdatascience.com/correlation-is-not-causation-ae05d03c1f53):** This article describes the impact to a business when correlation and causation are confused.
- [**Correlation and causation](https://www.khanacademy.org/test-prep/praxis-math/praxis-math-lessons/gtp--praxis-math--lessons--statistics-and-probability/a/gtp--praxis-math--article--correlation-and-causation--lesson) (Khan Academy lesson):** This lesson describes correlation and causation along with a working example. Follow the examples of the analysis and notice if there is a positive correlation between frostbite and sledding accidents.

---

# Dynamic visualizations

[index (40).mp4](Understand%20data%20visualization%20ca4ad341f695412f9bf9319d6212921c/index_(40).mp4)

**Introduction:**

- The video begins by acknowledging that data analysts face many choices when creating visualizations.
- These choices should ensure that the visuals are meaningful and effective.

**Static vs. Dynamic Visualizations:**

- **Static visualizations:**
    - Do not change over time unless edited.
    - Useful for controlling the data and story.
    - Examples: printed charts, graphs in spreadsheets.
- **Dynamic visualizations:**
    - Interactive or change over time.
    - Users have control over what they see.
    - Examples: Tableau visualizations, real-time data updates.

**Tableau Example:**

- The video showcases a Tableau visualization about happiness scores from 2015 to 2017.
- Users can interact with the visualization to see changes in happiness scores over time.
- This highlights the power of dynamic visualizations for engaging audiences.

**Considerations:**

- The choice between static and dynamic visualizations depends on:
    - The data being visualized.
    - The audience.
    - The presentation format.
- Finding the right balance between interactivity and control is crucial.

**Conclusion:**

- Understanding the difference between static and dynamic visualizations is essential for effective data storytelling.
- The next lecture will delve deeper into visualization design.

**Key Points:**

- Static visualizations offer control but lack interactivity.
- Dynamic visualizations engage audiences but require careful consideration.
- Tableau is a powerful tool for creating interactive visualizations.
- Balancing interactivity and control is key to effective data storytelling.

**Definitions:**

- **Static visualization:** A visualization that does not change over time unless edited.
- **Dynamic visualization:** A visualization that is interactive or changes over time.
- **Interactivity:** The ability of users to control what they see in a visualization.
- **Data storytelling:** The process of using data to tell a compelling story.

---

# The wonderful world of visualizations

As a data analyst, you will often be tasked with relaying information and data that your audience might not readily understand. Presenting your data visually is an effective way to communicate complex information and engage your stakeholders. One question to ask yourself is: “what is the best way to tell the story within my data?” This reading includes several options for you to choose from (although there are many more).

## Line chart

A **line chart** is used to track changes over short and long periods of time. When smaller changes exist, line charts are better to use than bar graphs. Line charts can also be used to compare changes over the same period of time for more than one group.

Let’s say you want to present the graduation frequency for a particular high school between the years 2008-2012. You would input your data in a table like this:

| **Year** | **Graduation rate** |
| --- | --- |
| 2008 | 87 |
| 2009 | 89 |
| 2010 | 92 |
| 2011 | 92 |
| 2012 | 96 |

From this table, you are able to present your data in a line chart like this:

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/0ePQrdhCShyj0K3YQhocnw_66093e0e5563465eb9ed4254808c35f7_Screen-Shot-2021-02-26-at-4.36.35-PM.png?expiry=1717027200000&hmac=TMv03-cpeupya3NXxGfWT8d0JNURp83Ruum8hWJDJGo)

Maybe your data is more specific than above. For example, let’s say you are tasked with presenting the difference of graduation rates between male and female students. Then your chart would resemble something like this:

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/vHWto26pS3y1raNuqRt8Ig_a25ef4386a9a456489cbe61f02f5c77d_Screen-Shot-2021-02-26-at-4.37.23-PM.png?expiry=1717027200000&hmac=Q0Om_oWdW-Zv66sP8g43fqVgygUiw0VsTIUyK961B68)

## Column chart

**Column charts** use size to contrast and compare two or more values, using height or lengths to represent the specific values.

The below is example data concerning sales of vehicles over the course of 5 months:

| **Month** | **Vehicles sold** |
| --- | --- |
| August | 2,800 |
| September | 3,700 |
| October | 3,750 |
| November | 4,300 |
| December | 4,600 |

Visually, it would resemble something like this:

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/n4cD_qVKSOyHA_6lSpjsQQ_9fd9f75dcd274bdaaa9505f399911fe5_Screen-Shot-2021-02-26-at-4.38.08-PM.png?expiry=1717027200000&hmac=l_kcwN3kO1h6IQQH0YhBkCYYJWRJVkxx-C9_crUT55E)

What would this column chart entail if we wanted to add the sales data for a competing car brand?

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/ZD_NDLAfSaq_zQywHxmqQw_c3c5fe0a7f6e4ae48fe3a252c9be3013_Screen-Shot-2021-02-26-at-4.38.42-PM.png?expiry=1717027200000&hmac=KN2ThCHpMN3o-Rjla-PQdxtJbsSr1L1WjoLGAEKak_k)

## Heatmap

Similar to bar charts, **heatmaps** also use color to compare categories in a data set. They are mainly used to show relationships between two variables and use a system of color-coding to represent different values. The following heatmap plots temperature changes for each city during the hottest and coldest months of the year.

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/ePb_n408Teq2_5-NPN3qIA_b74401e8715a49fb842965c813f3ef1b_Screen-Shot-2021-02-26-at-4.39.28-PM.png?expiry=1717027200000&hmac=za6MPg75Lg9AXfDuTNMvAUKek8qrTmFvD0oZb7xbtgs)

## Pie chart

The **pie chart** is a circular graph that is divided into segments representing proportions corresponding to the quantity it represents, especially when dealing with parts of a whole.

For example, let’s say you are determining favorite movie categories among avid movie watchers. You have gathered the following data:

| **Movie category** | **Preference** |
| --- | --- |
| Comedy | 41% |
| Drama | 11% |
| Sci-fi | 3% |
| Romance | 17% |
| Action | 28% |

Visually, it would resemble something like this:

Action- 28%
Comedy- 41%
Romance- 17%
Sci-fi- 3%
Drama- 11%

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/uQnZmwh2R_2J2ZsIdsf9Sg_aae18f0b697d429191e9d2690c5f74c4_Screen-Shot-2021-02-26-at-4.40.22-PM.png?expiry=1717027200000&hmac=icuT1OptKXaiv8mIvu2KyHczmVZqsQamOyw6HOnRvX8)

## Scatterplot

**Scatterplots** show relationships between different variables. Scatterplots are typically used for two variables for a set of data, although additional variables can be displayed.

For example, you might want to show data of the relationship between temperature changes and ice cream sales. It would resemble something like this:

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/UnuZ6BvMRja7megbzGY2bQ_642b9eda7a2d424ca958dc9282d6b790_Screen-Shot-2021-04-21-at-10.29.31-AM.png?expiry=1717027200000&hmac=hd24ckCc46Spt83x8teBqnugCY87Kg4JOuucvLwIDXo)

As you may notice, the higher the temperature got, the more demand there was for ice cream—so the scatterplot is great for showing the relationship between the two variables.

## Distribution graph

A **distribution graph** displays the spread of various outcomes in a dataset.

Let’s apply this to real data. To account for its supplies, a brand new coffee shop owner wants to measure how many cups of coffee their customers consume, and they want to know if that information is dependent on the days and times of the week. That distribution graph would resemble something like this:

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/iXJq4GcJRM-yauBnCZTPkQ_68a9c0b7f2314e4c82bb4f134c178c52_Screen-Shot-2021-02-26-at-4.42.30-PM.png?expiry=1717027200000&hmac=waHeThVDwygX9i1gkTGz-PGzzTHoVA3CekxdId7--Lc)

From this distribution graph, you may notice that the amount of coffee sales steadily increases from the beginning of the week, reaching the highest point mid-week, and then decreases towards the end of the week.

If outcomes are categorized on the x-axis by distinct numeric values (or ranges of numeric values), the distribution becomes a **histogram**. If data is collected from a customer rewards program, they could categorize how many customers consume between one and ten cups of coffee per week. The histogram would have ten columns representing the number of cups, and the height of the columns would indicate the number of customers drinking that many cups of coffee per week.

Reviewing each of these visual examples, where do you notice that they fit in relation to your type of data? One way to answer this is by evaluating patterns in data. Meaningful patterns can take many forms, such as:

- **Change:** This is a trend or instance of observations that become different over time. A great way to measure change in data is through a line or column chart.
- **Clustering:** A collection of data points with similar or different values. This is best represented through a distribution graph.
- **Relativity:** These are observations considered in relation or in proportion to something else. You have probably seen examples of relativity data in a pie chart.
- **Ranking:** This is a position in a scale of achievement or status. Data that requires ranking is best represented by a column chart.
- **Correlation:** This shows a mutual relationship or connection between two or more things. A scatterplot is an excellent way to represent this type of data pattern.

## Studying your data

Data analysts are tasked with collecting and interpreting data as well as displaying data in a meaningful and digestible way. Determining how to visualize your data will require studying your data’s patterns and converting it using visual cues. Feel free to practice your own charts and data in spreadsheets. Simply input your data in the spreadsheet, highlight it, then insert any chart type and view how your data can be visualized based on what you choose.

---

# Data grows on decision trees

With so many visualization options out there for you to choose from, how do you decide what is the best way to represent your data?

A **decision tree** is a decision-making tool that allows you, the data analyst, to make decisions based on key questions that you can ask yourself. Each question in the visualization decision tree will help you make a decision about critical features for your visualization. Below is an example of a basic decision tree to guide you towards making a data-driven decision about which visualization is the best way to tell your story. Please note that there are many different types of decision trees that vary in complexity, and can provide more in-depth decisions.

- 
    
    ![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/iV-otJ4pQCafqLSeKZAmjg_9519536f4aa94268af3600263793b237_Screen-Shot-2021-02-23-at-4.21.13-PM.png?expiry=1717027200000&hmac=X5vmbEAf2pys44SF8FaW_yyq7-Tl4MSN3fPkozo9O_k)
    
    - Does your data have only one numeric variable? Histogram or Density plot
    -Are there multiple data sets? Line chart or pie chart
    -Are you measuring changes over time? Bar chart
    -Do relationships between the data need to be shown? Scatter plot or heatmap

## Begin with your story

Start off by evaluating the type of data you have and go through a series of questions to determine the best visual source:

- **Does your data have only one numeric variable?** If you have data that has one, continuous, numerical variable, then a histogram or density plot are the best methods of plotting your categorical data. Depending on your type of data, a bar chart can even be appropriate in this case. For example, if you have data pertaining to the height of a group of students, you will want to use a histogram to visualize how many students there are in each height range:

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/rVQyQMBvRoKUMkDAbwaCWg_aaa67e65c6254e76998babe14f84b525_Screen-Shot-2021-03-02-at-10.48.02-AM.png?expiry=1717027200000&hmac=usQHZ4LkeVRGx-Y16pSjApFYKL6YoZCCZ_BARMEjURY)

- **Are there multiple datasets?** For cases dealing with more than one set of data, consider a line or pie chart for accurate representation of your data. A line chart will connect multiple data sets over a single, continuous line, showing how numbers have changed over time. A pie chart is good for dividing a whole into multiple categories or parts. An example of this is when you are measuring quarterly sales figures of your company. Below are examples of this data plotted on both a line and pie chart.

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/3MRAH5jdRuaEQB-Y3Sbm7A_67d5ecf363804b8d8f285bfc648b3639_Screen-Shot-2021-03-02-at-10.48.34-AM.png?expiry=1717027200000&hmac=m44dXuassNrlZ-U4B8tVuHWPd7uGCVNJc-4V1tt0mw8)

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/y7sQLyDRQpG7EC8g0cKRAA_e678b13ea07e4d15ad451695bf469514_Screen-Shot-2021-03-02-at-10.48.39-AM.png?expiry=1717027200000&hmac=TEq442_ePr8A0Q0ua9V516VRWuiIwFFfCwQUdFNod_k)

- **Are you measuring changes over time?** A line chart is usually adequate for plotting trends over time. However, when the changes are larger, a bar chart is the better option. If, for example, you are measuring the number of visitors to NYC over the past 6 months, the data would look like this:

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/Qb5mXHLIQuu-ZlxyyNLrbg_db202cb2d1c4496b8953ed5212b0b465_Screen-Shot-2021-03-02-at-10.50.00-AM.png?expiry=1717027200000&hmac=Osgq3Nmo5j4TTsJKu6HdU8ZsfpjhbLMjffRvxr5W5wM)

- **Do relationships between the data need to be shown?** When you have two variables for one set of data, it is important to point out how one affects the other. Variables that pair well together are best plotted on a scatterplot. However, if there are too many data points, the relationship between variables can be obscured so a heat map can be a better representation in that case. If you are measuring the population of people across all 50 states in the United States, your data points would consist of millions so you would use a heat map. If you are simply trying to show the relationship between the number of hours spent studying and its effects on grades, your data would look like this:

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/s3R2A0spTg-0dgNLKe4Paw_b5332baafd9346bb8d1311bbda388d5d_Screen-Shot-2021-03-02-at-10.50.39-AM.png?expiry=1717027200000&hmac=9phkm8hacXFfvXyutkzCR4DRrM2iXZTqUHS0mYu1sYE)

## Additional resources

The decision tree example used in this reading is one of many. There are multiple decision trees out there with varying levels of details that you can use to help guide your visual decisions. If you want more in-depth insight into more visual options, explore the following resources:

- [From data to visualization](https://www.data-to-viz.com/): This is an excellent analysis of a larger decision tree. With this comprehensive selection, you can search based on the kind of data you have or click on each graphic example for a definition and proper usage.
- [Selecting the best chart](https://www.youtube.com/watch?v=C07k0euBpr8): This two-part YouTube video can help take the guesswork out of data chart selection. Depending on the type of data you are aiming to illustrate, you will be guided through when to use, when to avoid, and several examples of best practices. [Part 2](https://www.youtube.com/watch?v=qGaIB-bRn-A) of this video provides even more examples of different charts, ensuring that there is a chart for every type of data out there.

---

# Choosing a visualization type

## Activity Overview

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/UWFf-U9hTzKhX_lPYX8yBw_8c2e9cd211e3479a89816c7b1816ab07_image4.png?expiry=1717027200000&hmac=S7U_iCIr_A-T4nGo509ICpMLn8bVPSRIGsZ5Rx4tEY4)

Now that you’ve been introduced to decision trees, pause for a moment and practice what you’ve been learning. In this self-reflection, you’ll first review decision trees and data visualization best practices. Then, you’ll examine a scenario, use a decision tree to determine the most effective chart type based on the scenario, and respond to brief questions.

This self-reflection will help you develop insights into your own learning and prepare you to use a decision tree to help you plan your next visualization. As you answer questions—and come up with questions of your own—you will consider concepts, practices, and principles to help refine your understanding and reinforce your learning. Answering and asking questions in this self-reflection will help to reinforce what you’ve learned so far, so it will be easier for you to remember it later.

Next, review decision tree uses, concepts, and best practices.

# **Review decision tree uses, concepts, and best practices**

**Decision tree uses**

A **decision tree** is a flowchart that you can use to help frame larger decisions as a series of smaller yes/no decisions. These are useful when trying to choose the best data visualization to communicate a given message to your audience. Because different visualizations have different strengths and weaknesses, a decision tree can help you pick the best visualization for your data and audience. Here’s the decision tree you examined earlier in this course:

Path 1: Does your data have only one numeric variable? If so, choose a histogram or a density plot. Path 2: Are they multiple datasets? If so, choose a line chart or a pie chart. Path 3: Are you measuring changes over time? If so, choose a bar chart. Path 4: Do relationships between data need to be shown? If so, choose a scatterplot or a heatmap.

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/Yvz1NiVHTeSUTBqRMfW6Zw_add6135ca6ba494580a5c26817eb8ae1_image.png?expiry=1717027200000&hmac=HiK90U4sOmqRYksR144pzO9HX3TlDHLEyYRBJvwuDT0)

**Decision tree concepts and best practices**

Before you use the decision tree in a scenario to create successful data visualizations, take a moment to review some of the design concepts and best practices you’ve learned so far. Recall that there are four elements of successful data visualization:

- **Information:** reflects the conclusion you’ve drawn from the data, which you will communicate with visualization
- **Story:** adds meaning to the data and makes it interesting
- **Goals:** makes the data usable and useful
- **Visual form:** creates both beauty and structure

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/nFq79wWOSAC69Riv8u086w_91eec3046e334a6981c6c02f694de7e1_image.png?expiry=1717027200000&hmac=cvwBafahq_vaUudlgpMA0w3oW5uZnBeofM487SXYKtI)

Keep these elements in mind as you review the scenario below. This will help you make better data visualizations by helping you connect the information you want to communicate with your audience and your goals.

Here are some additional best practices to keep in mind:

- Your audience should know what they are observing within five seconds of being shown a data visualization. Visuals should be clear and easy to follow.
- In the five seconds after that, your audience should understand the conclusion your visualization is making—even if they aren’t familiar with your research.
- As long as it’s not misleading, you should visually represent only the data that your audience needs to understand your findings. Including irrelevant data may confuse, distract, or overwhelm your audience.

These rules will guide you as you create your visualizations and you can apply them as you consider the following scenario.

# **Scenario**

You’re a junior data analyst at a local retailer. In your current data analysis project, you’ve been exploring sales data for all of your company’s products, including the top products and sales trends for the last year. You need to present the results of this analysis to the company executives. Your goal for this presentation is to demonstrate how sales of the company’s products have changed over the last 12 months. Your findings about the two top-selling products include:

| **Product name** | **Units sold** | **Time period with highest sales** |
| --- | --- | --- |
| Product A | 2.5 million | 70% of total annual sales occur in October, November, and December |
| Product B | 1.9 million | Mostly consistent sales year-round, with a slight increase in November, December, and January |

Your audience is the chief marketing officer (CMO) and marketing department vice presidents (VPs), not other data analysts or engineers. The audience will use the information you present to make decisions on how to allocate the advertising budget for each product for the coming year.

Now, use the decision tree.

# **Use the decision tree**

Consider what you know about the type of data you have (product sales data) and the kind of relationships you are trying to communicate (time periods with the most sales). Use this information to navigate the decision tree and use it to determine what type of visualization would be most appropriate.

Based on how you want to represent the sales data, there are several choices that would result in a successful chart. You could frame this by using a comparison of different categories with a bar graph or by showing how the composition of total sales changes month-to-month as a line chart with lines for each product.

Either of these would be a successful choice. Combined with effective use of design principles, either could accurately communicate the message you need to convey to company leadership. This message being: Sales for Product A are extremely seasonal, so they may want to consider reducing their advertising spend for this product when it’s out of season.

---