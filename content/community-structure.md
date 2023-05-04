---
title: Community Structures ??
prev: network-structure
next: congressional-communities
---
+forord

<!-- Louvain:   
            Confusion matrix
            Community size (power law) (farve efter parti?)
            Evt. statistisk tests
-->

Using the Louvain clustering algorithm, we optimize for modularity score and get a partitioning with a modularity of 0.35. The Louvain partitioning is compared with the partitioning by party in a confusion matrix below. With the Louvain partitioning, we get an approximately 36% and 75% percent increase compared to party-chamber and party-party partioning respectively, indicating that there indeed is a third dimension to the way the congressial communities organize themselves, beyond party and party-chamber.

![](/images/confmatrixlouvain.png)

However, regarding polarization, we see taht in the first two communities found by the algorithm, there is a clear division between republicans and democrats, with about 80% of the democrats and 10% of the republicans in the first community, and about 70% of the republicans and 2% of the democrats in the second community. In the third and fourth communities, the proportion of republicans to democrats vice versa is also low.

It appears, that our optimal partitioning still generates polarization, which is a strong indicator for the fact, that there is polarization within the US congress. We see this in the way, that the different communities are divided so heavily along party line. We will now investigate, whether or not the different communities are centered around policy issues. As a proxy measure for this, we will look at the most central node in each community, measured by indegree centrality, and see whether or not it is a caucus or a committee.

We assume that the most central nodes represent the communities well, as our graph follows a power law with regards to edges. This tells us, that 20% of the nodes have approximately 80% or more of the edges, which should mean that the most central nodes in each community should have a major share of the mentions. However, this may not be true, as our power law is on a network wide-scale, and this property may therefore not transfer down to our modelling of the communities, especially when our communities have such a relatively low modularity.

As a way to measure polarization in the different communities we will also employ the measure "partisanship," which is calculated by first finding out how big a percentage of the community is republican and how big a percentage is democratic, and taking the maximum of that. This means, that we have a range of partisanship from [0,1], where 0 indicates that 0% of the members belong to any political party, and 1 indicates that 100% of the members belong to the same party.


<!-- ^Mangler lige at poste mein graf her -->

When running a single sample of the Louvain algorithm, we see, that the smallest communities have none to negative partisanship, showing how they're very much not polarized. And at the same time, the central nodes of these communities have a very high centrality, which indicates, that they're the focus of the communication taking place in those communities. 

Looking at the number of edges inside of these 4 smallest networks, we see however, they're considerably smaller than the top 4 communities; Making up only 3.5% of the total edges in the network. They therefore make up a minor part of the modularity calculations, and are therefore most likely not the reason for why we saw such a huge increase in the modularity, when running the Louvain algorithm opposed to simply partitioning among party- or party-chamber lines.

We see that these communities, which can be considered the most important with regards to the modularity, have very high partisanship and very low centrality. Under the assumption, that high centrality around a single node is a measure of how much a community's tweets are focused around that person, subject or party. And that partisanship is a true measure for how polarized the communities are. It appears, that despite one of the biggest community's central nodes being a committee, the low centrality of this committee tells us, that it is not the locus of the communication taking place in that community.

Rather, it appears, that the common pattern for the largest communities is, that they're very much polarized.  With the lowest partisanship being around 0.8, meaning that 80% of the third and fourth largest networks' members are part of the same party. While the largest communities, who make up the lion's share of congress members, have a partisanship north of 0.85.

So in summation, combined with the previous page, it appears that there is a strong argument to make for the existence of polarization in the US congress. Besides the points from the previous page, we see that republicans and democrats fundamentally engage in different communities. 

Furthermore, as another argument for the existence of polarization; We cannot say anything with regards to our hypothesis, that the communities are centered around political issues, since we expected these political issues to manifest in commitees and caucuses having central places in the communities formed by the Louvain algorithm. When we investigate the most central node in all of these communities in order to determinte, whether the increase in modularity relatively between our party-chamber,party and Louvain based partitionings are based on the fact, that the Louvain algorithm centers its communities around policy issues and not necessarily political party. We're met with the fact, that for the largest communities, there is such a low centrality for the community's most central node, that even when the community's most central node is a committee, it has such a low centrality, that it cannot be considered the locus of communication for that network. This says a lot, considering our community's distribution of edges follows a power law. And at the same time, they have very high partisanship. 

<!-- ^Skal lige omskrives, når kl ikke er 03 om morgenen, lol -->


Based on all of these factors, we've decided to investigate the communities through text analysis, rather than community measures, to get a better understanding of what binds these communities together.



<!--  -->



<!--
Lorem ipsum dolor sit amet, consectetur adipiscing elit. In nulla tellus, tempus sed lobortis quis, venenatis ac ante. Maecenas accumsan augue ultricies metus hendrerit, in ultrices urna fringilla. Suspendisse lobortis egestas magna, sit amet fermentum ligula tincidunt vitae. Suspendisse cursus non dui a vulputate. Cras vestibulum vulputate enim eu placerat. Ut scelerisque semper justo sit amet auctor. Aliquam sit amet iaculis tortor.

> Nulla in justo hendrerit, tincidunt mauris et, porta est. Donec in leo vitae est ultrices dapibus id nec tortor. Maecenas ut ipsum eu nisl cursus facilisis scelerisque eu ex. Aliquam euismod elementum libero, at vehicula ipsum.

Nam commodo lorem quis tortor euismod, ut ultrices orci aliquet. Sed eget dui nec sem ullamcorper convallis id nec ante. Aliquam ultricies a massa quis semper. Donec suscipit augue ut sagittis hendrerit. Aliquam erat volutpat. Proin aliquet maximus nibh, id aliquet justo maximus at. Sed accumsan ante id aliquam pellentesque. Aliquam nec hendrerit quam. Suspendisse maximus eros sollicitudin, accumsan turpis eu, blandit nulla. Nunc lorem elit, molestie at libero gravida, placerat consectetur ante. Sed tincidunt viverra tellus a vehicula.

Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nam blandit lobortis turpis. Praesent porttitor, turpis eu posuere molestie, sem dolor scelerisque sapien, eu aliquet ante felis ac metus. Pellentesque semper ultricies urna. Aenean auctor, turpis ut convallis ultrices, eros tellus bibendum risus, eu varius velit ante et diam. In suscipit lorem orci, eu placerat nibh dignissim ut. Nullam consequat nisl dui, in ornare risus porttitor sed. Integer vitae nibh semper purus ultrices rutrum. Pellentesque non diam ornare, imperdiet elit a, tempus lacus. Suspendisse viverra euismod dapibus.
-->
