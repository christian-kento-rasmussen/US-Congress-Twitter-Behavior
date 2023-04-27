---
title: US Congress communication on Twitter
layout: single
next: data-description
---


<!---  
    Background på US congress  
--->

The United States Congress is the the legislature of the United States Government [[1]](https://en.wikipedia.org/wiki/United_States_Congress). It is responsible for creating and ractifying exisitnig laws. It is composed of two chambers the senate with 100 elected officials and the house with 435 elected officials giving a total of 534. All members of both houses are elected by the public which means that they all need to have good public relations. This is where social media comes into play. Social media is a great way to reach out to the public and show what they are doing and why voters should vote for them over the competition.

<!---  
    Hvad vi gerne vil undersøge
--->

# In this report, we want to explore how the US Congress communicates on twitter.

It seems like there is a lot of talk about polarization in US politics between democrats and republicans in the news. We would like to explore whether this polarization exists in reality, that is, do democrats and republicans actually never cooperate, or this just an image potrayed by the media?
As a proxy measurement for this, we've decided to look at twitter exchanges between members of the U.S congress and organization related to these in order to look for patterns that may tell us, how the U.S congress communciates. Our data consists of tweets made by members of congress, governmental organization and caucuses from 2017-2023 plus data like political affiliation and region of the different political users. [Dataset](data-description)

Specifically, we start off by investigating the relationship between democrats and republicans to establish, whether our big community (the U.S congress) can in fact be divided into seperate communities based on political affiliation. We do this by looking at the modularity of dividing the users into communities based on political affiliation. We also look at the assortativity between the different political affiliation. [Network-structure](network-structure)

Should our hypothesis, that the U.S congress is polarized not undoubtadly hold, we would like to investiage what relations that actually best describe the way the U.S congress communicates and organizes itself. We do this by dividing the different Twitter users into communities with the help of the Louvain algorithm. From here, we look to see if the modularity increases, that is, do we get a better community partitioning. [Community-structure](community-structure)

From here we would like to see, what underlying structures, if not political party, that binds the different communities together. Is it a special commitee that they talk a lot about, a law or a maybe a more general topic like foreign policy or welfare? We do this by doing text analysis on the biggest communities to see which keywords that describe them best. We would furthermore also like to do some wordclouds on these communities. [Congressional-communities](congressional-communities)

Finally, we would like to see, how the relationship between democrats and republicans has changed over the years. We do this by looking at the democrat-republican modularity and associativity throughout the years. We also look at what has changed in the two parties' talking points by doing TF-IDF on the two parties' corpuses throughout the years. [Evolving-dynamics](evolving-dynamics)


<!---
Donec posuere justo at risus [efficitur convallis](#). Donec enim nibh, aliquet vel risus id, tincidunt consectetur felis. Proin porttitor odio a orci accumsan bibendum id at risus. Sed a posuere odio, ac lobortis augue. Maecenas aliquet ipsum vel libero dignissim, non aliquet justo eleifend. Fusce mollis, ante eget tincidunt imperdiet, mi ligula venenatis ex, ut pulvinar nunc ipsum tempus eros. Aliquam erat volutpat. Sed id _iaculis arcu_, sit amet varius libero. Etiam quis nisl pretium, eleifend quam nec, rutrum sapien. **Donec rutrum accumsan orci.**


## Math formula


$$ x^n + y^n = z^n $$

## Code chunk

```
import pandas as pd

df = pd.DataFrame()
```

Sed id orci ullamcorper, commodo sapien in, scelerisque nunc. Duis posuere sed nisl in gravida. Pellentesque rutrum justo ut mi tempus dignissim. Ut pulvinar quis urna ut molestie. Pellentesque nec arcu metus. Vivamus non rutrum magna. Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas.

![](https://source.unsplash.com/random/?Copenhagen)

Phasellus viverra tellus viverra purus placerat, et lacinia mauris tristique. Nam semper venenatis lorem, nec ullamcorper tortor dignissim eget. Etiam non ipsum sed neque pharetra ullamcorper. Praesent ultrices ipsum varius dictum lacinia. Nulla placerat magna augue, volutpat rutrum nulla finibus sed. Phasellus maximus mi sit amet risus mattis, porta rhoncus elit dictum. Donec vel viverra lectus, vitae elementum arcu. Quisque quis molestie elit. Cras eget tellus vitae risus fermentum bibendum vitae ac turpis. Praesent mi eros, scelerisque sit amet sem at, hendrerit accumsan ligula.

> Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nam nec mauris aliquet, convallis ligula vel, mollis est. Fusce accumsan massa vel lectus dapibus, at vehicula elit auctor.

| Column 1  | Column 2  |  Column 3 |
|---|---|---|
| 1 | 4 | 7 |
| 2 | 5 | 8 |
| 3 | 6 | 9 |

## [Explainer Notebook](explainer-notebook.html)

Aenean non augue vulputate, bibendum ligula ac, euismod arcu. Proin consequat, urna at lobortis sodales, ligula nulla molestie dolor, et interdum nulla arcu eu lacus. Aenean maximus mi vel augue blandit, quis vehicula libero egestas. In mollis nibh in turpis sodales, eget luctus sem pretium. Integer lobortis diam vel nisi laoreet, ut condimentum risus ultrices. Praesent diam risus, imperdiet at lorem in, hendrerit auctor ex.
-->
