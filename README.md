# Social Media Sentiment Analysis

## Introduction

In today’s digital age, social media platforms have become powerful tools for brands and products to connect with their audience. The opinions shared on these platforms significantly influence public perception and, ultimately, business success. This report presents a comprehensive analysis of social media sentiment around a specific brand/product using a dataset comprising various attributes such as sentiment, text, platform, engagement metrics, and geographical information. The objective of this analysis is to monitor and analyze sentiment trends to inform strategic marketing decisions.

## Objectives

The primary objectives of this analysis are:

- **Sentiment Monitoring**: To monitor the sentiment (positive, neutral, negative, etc.) associated with the brand or product across different social media platforms.
- **Trend Analysis**: To identify how sentiment changes over time, highlighting any significant shifts in public opinion.
- **Platform-Specific Insights**: To understand sentiment distribution across different social media platforms and identify platform-specific sentiment trends.
- **Geographical Sentiment Analysis**: To analyze sentiment based on geographical data to identify regional differences in public perception.
- **Engagement Analysis**: To assess the relationship between sentiment and engagement (likes, retweets) and understand how different sentiments drive user interaction.

## Data Description

The dataset used for this analysis contains the following columns:

- **Id**: A unique identifier for each social media post.
- **Text**: The actual content of the post.
- **Sentiment**: The sentiment label of the post (Positive, Neutral, Negative, etc.).
- **Date**: The date when the post was published.
- **Username**: The username of the individual who posted the content.
- **Platform**: The social media platform (e.g., Twitter, Facebook, Instagram) where the post was published.
- **Hashtags**: Hashtags included in the post.
- **Retweets**: The number of times the post was retweeted.
- **Likes**: The number of likes the post received.
- **Country**: The geographical location associated with the post.
- **Sentiment Count**: Sentiment count measure was calculated using Power BI DAX with the formula:
  ```DAX
  SentimentCount = COUNTAX(FILTER(TableName, TableName[Sentiment] = MAX(TableName[Sentiment])), TableName[Sentiment])

  ## Data Preparation

To ensure accurate analysis, the following data preparation steps were undertaken:

- **Data Cleaning**: Missing values were handled, and any inconsistencies in data types, particularly in the Date, Sentiment, and Platform columns, were resolved.
- **Date Formatting**: The Date column was standardized to ensure consistency and enable effective time-series analysis.
- **White Spaces**: White spaces were found in most of the strings, which were fixed using the `TRIM` function.

## Data Analysis

The analysis was carried out using SQL for data extraction and Power BI for visualization. The key analyses performed include:

### Sentiment Distribution

A sentiment distribution analysis was conducted to understand the overall public perception of the brand or product.

**Tree Map Visualization**

### Sentiment Over Time

To track how sentiment changed over time, a time-series analysis was conducted.

### Sentiment by Platform

The sentiment distribution across different social media platforms was analyzed to identify platform-specific sentiment trends.

**Visualization**: A stacked bar chart in Power BI was used to display how sentiment varies across platforms such as Twitter, Facebook, and Instagram.

### Geographical Sentiment Analysis

The sentiment associated with different countries was analyzed to understand regional variations in public perception.

### Engagement Analysis

To understand the impact of sentiment on user engagement, an analysis of Retweets and Likes based on sentiment was conducted.

**Visualization**: A bar chart in Power BI was used to display the average number of retweets and likes for each sentiment, helping to assess which sentiment drives the most engagement.

## Dashboard

This is an interactive dashboard where sentiments were filtered to display the top 10 sentiments based on count. You can view all sentiments using the filters on the left of the dashboard, which also enable you to filter by platforms, country, and date. [Link to dashboard](#).

## Key Insights and Recommendations

The analysis provided several key insights:

- **Overall Sentiment**: The brand/product generally received positive sentiment across most platforms, but there were notable spikes in negative sentiment on certain dates, possibly corresponding to specific events or issues.
- **Platform-Specific Trends**: Twitter showed a higher proportion of negative sentiment compared to other platforms, suggesting a need for targeted reputation management efforts on that platform.
- **Regional Sentiment Variations**: Certain countries exhibited stronger negative sentiment, which may indicate regional issues or challenges that need to be addressed through localized marketing strategies.
- **Engagement Correlation**: Posts with positive sentiment tended to receive higher engagement (more likes and retweets), highlighting the importance of maintaining a positive brand image.

### Recommendations

- **Targeted Engagement**: Focus on engaging more with users on platforms like Twitter where negative sentiment is higher, possibly through customer support or targeted positive messaging.
- **Localized Campaigns**: Develop localized marketing campaigns to address regions where negative sentiment is prevalent, focusing on understanding and resolving specific regional concerns.

## Conclusion

This comprehensive analysis of social media sentiment around the brand/product provided valuable insights into public perception across different platforms and regions. By leveraging these insights, the brand can make informed strategic decisions to enhance its online presence, improve customer satisfaction, and drive positive engagement across social media channels.

The use of SQL for data extraction and Power BI for visualization proved effective in uncovering trends and patterns that are critical for shaping future marketing and reputation management strategies. The visualizations created in Power BI offer an intuitive and interactive way to explore the data and gain actionable insights, making them an essential tool for decision-makers.

## Future Work

Future analysis could involve more advanced text analysis techniques, such as natural language processing (NLP), to gain deeper insights into the specific topics or issues driving sentiment. Additionally, real-time sentiment analysis could be implemented to provide ongoing monitoring and immediate responses to shifts in public perception.

