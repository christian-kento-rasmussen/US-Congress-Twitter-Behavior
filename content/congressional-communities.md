---
title: Community Structures Text Analysis
prev: "community-structure"
next: evolving-dynamics
---

<!-- 
om here we would like to see, what underlying structures, if not political party, that binds the different communities together. Is it a special commitee that they talk a lot about, a law or a maybe a more general topic like foreign policy or welfare? We do this by doing text analysis on the biggest communities to see which keywords that describe them best. We would furthermore also like to do some wordclouds on these communities. [Congressional-communities](congressional-communities)
-->
After finding some appropriate communities, we want to explore what underlying structure that represents them. We do this, by looking at at the tweets that originates from users in a community.



## TF-IDF

TF:
| Partition | Top 10 Tokens |
| --- | --- |
| 0 | act, house, bill, congress, people, proud, american, work, health, need |
| 1 | house, american, democrats, act, bill, americans, biden, congress, people, border |
| 2 | senate, bill, act, american, bipartisan, support, help, americans, work, democrats |
| 3 | senate, act, bill, health, help, care, need, bipartisan, people, americans |
| 4 | people, house, chairman, act, support, statement, president, security, american, foreign |
| 5 | budget, chair, senate, bill, tax, process, spending, federal, committee, hearing |


TF-IDF
| Partition | Top 10 TF-IDF |
| --- | --- |
| 0 | rep, democracy, safe, caucus, police, de, impeachment, protections, abortion, hate |
| 1 | rep, impeachment, safe, police, caucus, schiff, fentanyl, abortion, parents, texas |
| 2 | safe, iowa, hatch, kansas, arkansas, north, tennessee, georgia, dakota, police |
| 3 | mcconnell, nevada, democracy, protections, safe, conditions, georgia, preexisting, abortion, judiciary |
| 4 | rm, chm, democracy, allies, partners, ccp, chinese, humanitarian, hong, attack |
| 5 | wyoming, dnd, nazilinked, duplication, gregg, outlook, laramie, cbos, deliberating, wyomings |

Top accounts
| Partition | Top 3 accounts |
| --- | --- |
| 0 | House Democrats, House Committee on the Judiciary, Hispanic Caucus |
| 1 | House Republicans, House Committee on Energy and Commerce, House Committee on Ways and Means |
| 2 | Senate Republicans, John Cornyn, Ted Cruz |
| 3 | Senate Democrats, Chuck Schumer, Dick Durbin |
| 4 | House Committee on Foreign Affairs, Michael McCaul, Gregory Meeks |

## Word clouds 
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