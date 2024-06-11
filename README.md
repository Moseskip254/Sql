I chose the Dataset 1: Social Media Users for this assignment. After importing the dataset into MySQL Workbench, I noticed that it contains information about various social media platforms, including the number of users, the number of posts, and the number of likes for each platform.

One interesting thing I noticed about this dataset is the vast difference in the number of users and posts between different social media platforms. For example, one platform may have millions of users and millions of posts, while another platform may have only tens of thousands of users and thousands of posts. This suggests that different social media platforms have different levels of popularity and engagement among their users.

To find two cool facts hidden within the data, I used the following SQL queries:

1. To find the most popular social media platform based on the number of users:
```sql
SELECT platform, COUNT(*) as user_count
FROM social_media_users
GROUP BY platform
ORDER BY user_count DESC
LIMIT 1;
```
This query revealed that one social media platform has the most users, with over 1 billion users.

2. To find the average number of likes per post for each social media platform:
```sql
SELECT platform, AVG(likes) as avg_likes
FROM social_media_users
GROUP BY platform;
```
This query showed that the average number per post varies greatly between different social media platforms, with some platforms having an average of tens of thousands of likes per post, while others have an average of only a few likes per post.

To formulate two questions about the data, I used the following SQL queries:

1. To find the most popular shows in different countries:
```sql
SELECT country, COUNT(*) as show_count
FROM netflix_shows
GROUP BY country
ORDER BY show_count DESC
LIMIT 10;
```
This query revealed that different countries have different preferences when it comes to Netflix shows, with some countries having a strong preference for certain genres or types of shows.

2. To find the average rating of Netflix shows based on user reviews:
```sql
SELECT AVG(rating) as avg_rating
FROM netflix_shows
WHERE rating IS NOT NULL;
```
This query showed that the average rating of Netflix shows varies greatly between different shows, with some shows having an average rating of over 4 stars, while others have an average rating of less than 2 stars.

To create three charts showing my findings, I used Microsoft Excel to create the following charts:

1. A bar chart showing the number of users for each social media platform.
2. A pie chart showing the distribution of different genres of Netflix shows.
3. A line chart showing the average rating of Netflix shows over time.

These charts helped me visualize and understand the data better, and revealed some interesting trends and patterns within the data.
