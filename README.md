# US Congress Twitter Behavior

<!---  
    Background på US congress  
--->

The United States Congress is the the legislature of the United States Government [[1]](https://en.wikipedia.org/wiki/United_States_Congress). It is responsible for creating and ractifying exisitnig laws. It is composed of two chambers the senate with 100 elected officials and the house with 435 elected officials giving a total of 534. All members of both houses are elected by the public which means that they all need to have good public relations. This is where social media comes into play. Social media is a great way to reach out to the public and show what they are doing and why voters should vote for them over the competition.

<!---  
    Hvad vi gerne vil undersøge
--->

## In this report, we want to explore how the US Congress communicates on twitter.

To view the report, click [**here to go to website**](https://christian-kento-rasmussen.github.io/US-Congress-Twitter-Behavior)

It seems like there is a lot of talk about polarization in US politics between democrats and republicans in the news. We would like to explore whether this polarization exists in reality, that is, do democrats and republicans actually never cooperate, or this just an image potrayed by the media?
As a proxy measurement for this, we've decided to look at twitter exchanges between members of the U.S congress and organization related to these in order to look for patterns that may tell us, how the U.S congress communciates. Our data consists of tweets made by members of congress, governmental organization and caucuses from 2017-2023 plus data like political affiliation and region of the different political users. [Dataset](data-description)

Specifically, we start off by investigating the relationship between democrats and republicans to establish, whether our big community (the U.S congress) can in fact be divided into seperate communities based on political affiliation. We do this by looking at the modularity of dividing the users into communities based on political affiliation using the Louvain algorithm. We also look at the assortativity between the different political affiliation. 

Should our hypothesis, that the U.S congress is polarized not undoubtadly hold, we would like to investiage what relations that actually best describe the way the U.S congress communicates and organizes itself. We do this by dividing the different Twitter users into communities with the help of the Louvain algorithm. From here, we look to see if the modularity increases, that is, do we get a better community partitioning.

From here we would like to see, what underlying structures, if not political party, that binds the different communities together. Is it a special commitee that they talk a lot about, a law or a maybe a more general topic like foreign policy or welfare? We do this by doing text analysis on the biggest communities to see which keywords that describe them best. We would furthermore also like to do some wordclouds on these communities. 

Finally, we would like to see, how the relationship between democrats and republicans has changed over the years. We do this by looking at the democrat-republican modularity and associativity throughout the years. We also look at what has changed in the two parties' talking points by doing TF-IDF on the two parties' corpuses throughout the years.

