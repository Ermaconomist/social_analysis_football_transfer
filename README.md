# social_analysis_football_transfer

## Table of Content:

_Prepartion_
* [Import packages](#import-packages)
* [Read scraped dataframe](#Read)
* [Create graphs with module networkx](#a)

_Analysis_
* [Attributes of generated graphs](#b)
* [Plot the graphs for first insights](#c)
* [Key metrics & Network structure](#d)
* [Preparation for metrics](#e)

_Visualization_
* [visualize degree of centrality](#f)
* [Community detection & analysis](#g)
* [Define helper functions](#h)
* [Visualize communities](#i)
* [Communities by modularity](#j)
* [Communities by degeneracy](#k)

_recap_
* [Findings](#m) 
* [Disclaimer & Scientific Delimitation](#l)


### Design approach for our graphs

Approach for a good graph layout we aim for:

1. **Minimum edges intersection** <br>
Too many intersections make the plot look messy. If applicable we will try to minimize dimensions.

2. **Adjacent vertices are closer to each other than not adjacent** <br>
Connected nodes should be close to each other. This represents the main information that is present in a graph by definition.

3. **Communities are grouped into clusters** <br>
If there are a set of vertices that are connected to each other more frequent then to other parts of the graph, they should look like a dense cloud.

4. **Minimum overlapping edges and nodes.**<br>
If we cannot determine if there few vertices or one, then the readability of plot is poor.


# Findings <a class="m" id="Read"></a> 

After the first plots we decided to plot the transfer network with colored nodes. Coloring the nodes referring to their impact in the network was quickly implemented. After a discussion in the group we decided to map the node coloring to the language family of the club.
Unfortunately this task was not possible to fulfill within the time avaliable. We tried different approaches from creating ID/VALUE sets or trying to map on a value for each language family. In the end we decided to show the best result we achieved within time.

Altough we did not achieved every goal we have set in the beginning, we made some interesting findings. The centrality scores defined that FC Lugano and FC Sion had the most transfers in the examined time-period. This is a bit surprising, because normally you would expect the clubs with the biggest budget in these positions (for Switzerland this would be FC Basel and BSC Young Boys).

The community plots and calculations are all on the same direction. We can state, that there is a quite strong network of transfers within the clubs of Switzerland. Because you normally expect this behaviour we were not surprised. We detected also some networks between swiss footbal clubs and foreign clubs. But those networks were rather loose.

It is also difficult to statistically proove the things we saw in the plots due to our limited dataset of about 4000 datapoints.