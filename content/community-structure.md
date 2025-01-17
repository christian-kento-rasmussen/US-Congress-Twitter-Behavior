---
title: Community Structures 
prev: network-structure
next: congressional-communities
---
<!-- Louvain:   
            Confusion matrix
            Community size (power law) (farve efter parti?)
            Evt. statistisk tests
-->

Using the Louvain clustering algorithm, we optimize for modularity score and get a partitioning with a modularity of around 0.35. This is an approximately 36% and 75% percent increase compared to party-chamber and party-party partitioning respectively, indicating that there is a third dimension to the way the congressional communities communicate, beyond party and party-chamber.

In the matrix below, we have compared how the members of the different parties have spread themselves out across the Louvain partitioning. The communities are ranked after member size, the largest being community 0, and the number in each cell is the percentage of total members of the party in the community:

![](/images/Matrix.png) <!-- forket titel skal være "..over parties vs..." chr -->


In the first two communities found by the algorithm, there is a clear division between republicans and democrats, with about 75% of the republicans being in the first community, and about 80% of the democrats being in the second community. In the third and fourth communities, the proportion of republicans to democrats vice versa is also low.

The graph of the network is shown below colored by party partition and Louvain partition in each image.

![](/images/nwlvai.png)
![](/images/nwpartyai.png)

From the Louvain partition graph, we see that most of the colors stay the same, but with separate communities between the chambers. The darker colors represent the House and the lighter shades represent the Senate. The committees and others are captured poorly in the rest of the communities, and most of them are assigned to one of the parties in the corresponding chamber. In the House, a few republicans and democrats are classified as their opposite within Community 0 and 1, as is the case for a few members of the Senate. Overall, the Louvain partition seems to be very neatly divided into the first four communities.

This shows a clear tendency that most democrats and republicans primarily communicate within the party on twitter, and more rarely across the two main parties. Therefore, an argument can be made that the twitter discourse of the two primary parties is heavily polarized. 

## Analysis of the communities splits
To further explore this connection we will try to analyze the communities more closely by looking at the nodes that makes up each community to see if they also are centered around policy issues, or something else. As a proxy measure for this, we will look at the most central node in each community, measured by indegree centrality, and see whether or not it is a caucus or a committee. We use this measure as it seems reasonable that if we have a community heavily centered around eks. the Committee for Climate Change, we assume that the communication in that community is also centered on discussing on climate change. This assumption that the most contral node represent the communities well is based on the fact that our graph follows a power law with regards to edges. Which means that the most central nodes in each community have a majority share of the mentions. However, this may not hold for all communites, as we have only proved it for the full network, and there may therefore be a case of many high-centrality nodes being grouped together in the same community.

<!-- sammensat til en tekst 
If there is a high centrality around non-partisan committees, we assume this to mean, that the communication done in that community are centered around the subject, which the committee is itself centered around. That is, if we have a community heavily centered around the Committee for Climate Change, we assume that the communication in that community is centered on discussing climate change. 

We assume that the most central nodes represent the communities well, as our graph follows a power law with regards to edges. This tells us, that 20% of the nodes have approximately 80% or more of the edges, which should mean that the most central nodes in each community should have a major share of the mentions. However, this may not be true, as our power law is on a network wide-scale, and there may therefore be a case of many high-centrality nodes being grouped together in the same community.
-->

As a way to measure polarization in the different communities we will also employ the measure "partisanship," which is calculated by first finding out how big a percentage of the community is republican and how big a percentage is democratic, and taking the maximum of that. This means, that we have a range of partisanship from [0,1], where 0 indicates that 0% of the members belong to any political party, and 1 indicates that 100% of the members belong to the same party. These measures have been plotted below.


![](/images/LouvainGraf.png) <!-- mangler titel chr -->

When running a single sample of the Louvain algorithm, we see that the smallest communities have a low value of partisanship, showing how they're very much not polarized. And at the same time, the central nodes of these communities have a very high centrality, which indicates, that they're the focus of the communication taking place in those communities. 

Looking at the number of edges inside of these 4 smallest communities, we see however, they're considerably smaller than the top 4 communities; making up only 3.5% of the total edges in the network. They therefore make up a minor part of the modularity calculations, and are therefore most likely not the reason for why we saw such a huge increase in the modularity, when running the Louvain algorithm opposed to simply partitioning among party- or party-chamber lines.

We see that the largest communities, which can be considered the most important with regards to the modularity, have very high partisanship and very low centrality. Under the assumption, that high centrality around a single node is a measure of how much a community's tweets are focused around that person, subject or party. And that partisanship is a true measure for how polarized the communities are. It appears, that despite one of the biggest community's central nodes being a committee, the low centrality of this committee tells us, that it is not the locus of the communication taking place in that community.

Rather, it appears, that the common pattern for the largest communities is, that they're very much polarized.  With the lowest partisanship being around 0.8, meaning that 80% of the third and fourth largest networks' members are part of the same party. While the largest communities, who make up the lion's share of congress members, have a partisanship north of 0.85.

Pertaining to our hypothesis that the increase in modularity - and therefore the quality of communities - was based on the Louvain algorithm creating groupings based on policy-issues, appears to be false. This is due to the fact, that we expected this policy-focus to be manifested in a high centrality around certain policy-focused users, like caucuses or committees which are usually single issue based. Instead we found, that amongst the top 4 communities, which made up approx. 98% of the congress members, only the second largest community was centered around a committee user. But even then, it had a very low centrality, and was therefore most likely not the locus of communication in that community. However nothing definitve can be concluded regarding this, besides our measure of policy-focus not manifesting itself.

So in summation, combined with the previous page, it appears that there is a strong argument to make for the existence of polarization in the US congress. Besides the points from the previous page, we see that republicans and democrats fundamentally engage in different communities. We furthermore cannot conclude anything about whether or not the Louvain algorithm's partitionings having such a higher modularity is based on the communities being centered around policy-issues instead of around party-chamber lines, as the proxy measure we used to measure this did not manifest itself.

To continue our analysis we have chosen the analyze the tweets made in each community on the following page.


<!--
Lorem ipsum dolor sit amet, consectetur adipiscing elit. In nulla tellus, tempus sed lobortis quis, venenatis ac ante. Maecenas accumsan augue ultricies metus hendrerit, in ultrices urna fringilla. Suspendisse lobortis egestas magna, sit amet fermentum ligula tincidunt vitae. Suspendisse cursus non dui a vulputate. Cras vestibulum vulputate enim eu placerat. Ut scelerisque semper justo sit amet auctor. Aliquam sit amet iaculis tortor.

> Nulla in justo hendrerit, tincidunt mauris et, porta est. Donec in leo vitae est ultrices dapibus id nec tortor. Maecenas ut ipsum eu nisl cursus facilisis scelerisque eu ex. Aliquam euismod elementum libero, at vehicula ipsum.

Nam commodo lorem quis tortor euismod, ut ultrices orci aliquet. Sed eget dui nec sem ullamcorper convallis id nec ante. Aliquam ultricies a massa quis semper. Donec suscipit augue ut sagittis hendrerit. Aliquam erat volutpat. Proin aliquet maximus nibh, id aliquet justo maximus at. Sed accumsan ante id aliquam pellentesque. Aliquam nec hendrerit quam. Suspendisse maximus eros sollicitudin, accumsan turpis eu, blandit nulla. Nunc lorem elit, molestie at libero gravida, placerat consectetur ante. Sed tincidunt viverra tellus a vehicula.

Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nam blandit lobortis turpis. Praesent porttitor, turpis eu posuere molestie, sem dolor scelerisque sapien, eu aliquet ante felis ac metus. Pellentesque semper ultricies urna. Aenean auctor, turpis ut convallis ultrices, eros tellus bibendum risus, eu varius velit ante et diam. In suscipit lorem orci, eu placerat nibh dignissim ut. Nullam consequat nisl dui, in ornare risus porttitor sed. Integer vitae nibh semper purus ultrices rutrum. Pellentesque non diam ornare, imperdiet elit a, tempus lacus. Suspendisse viverra euismod dapibus.
-->
