<div align="center">
  <img src="https://raw.githubusercontent.com/MadanThevar/Amazon-Viewership-Analysis-/main/giphy.webp" alt="Amazon Viewership Analysis" width="750"/>
</div>


<div align="center">
  <h1> 🎬 Amazon Prime Movies and TV Shows Analysis 🎥 </h1>
</div>

## 📊 Power-Bi Dashboard

<img width="940" alt="Screenshot 2024-08-18 at 13 07 18" src="https://github.com/user-attachments/assets/9297dfeb-9e49-41d0-a58d-11e04dc3ff6b">

## 🌟 Overview

Welcome to my data analysis project on **Amazon Prime Movies and TV Shows**! 📺 The goal of this project was to dive deep into the content available on Amazon Prime, exploring trends, distributions, and insights using the power of **Power BI**. 🌐 This dashboard provides a comprehensive look at how content is distributed across various categories, ratings, regions, and more.

## 📊 Dataset

The dataset used is **`amazon_prime_titles.csv`**, featuring over **9,600 titles** 🌟 from a diverse range of countries 🌍. It includes essential details such as the title, category (Movie/TV Show), content rating, release year, and the region of release.

## 🎯 Key Objectives

- **🔍 Content Rating Analysis:** Determine how titles are distributed across different content ratings.
- **🎬 Category Breakdown:** Analyze the split between Movies and TV Shows on Amazon Prime.
- **🗺️ Geographical Distribution:** Visualize where and when content was released across the globe from 2014 to 2021.
- **🌏 Top Countries by Content:** Identify the leading countries contributing content to Amazon Prime.
- **🎭 Cast Popularity:** Discover the most frequently featured actors in Amazon Prime content.

## 🕵️‍♂️ Dashboard Walkthrough

### 1. **🔖 Rating by Show ID**
   - **Visual Insight:** A bar chart showing the distribution of titles by content rating.
   - **✨ Key Finding:** Titles rated **13+** dominate the platform, followed by **16+** and **18+** categories.

### 2. **🍿 Category Breakdown**
   - **Visual Insight:** A pie chart representing the proportion of Movies vs. TV Shows.
   - **✨ Key Finding:** **Movies** make up the bulk of content on Amazon Prime, contributing to over **86%** of the total.

### 3. **🌍 Geographical Distribution**
   - **Visual Insight:** A world map showing content releases by region from 2014 to 2021.
   - **✨ Key Finding:** **North America** and **Europe** lead the charge in content releases, with increasing activity in **Asia**.

### 4. **🌐 Top Countries by Content**
   - **Visual Insight:** A bar chart listing the top countries producing content for Amazon Prime.
   - **✨ Key Finding:** The **United States** is the top contributor, followed closely by **India** and the **United Kingdom**.

### 5. **🎭 Top Cast Members**
   - **Visual Insight:** A bar chart showing the most frequently featured actors on Amazon Prime.
   - **✨ Key Finding:** **Danny DeVito**, **Arnold Schwarzenegger**, and **Jayasurya** are among the top recurring actors.

## 🧠 Additional Insights

While the dashboard already provides valuable insights, several other analyses could further enhance understanding:

- **📈 Trend Analysis:** Explore the yearly growth in the number of titles released to identify any significant trends.
- **🌎 Regional Preferences:** Investigate if certain genres or ratings are more popular in specific regions.
- **🕒 Release Timing:** Analyze the release timings of titles (e.g., quarter of the year) to identify patterns in content drops.
- **🔁 Content Longevity:** Determine how long titles remain popular after their release.
- **👥 Audience Demographics:** Although not available in the current dataset, linking demographic data could reveal audience preferences for different types of content.

## 🧑‍💻 Important DAX Functions Used

In this project, several DAX (Data Analysis Expressions) functions were utilized to create calculated columns and measures, enhancing the analytical capabilities of the dashboard. Here are five key DAX functions used:

1. **`CALCULATE()`**
   - **Purpose:** Modifies the filter context of a calculation, allowing for conditional calculations.
   - **Example:**
     ```dax
     Total Movies = CALCULATE(COUNTROWS('Titles'), 'Titles'[Category] = "Movie")
     ```
   - **Explanation:** This measure calculates the total number of movies by applying a filter to count only rows where the category is "Movie." It enhances the analysis by allowing the dashboard to focus on specific content types, helping to differentiate between Movies and TV Shows.

2. **`SUMX()`**
   - **Purpose:** Iterates over a table, evaluates an expression, and then sums the results.
   - **Example:**
     ```dax
     Total Duration = SUMX('Titles', 'Titles'[Duration])
     ```
   - **Explanation:** This measure sums the total duration of all titles. By using `SUMX()`, we can aggregate data across all titles, which could be insightful when analyzing how much content (in terms of time) is available for different categories or ratings.

3. **`FILTER()`**
   - **Purpose:** Returns a table that represents a subset of another table or expression, typically used to filter rows.
   - **Example:**
     ```dax
     Filtered Titles = FILTER('Titles', 'Titles'[Release Year] > 2015)
     ```
   - **Explanation:** This function filters the dataset to include only titles released after 2015. It is particularly useful for analyzing recent trends and understanding how content release patterns have evolved over time.

4. **`DISTINCTCOUNT()`**
   - **Purpose:** Counts the number of distinct values in a column.
   - **Example:**
     ```dax
     Distinct Countries = DISTINCTCOUNT('Titles'[Country])
     ```
   - **Explanation:** This measure counts the number of distinct countries contributing content. It adds value by highlighting the diversity of content sources, showing which regions are actively contributing to Amazon Prime's catalog.

5. **`DIVIDE()`**
   - **Purpose:** Performs division and handles cases where division by zero might occur, preventing errors.
   - **Example:**
     ```dax
     Average Rating = DIVIDE(SUM('Titles'[Rating Value]), COUNTROWS('Titles'))
     ```
   - **Explanation:** This function calculates the average rating value by dividing the total sum of ratings by the number of titles. `DIVIDE()` ensures that the calculation is error-free even if the denominator is zero, which makes the analysis more robust and reliable.

## 🚀 Room for Improvements

Although this dashboard provides valuable insights, there are several areas where it can be further improved:

- **🔗 Integrate Viewer Data:** Incorporating data on viewer preferences, watch times, and demographics could provide a more comprehensive understanding of content performance.
- **📅 Time-Series Forecasting:** Implementing time-series forecasting could help predict future trends in content releases, helping Amazon Prime strategize content planning.
- **🌐 Multi-Platform Comparison:** Compare Amazon Prime's content with other streaming platforms (e.g., Netflix, Hulu) to identify strengths and areas for improvement.
- **📝 Sentiment Analysis:** Analyze viewer reviews and ratings to understand audience sentiment towards different types of content and use this information to guide content acquisition and production.

## 🎯 Strategic Ideas to Improve Viewership and Beat Competitors

Here are some unique and trending strategies that could help Amazon Prime improve viewership and gain a competitive edge:

1. **🔍 Personalized Content Recommendations:**
   - Utilize machine learning algorithms to provide highly personalized content recommendations based on individual viewing habits and preferences. By offering tailored suggestions, Amazon Prime can enhance user engagement and retention.

2. **🎥 Exclusive Content Partnerships:**
   - Form strategic partnerships with renowned filmmakers, studios, or content creators to produce exclusive, high-quality content that can’t be found on other platforms. This could include original movies, TV shows, documentaries, and more.

3. **🎮 Interactive Storytelling:**
   - **Choose-Your-Own-Adventure:** Create shows or movies where viewers can make choices that affect the storyline, leading to multiple possible endings. This format engages the audience by giving them control over the narrative.
   - **Branching Narratives:** Similar to choose-your-own-adventure, but with more subtle choices that can influence character development, relationships, or plot direction. This can significantly enhance viewer engagement and make the viewing experience more personalized.

4. **🎥 Short-Form Episodic Content:**
   - Produce series with episodes that are 5-10 minutes long, perfect for viewers with limited time or those who prefer quick entertainment. This format could cater to busy professionals or younger audiences who favor shorter content.
   - **Webisodes and Minisodes:** Create supplementary short episodes for existing popular series that provide backstories, side plots, or character development, keeping fans engaged between full-length episodes.

5. **📱 Social Viewing Features:**
   - **Watch Parties:** Allow viewers to watch shows and movies together virtually, with synchronized playback and chat features. Integrate video calls or live reactions to enhance the communal viewing experience.
   - **Shared Playlists:** Enable users to create and share custom playlists of their favorite shows and movies, or even thematic collections, with friends or the wider community.

6. **📈 Data-Driven Content Creation:**
   - Leverage data analytics to identify content gaps and predict emerging trends, allowing Amazon Prime to create and acquire content that is more likely to succeed. This proactive approach can ensure that the platform stays ahead of the curve.

## 💬 Contact

For any questions, suggestions, or collaboration ideas, feel free to reach out via [LinkedIn](https://www.linkedin.com/in/madanthevar/) I’d love to connect! 🤝
