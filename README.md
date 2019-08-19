# Udacity-We-Rate-Dogs

## Tasks

In this Project, we gather data from a variety of sources and in a variety of formats, assess its quality and tidiness, then clean it. We document the wrangling efforts in a Jupyter Notebook, plus showcase them through analyses and visualizations using Python.

## Data Gathering

The dataset that we are wrangling is the tweet archive of Twitter user @dog_rates, also known as WeRateDogs. WeRateDogs is a Twitter account that rates people's dogs with a humorous comment about the dog. 
.
The dataset that we are wrangling (and analyzing and visualizing) is the tweet archive of Twitter user @dog_rates, also known as WeRateDogs. WeRateDogs is a Twitter account that rates people's dogs with a humorous comment about the dog.

   * Twitter archive file: the twitter_archive_enhanced.csv was provided by Udacity and downloaded manually.

   * The Tweet image predictions: i.e. what breed of is present i each tweet according to a neural network. The file is hosted on Udacity's servers and was downloaded programmatically using the Requests library and URL information.

   * Tweeter API & Json: by using the tweet IDs in the WeRateDogs twitter acchieve, I queries the Twitter API for each tweet's Json data using Python's Tweepy library and converted each tweet's partial data into dataframe with tweet ID,favorite count, retweet count,text and favorite_count.

## Assessing data
Once the three tables were obtained I assessed the data as following:
      -- **Visually** I read three dataframes in Jupyter Notebook one by one.
      -- **Programmatically**  by using bunch of methods(e.g. info, value_count, duplicated, describe, etc) 

Then I seperated the issues encountered in quality issues and tidiness issues.

## Clean data
This part of the data wrangling was devided in three parts: Define, code and check. These three steps were on each of the issues described in the assess section.

First and very helpful step was to created a copy of the three original dataframes. I wrote the codes to manipulate the copies. if there was an error, I could create a new copy from the original.

Whenever I made a mistake, I could create another copy of the dataframes and continue working on the cleaning part.

I combine four dog status(doggo,floofer,pupper,puppo) in one colume, correct the wrong rating data manually, find the most likely dog type and picture confidence, convert data type to an appropriate form,etc

at last we conbined three clean dataframe into one dataset and save the dataset as csv file"twitter_archive_master.csv"

## Insight
### Insight one: Most common dog type
From around 2000 tweets, we can find the most rated dogs was golden retriever with 157 ratings, way higher than average ratings 11.59, followed by labrador retriever(108 ratings) and Pembroke (95 ratings)

### Insight two: Retweets and favorites with time
All tweets are created from Nov 2015 to Sep 2019, we can see count of retweets and favorites increase gradually by time. favorites increase more significantly than retweets.

### Insight three: Rating and Retweet
The tweet got the highest rating is # 975 tweet which got 177.6 rating. We explore the relation of rating and retweet and find that there is no correlation between rating and retweets. It can be because the dogs are not actually getting better. It can be that 'lower quality' dogs are given funnier captions. In this case, it is the caption that is getting more retweets rather than the dog itself.
