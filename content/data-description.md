---
title: Data description
prev: "/"
next: network-structure
---

To perform this analysis we need to collect tweets from member of the United States Congress. An ideal way to do this, would be to call the twitter api and request tweets in a specific time period with hastags or accounts names that mathces with member of the congress. However, this approach is not feasible after Twitter has changed their policy when Mr. Musk accouired the company. Therefore, we have used the public available dataset of US Congress tweets hosted on [github](https://github.com/alexlitel/congresstweets) and part of the open source project [Congressional Tweet Automator](https://github.com/alexlitel/congresstweets-automator).

The raw data consist of 2.6GB of json files with tweets from 2017 up to and including 2023. The data is structured in a way that each json file contains tweets from a specific month and year. An example of a raw tweet is shown below.

```
{
    "id":"879411283275153408",
    "screen_name":"RosLehtinen",
    "time":"2017-06-26T14:49:23-04:00",
    "link":
        "https://www.twitter.com/RosLehtinen/statuses/87
        9411283275153408",
    "text":
        "With my hubby Dex accepting @Rotary Club award! 
        Their core values &amp; philanthropic mission 
        strive to improve our #SoFla cmnty! 
        @EugeneFlinn https://t.co/hxWKhoZR9z",
    "source":"Twitter Web Client",
    "user_id":"14275291"
}
```

This data has then been parsed into 4 differnet dataframes. Which is used to construct a single directed multigraph where nodes are users and edges are each time a user mentions ('@name_of_mention') another user in a tweet. The graph and dataframe have also been filted based on tweet year for later analysis.

We also had a JSON file called [historical users](https://github.com/alexlitel/congresstweets-automator/blob/master/data/historical-users-filtered.json) consisting of data on the different twitter users. It contained the name of the user, which chamber they were a part of, their political affiliation, what type of user they were (comittee, political party, member or caucus) and a list of which twitter accounts were associated with that user. Furthermore, if the user was a member of congress they would also have a field explaining which state they represented. 

# The four dataframes and graph are:

## 1. Users dataframe:

The main purpose of the user dataframe is to gather data on the real life organizations or humans who use the twitter accounts.

Each user represents a person or organization related to the U.S congress, who may have multiple Twitter accounts and whom is a part of the historical users JSON file. Each row in our users dataframe has the following information:
* The user's name, which we use as a unique identifier, as no members of congress in our dataset have the same name.
* Which house they're part of (representatives or senate)
* Their type, that is, wheter the user is a commitee, a member (human), party or caucus
* Their political party, if any
* Which U.S state they represent, if any

Size: 806

## 2. Accounts dataframe:

As each user can have multiple Twitter accounts, we needed a dataframe to link between accounts and the real life organization/person that uses these whenever, we wanted to figure out who had tweeted something, and at whom.

Each row in our accounts data is a single account, and consists of the following data:
* ID: the ID of that specific account
* screen_name: the name of that specific account
* account_type: whether it is an office or campaign account
* name: the name of the user behind the account

Size: 1754


## 3. Tweets dataframe:

The tweets dataframe consists of all the tweets information. The primary purpose of this dataframe was to provide an organized way to do text analysis. It has a size of 4777249 entries

Each row is a single tweet with the following information:
* user_name: The username of the user behind the tweet
* screen_name: The name of the account from which the tweet was posted
* tweet_account_ID: The ID of that account
* tweet_ID: The unique identifier identifying that single tweet
* handles_mentioned: All the twitter handles mentioned, which are in our account dataframe.
* names_mentioned: The username of the accounts mentioned.


## 4. text dataframe:

The text dataframe consists of all the text of every tweet in the tweets dataframe. This should be used together with the tweets dataframe. It has a size of 4777249 entries

Each row is a single tweet with the following information:
* user_name: The username of the user behind the tweet
* screen_name: The name of the account from which the tweet was posted
* text: The actual text of that tweet
* tweet_ID: The unique identifier identifying that single tweet

## 4. Multidirected graph:

The multidirectional graph was created by making each user a node and each time a user mentions another user in a tweet an edge. The graph is directed as the order of the mention is important. The graph is multidirectional as there often are multiple tweets between users. We choose to make it multidirectional because we wanted to keep the information that each individual tweet contains instead of just counting the number of tweets between users.

The graph contains 803 nodes and 1,602,970 edges. The distribution of degree of edges is shown below.

![](/images/degree-distribution.png)

From the graph we can see that the distribution of degree of edges is very skewed. This means that there are a few nodes with a very high degree and a lot of nodes with a very low degree. This is expected as there are a few users who are very active on twitter and a lot of users who are not. When plotting the distribution on a log-log scale we can see that the distribution looks to loosely follow a power law. With parameters:$$C=0.002, \gamma=1.182$$.


<!--- 

## How we have created our dataset

this was done

Lorem ipsum dolor sit amet, consectetur adipiscing elit. In nulla tellus, tempus sed lobortis quis, venenatis ac ante. Maecenas accumsan augue ultricies metus hendrerit, in ultrices urna fringilla. Suspendisse lobortis egestas magna, sit amet fermentum ligula tincidunt vitae. Suspendisse cursus non dui a vulputate. Cras vestibulum vulputate enim eu placerat. Ut scelerisque semper justo sit amet auctor. Aliquam sit amet iaculis tortor.

> Nulla in justo hendrerit, tincidunt mauris et, porta est. Donec in leo vitae est ultrices dapibus id nec tortor. Maecenas ut ipsum eu nisl cursus facilisis scelerisque eu ex. Aliquam euismod elementum libero, at vehicula ipsum.

Nam commodo lorem quis tortor euismod, ut ultrices orci aliquet. Sed eget dui nec sem ullamcorper convallis id nec ante. Aliquam ultricies a massa quis semper. Donec suscipit augue ut sagittis hendrerit. Aliquam erat volutpat. Proin aliquet maximus nibh, id aliquet justo maximus at. Sed accumsan ante id aliquam pellentesque. 

![](/images/dtu-logo.png)

Aliquam nec hendrerit quam. Suspendisse maximus eros sollicitudin, accumsan turpis eu, blandit nulla. Nunc lorem elit, molestie at libero gravida, placerat consectetur ante. Sed tincidunt viverra tellus a vehicula.


1. Lorem ipsum dolor sit amet
1. Lorem ipsum dolor sit amet
1. Lorem ipsum dolor sit amet

Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nam blandit lobortis turpis. Praesent porttitor, turpis eu posuere molestie, sem dolor scelerisque sapien, eu aliquet ante felis ac metus. Pellentesque semper ultricies urna. Aenean auctor, turpis ut convallis ultrices, eros tellus bibendum risus, eu varius velit ante et diam. 

* Lorem ipsum dolor sit amet
* Lorem ipsum dolor sit amet
* Lorem ipsum dolor sit amet

In suscipit lorem orci, eu placerat nibh dignissim ut. Nullam consequat nisl dui, in ornare risus porttitor sed. Integer vitae nibh semper purus ultrices rutrum. Pellentesque non diam ornare, imperdiet elit a, tempus lacus. Suspendisse viverra euismod dapibus.

Suspendisse non tellus faucibus, dapibus leo at, elementum magna. Fusce quis ante ex. In non ex eleifend, luctus risus quis, dapibus velit. Nulla facilisi. Integer iaculis arcu at fermentum varius. Donec auctor dolor non dolor pulvinar luctus. Mauris vestibulum lacinia nisl, a dictum erat molestie sed. Vivamus vel blandit turpis, nec sollicitudin massa. Nunc velit eros, tristique elementum congue eget, auctor dictum tellus. 

Quisque iaculis, sem quis imperdiet faucibus, nunc lorem feugiat purus, vestibulum condimentum turpis turpis ut ante. Donec vestibulum lectus ut ullamcorper condimentum. Curabitur fermentum nulla vitae arcu sollicitudin pulvinar.

<img src="/images/dtu-logo.png" width="200" />

Vestibulum ante ipsum primis in faucibus orci luctus et ultrices posuere cubilia curae; Suspendisse eu tellus ut erat porttitor luctus. Vivamus aliquam auctor massa, in auctor orci. Ut quis enim ut lorem consectetur blandit dictum eu mauris.
--->
