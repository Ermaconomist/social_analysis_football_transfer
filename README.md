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
