---
title: Network Structure
prev: data-description
next: community-structure
---

<!-- 
Specifically, we start off by investigating the relationship between democrats and republicans to establish, whether our big community (the U.S congress) can in fact be divided into seperate communities based on political affiliation. We do this by looking at the modularity of dividing the users into communities based on political affiliation using the Louvain algorithm. We also look at the assortativity between the different political affiliation. [Network-structure](network-structure)
-->

We want to start by investigating the network structure. Specifically, we want to investigate the mixing patterns based on parties. As a starting point, we compute the fraction of out edges that connects to users with the same party affiliation. We then shuffle the members party affiliation 100 times and plot the distribuition as a histogram together with the actual fraction from the data. The results are shown in the figure below. 

![](/images/histogram-frac-edges-party.png)

<!-- t-test virker  -> implications -->
By performing a permutation test, we get a p-value that is far below 0.05. This means that we can conclude on a 0.05 significant level that the chance that a tweet mentions a user with the same party affiliation is statistically significantly higher than it would be by chance. This supports the belive that members of the U.S congress are more likely to messsage eachother internally in each party.
 
<!-- Vi regner assortativity coefficient with respect to party, det har også implications -->
To further investiage this, we compute the assortativity coefficient with respect to party for Republicans, Democrats, and Independents. The edge count is shown in the confusion matrix below. This results in an assortativity coefficient of 0.65. 
This high party affiliation assortivity coefficient implies some social polarization based on party.
When doing this analysis it is important to mention that not all mentions/edges are communication betwee user, but some are simply members tagging or promoting other members campaigns. These have been included but arguments can be made for excluding them as they do not represent active conversation.

<!-- Vi kigger nu på community party-party wise -->
If we partition our network into 4 groups based on party affiliation, that is, a community for republicans, democrats, independents and non-alligned, we get a modularity of 0.2. This is a moderate number, and it indicates, that there might be better ways to partition the Congress than purely along party lines.

Specifically, if we take a look at our graph, we see what appears to be four distinct communities along both party as well as chamber lines. 
<

Partitioning our graph along party-chamber lines, we get a modularity of 0.25.

Both numbers are statistically different from 0, indicating, that there might be some truth to the idea, that Republicans and Democrats are polarized around party lines. At the very least, it indicates, that the amount of intra-party clustering the respective parties' chambers do is non-random, and that there therefor is some degree of polarization. 

However, due to the moderate value of our modularity, it is evident, that there are better clusterings than simply party-party or party-chamber.

If we look at our assortativity, we furthermore get an indication of polarization among congressmember. We have an assortativity around party-lines above 0.6, clearly indicating, that there is a higher probability of congress members to communicate with their own party-peers than with those of the opposite party.

However, as can be seen from the assortativity matrix, it isn't completely divided; We see a moderate level of cross-party communication. 

Taking both of these statistics in combination, we get an indication, that there is some level of polarization in the U.S congress. We see this in the way, that we get a modularity significantly different from 0 when we divide our graph into party-party or party-chamber, and through the high level of party-party assortavitiy. On the other hand, this polarization isn't complete; Our modularity when dividng along party lines is still moderate, and we see from the assortativity matrix, that there clearly occurs cross-party communication.

This indicates to us, that there are more complex mechanisms at play, that can describe the way that the two major parties in the U.S congress organize themselves. We suspect, that the best community partitions are centered around subjects and commitees, that is, they're centered around political issues rather than political parties.

This follows the logic, that republicans tend to communicate more with republicans, not because they're republicans. But rather, because they care about and therefore work with the same issues, which is the reason for why they're both republican to begin with. And vise versa for democrats. This might also explain why we do not have a complete polarization, as democrats and republicans that care about the same issues will most likely communicate with one another.

We will explore this on the next page, where we will use the Louvain algorithm to find the optimal community partitioning. We will explore these partitionings for signs of polarization around party lines, and from there we will investigate, what may be the "center" for these partitionings.


 


![](/images/matrixe.png)













<!--- 
Lorem ipsum dolor sit amet, consectetur adipiscing elit. In nulla tellus, tempus sed lobortis quis, venenatis ac ante. Maecenas accumsan augue ultricies metus hendrerit, in ultrices urna fringilla. Suspendisse lobortis egestas magna, sit amet fermentum ligula tincidunt vitae. Suspendisse cursus non dui a vulputate. Cras vestibulum vulputate enim eu placerat. Ut scelerisque semper justo sit amet auctor. Aliquam sit amet iaculis tortor.

> Nulla in justo hendrerit, tincidunt mauris et, porta est. Donec in leo vitae est ultrices dapibus id nec tortor. Maecenas ut ipsum eu nisl cursus facilisis scelerisque eu ex. Aliquam euismod elementum libero, at vehicula ipsum.

Nam commodo lorem quis tortor euismod, ut ultrices orci aliquet. Sed eget dui nec sem ullamcorper convallis id nec ante. Aliquam ultricies a massa quis semper. Donec suscipit augue ut sagittis hendrerit. Aliquam erat volutpat. Proin aliquet maximus nibh, id aliquet justo maximus at. Sed accumsan ante id aliquam pellentesque. Aliquam nec hendrerit quam. Suspendisse maximus eros sollicitudin, accumsan turpis eu, blandit nulla. Nunc lorem elit, molestie at libero gravida, placerat consectetur ante. Sed tincidunt viverra tellus a vehicula.

Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nam blandit lobortis turpis. Praesent porttitor, turpis eu posuere molestie, sem dolor scelerisque sapien, eu aliquet ante felis ac metus. Pellentesque semper ultricies urna. Aenean auctor, turpis ut convallis ultrices, eros tellus bibendum risus, eu varius velit ante et diam. In suscipit lorem orci, eu placerat nibh dignissim ut. Nullam consequat nisl dui, in ornare risus porttitor sed. Integer vitae nibh semper purus ultrices rutrum. Pellentesque non diam ornare, imperdiet elit a, tempus lacus. Suspendisse viverra euismod dapibus.
--->
