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

![](/images/matrixe.png)













<!--- 
Lorem ipsum dolor sit amet, consectetur adipiscing elit. In nulla tellus, tempus sed lobortis quis, venenatis ac ante. Maecenas accumsan augue ultricies metus hendrerit, in ultrices urna fringilla. Suspendisse lobortis egestas magna, sit amet fermentum ligula tincidunt vitae. Suspendisse cursus non dui a vulputate. Cras vestibulum vulputate enim eu placerat. Ut scelerisque semper justo sit amet auctor. Aliquam sit amet iaculis tortor.

> Nulla in justo hendrerit, tincidunt mauris et, porta est. Donec in leo vitae est ultrices dapibus id nec tortor. Maecenas ut ipsum eu nisl cursus facilisis scelerisque eu ex. Aliquam euismod elementum libero, at vehicula ipsum.

Nam commodo lorem quis tortor euismod, ut ultrices orci aliquet. Sed eget dui nec sem ullamcorper convallis id nec ante. Aliquam ultricies a massa quis semper. Donec suscipit augue ut sagittis hendrerit. Aliquam erat volutpat. Proin aliquet maximus nibh, id aliquet justo maximus at. Sed accumsan ante id aliquam pellentesque. Aliquam nec hendrerit quam. Suspendisse maximus eros sollicitudin, accumsan turpis eu, blandit nulla. Nunc lorem elit, molestie at libero gravida, placerat consectetur ante. Sed tincidunt viverra tellus a vehicula.

Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nam blandit lobortis turpis. Praesent porttitor, turpis eu posuere molestie, sem dolor scelerisque sapien, eu aliquet ante felis ac metus. Pellentesque semper ultricies urna. Aenean auctor, turpis ut convallis ultrices, eros tellus bibendum risus, eu varius velit ante et diam. In suscipit lorem orci, eu placerat nibh dignissim ut. Nullam consequat nisl dui, in ornare risus porttitor sed. Integer vitae nibh semper purus ultrices rutrum. Pellentesque non diam ornare, imperdiet elit a, tempus lacus. Suspendisse viverra euismod dapibus.
--->