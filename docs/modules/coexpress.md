## Coexpression analysis 

If coexpression data was provided (through either a .soft or .csv file), this panel will show expression information through both a hierarchically clustered heatmap and a coexpression network (see below).

![Coexpression header](../assets/images/image008.png)
![Coexpression heatmap 1](../assets/images/image010.png)
![Coexpression heatmap 2](../assets/images/image012.png)

You can choose to show either expression fluctuation (the rate of which expression level of a gene changes between samples), color-coded from white to black; or expression intensity (expression level of a gene related to the sample value distribution), color coded from yellow to red.

![Coexpression network](../assets/images/image014.png)

In the correlation network graph, you can see how genes within the cluster (box-shaped nodes) interact with each other, and with other genes in other clusters (ellipse-shaped nodes with solid edges and the corresponding cluster number inside) or anywhere else on the genome (ellipse-shaped nodes with dashed edges).

![Coexpression 1](../assets/images/coex_relations.png)

Additionally, by enabling the coexpression analysis, you will also get a Hiveplot overview of significant cluster-cluster interactions detected in the selected transcriptomics dataset. This can be accessed in the cluster overview screen.

## Input data 
To see the input data of this module check [Submitting jobs on the webserver](../website_submission.md/#gene-expression-analysis-coexpress)