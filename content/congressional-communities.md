---
title: Community Structures Text Analysis
prev: "community-structure"
next: evolving-dynamics
---

<!-- 
om here we would like to see, what underlying structures, if not political party, that binds the different communities together. Is it a special commitee that they talk a lot about, a law or a maybe a more general topic like foreign policy or welfare? We do this by doing text analysis on the biggest communities to see which keywords that describe them best. We would furthermore also like to do some wordclouds on these communities. [Congressional-communities](congressional-communities)
-->

We now want to analyse the tweets in each community to better understand the underlying structure of the communities. As a starting point for this analysis we will calculate the term frequency of each of the top 6 communities (based on number of nodes). The top 10 tokens for each community is shown in the table below.

| Partition | Top 10 Tokens |
| --- | --- |
| 0 | house, american, democrats, act, bill, americans, biden, congress, people, border |
| 1 | act, house, congress, bill, people, proud, health, work, american, need |
| 2 | senate, bill, act, american, bipartisan, support, help, americans, work, democrats |
| 3 | senate, act, bill, health, help, care, need, bipartisan, people, americans |
| 4 | act, research, science, bill, read, american, hearing, energy, house, committee |
| 5 | people, house, act, chairman, support, statement, president, security, american, foreign |

We can see that the communities are quite similar in terms of the most frequent tokens. This is not surprising as we can see that the most frequent tokens are related to the political process, such as bills, acts, senate, house, and congress. Furthermore, we can see that the communities are also related to the political parties, as the tokens democrats and republicans are present in the top 10 tokens for all communities. 
We already know from the confusion matrix of ??? on page ??? that partition 0 and 2 are mostly republicans and 1 and 3 are mostly democrats. This is also supported when looking at the top 3 accounts for each community. Where 0 and 2 are House and senate republicans and 1 and 3 are house and senate democrats.

| Partition | Top 3 accounts |
| --- | --- |
| 0 | House Republicans, House Committee on Energy and Commerce, House Committee on Ways and Means |
| 1 | House Democrats, House Committee on the Judiciary, Hispanic Caucus |
| 2 | Senate Republicans, John Cornyn, Ted Cruz |
| 3 | Senate Democrats, Chuck Schumer, Dick Durbin |
| 4 | House Committee on Science Space and Technology, Eddie Bernice Johnson, Frank Lucas |
| 5 | House Committee on Foreign Affairs, Michael McCaul, Gregory Meeks |

To get a better understanding of the difference between the communities we will now calculate the TF-IDF for each community. As the TF-IDF measure is is weighted by the inverse document frequency, it will give a higher weight to tokens that are more unique to each community. The top 10 TF-IDF tokens for each community is shown in the table below, and in the wordcloud.

| Partition | Top 10 TF-IDF |
| --- | --- |
| 0 | joe, schiff, mandate, adam, ec, farm, sham, defund, censure, infanticide |
| 1 | student, immigrant, progressive, citizenship, hall, weapons, sisters, para, los, cpc |
| 2 | rubio, joe, hatch, tennessee, georgia, farm, idaho, hawley, iowans, iowas |
| 3 | georgia, nevadans, nevada, student, stock, jackson, nh, nominees, doug, hampshire |
| 4 | oklahomas, telescope, oklahoma, rubin, researchers, quantum, icorps, possibleeven, necessaryto, telescopes |
| 5 | ametamct, ambassador, diplomacy, terrorist, weapons, regimes, syria, iranian, africa, gratitudeand |

From the above table and the wordcloud below, we can see that some of the top words for community 0 are "joe" and "defund" which are part of the words for "Joe Biden" and "Defund the police". Which means that this community has talked vocally about these subjects. This is of couse true for the republicans as they have especially used the "Defund the police" movement as a way to discredit democrats in past elections.
We can also see that the two big democratic communities (1 and 3) have words such as student, progressive, and weapons. Which are some of the democratic parties main issuies.

Community 5 looks to be centered around foreigh affairs as they top words are "syria", "iranian", and "africa" and they top 3 accounts are the committe and two congressmen from the committe. In future analysis, it could be interesting to look at the other nodes in the network to see what other political apponties are with in this committe, as they probably also have a vested interest in foreign affairs.

![](/images/wordcloud.png)


<!--
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
-->