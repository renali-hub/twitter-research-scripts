Twitter Scrape Script

Description:
The notebook first searches for tweets within a set time frame that contain 
within it's text a specified keyword or phrase. Using the returned URLs, the
Tweet ID (unique to each posted tweet) is extracted from the URL and used to
pull the API data of those tweets. Within the API data includes the data points
"in_reply_to_user_id" and "referenced_tweets" to determine the Tweet IDs of 
tweets that were replied to or quoted. We then recursively traverse up the 
Twitter conversation, pulling API data for more tweets, until we hit the 
original tweet. Since the Twitter API only allows a maximum of 100 pull 
requests, each "level" of traversing needs to be split into groups of 100 Tweet
IDs. After all the data is pulled, the notebook merges the groups of 100 tweets
for one level into one file, which is then merged into one file. Users are thus 
able to create robust and comprehensive Twitter data sets using this notebook.

TL;DR:
A Jupyter Notebook that allows for a user to search for tweets using key words
and phrases, and pulls API data of those tweets all of their referenced tweets.
This allows the user to pull tweets containing specific keywords and phrases,
and all the tweets they reference (ie. reply to, quote). 


How To Use:
- Requires Twitter API Access 
- Download .ipynb file
- Complete TODOs
- Run notebook



Log:
- July 20, 2022 (v1)