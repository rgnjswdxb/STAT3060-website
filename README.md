## STAT3060-website
- In STAT3060, we focus on how to use computational thinking and real data to quantitatively solve social science problems. 
- Through Python and its application in data science, we will take the smart community of Fuzhou as an example, discover problems, collect and combine data from end users, enterprises, governments and other parties and propose solutions. 
- This website shows how we improve the residential support function of the wechat public platform called "问需金山".
<hr>

### Introduction
![imagenhwy](nhwy.jpg)

"你呼我应", the residential support function of "问需金山" mainly provides a platform for residents to make complaints and suggestions to the community more easily. As long as one fills out the form as required, the complaint will be uploaded and sent to relevant staff, then he or she may get the reply in several days.
However, we noticed some problems:
1. Residents can only see the recently closed cases. There's no monthly or quarterly summary of cases closed available for residents. 
2. Residents don't get a quick idea of how much time each case takes for related department to resolve. ![imagebmx](sjbmx.jpg)
3. Each time a new case is uploaded, the staff member will manually identify the category and which related department it should be transferred to. What we are going to do is to simplify this step: for example, we can abstract some key words from the case descriptions to categorize these cases into some specified groups. In this way, we can better help classify and assign the cases. 

![image1](1.jpg)

### Our ideas (Method, Result and Discussion)
For the problems mentioned above, our solutions are given below:

##### It should be noted that due to the lack of data provided by Zhongtian Community, we additionally supplement the data recorded by Sanya "12345" citizen support hotline since both Fuzhou and Sanya belong to Second-tier City and they are tourist cities. 

##### 1. Visualization of monthly summary of cases closed 简单放一张月度总结的可视化图
展示完整报告 再简单介绍一下整体情况


##### 2. Quick access to the average time required for each type of case 

<script src="https://cdn.plot.ly/plotly-latest.min.js"></script>

<div>                            <div id="78ecfcf5-b98f-4bae-80c2-92591dfac6bd" class="plotly-graph-div" style="height:100%; width:100%;"></div>            <script type="text/javascript">                                    window.PLOTLYENV=window.PLOTLYENV || {};                                    if (document.getElementById("78ecfcf5-b98f-4bae-80c2-92591dfac6bd")) {                    Plotly.newPlot(                        "78ecfcf5-b98f-4bae-80c2-92591dfac6bd",                        [{"alignmentgroup":"True","hovertemplate":"category=%{x}<br>average processing time (hours)=%{marker.color}<extra></extra>","legendgroup":"","marker":{"color":[7,6,7,5,10,4,7,4,5,6,2],"coloraxis":"coloraxis","pattern":{"shape":""}},"name":"","offsetgroup":"","orientation":"v","showlegend":false,"textposition":"auto","x":["\u5b89\u5168\u76d1\u7ba1","\u7ecf\u6d4e\u7efc\u5408","\u79d1\u6559\u6587\u536b","\u793e\u4f1a\u7ba1\u7406","\u793e\u4f1a\u6295\u8d44\u670d\u52a1","\u793e\u4f1a\u56e2\u4f53","\u6570\u5b57\u57ce\u7ba1","\u516c\u5b89\u653f\u6cd5","\u516c\u7528\u4e8b\u4e1a","\u5efa\u8bbe\u4ea4\u901a","\u5176\u4ed6"],"xaxis":"x","y":[7,6,7,5,10,4,7,4,5,6,2],"yaxis":"y","type":"bar"}],                        {"barmode":"relative","coloraxis":{"colorbar":{"title":{"text":"average processing time (hours)"}},"colorscale":[[0.0,"#0d0887"],[0.1111111111111111,"#46039f"],[0.2222222222222222,"#7201a8"],[0.3333333333333333,"#9c179e"],[0.4444444444444444,"#bd3786"],[0.5555555555555556,"#d8576b"],[0.6666666666666666,"#ed7953"],[0.7777777777777778,"#fb9f3a"],[0.8888888888888888,"#fdca26"],[1.0,"#f0f921"]]},"legend":{"tracegroupgap":0},"margin":{"t":60},"template":{"data":{"barpolar":[{"marker":{"line":{"color":"#E5ECF6","width":0.5},"pattern":{"fillmode":"overlay","size":10,"solidity":0.2}},"type":"barpolar"}],"bar":[{"error_x":{"color":"#2a3f5f"},"error_y":{"color":"#2a3f5f"},"marker":{"line":{"color":"#E5ECF6","width":0.5},"pattern":{"fillmode":"overlay","size":10,"solidity":0.2}},"type":"bar"}],"carpet":[{"aaxis":{"endlinecolor":"#2a3f5f","gridcolor":"white","linecolor":"white","minorgridcolor":"white","startlinecolor":"#2a3f5f"},"baxis":{"endlinecolor":"#2a3f5f","gridcolor":"white","linecolor":"white","minorgridcolor":"white","startlinecolor":"#2a3f5f"},"type":"carpet"}],"choropleth":[{"colorbar":{"outlinewidth":0,"ticks":""},"type":"choropleth"}],"contourcarpet":[{"colorbar":{"outlinewidth":0,"ticks":""},"type":"contourcarpet"}],"contour":[{"colorbar":{"outlinewidth":0,"ticks":""},"colorscale":[[0.0,"#0d0887"],[0.1111111111111111,"#46039f"],[0.2222222222222222,"#7201a8"],[0.3333333333333333,"#9c179e"],[0.4444444444444444,"#bd3786"],[0.5555555555555556,"#d8576b"],[0.6666666666666666,"#ed7953"],[0.7777777777777778,"#fb9f3a"],[0.8888888888888888,"#fdca26"],[1.0,"#f0f921"]],"type":"contour"}],"heatmapgl":[{"colorbar":{"outlinewidth":0,"ticks":""},"colorscale":[[0.0,"#0d0887"],[0.1111111111111111,"#46039f"],[0.2222222222222222,"#7201a8"],[0.3333333333333333,"#9c179e"],[0.4444444444444444,"#bd3786"],[0.5555555555555556,"#d8576b"],[0.6666666666666666,"#ed7953"],[0.7777777777777778,"#fb9f3a"],[0.8888888888888888,"#fdca26"],[1.0,"#f0f921"]],"type":"heatmapgl"}],"heatmap":[{"colorbar":{"outlinewidth":0,"ticks":""},"colorscale":[[0.0,"#0d0887"],[0.1111111111111111,"#46039f"],[0.2222222222222222,"#7201a8"],[0.3333333333333333,"#9c179e"],[0.4444444444444444,"#bd3786"],[0.5555555555555556,"#d8576b"],[0.6666666666666666,"#ed7953"],[0.7777777777777778,"#fb9f3a"],[0.8888888888888888,"#fdca26"],[1.0,"#f0f921"]],"type":"heatmap"}],"histogram2dcontour":[{"colorbar":{"outlinewidth":0,"ticks":""},"colorscale":[[0.0,"#0d0887"],[0.1111111111111111,"#46039f"],[0.2222222222222222,"#7201a8"],[0.3333333333333333,"#9c179e"],[0.4444444444444444,"#bd3786"],[0.5555555555555556,"#d8576b"],[0.6666666666666666,"#ed7953"],[0.7777777777777778,"#fb9f3a"],[0.8888888888888888,"#fdca26"],[1.0,"#f0f921"]],"type":"histogram2dcontour"}],"histogram2d":[{"colorbar":{"outlinewidth":0,"ticks":""},"colorscale":[[0.0,"#0d0887"],[0.1111111111111111,"#46039f"],[0.2222222222222222,"#7201a8"],[0.3333333333333333,"#9c179e"],[0.4444444444444444,"#bd3786"],[0.5555555555555556,"#d8576b"],[0.6666666666666666,"#ed7953"],[0.7777777777777778,"#fb9f3a"],[0.8888888888888888,"#fdca26"],[1.0,"#f0f921"]],"type":"histogram2d"}],"histogram":[{"marker":{"pattern":{"fillmode":"overlay","size":10,"solidity":0.2}},"type":"histogram"}],"mesh3d":[{"colorbar":{"outlinewidth":0,"ticks":""},"type":"mesh3d"}],"parcoords":[{"line":{"colorbar":{"outlinewidth":0,"ticks":""}},"type":"parcoords"}],"pie":[{"automargin":true,"type":"pie"}],"scatter3d":[{"line":{"colorbar":{"outlinewidth":0,"ticks":""}},"marker":{"colorbar":{"outlinewidth":0,"ticks":""}},"type":"scatter3d"}],"scattercarpet":[{"marker":{"colorbar":{"outlinewidth":0,"ticks":""}},"type":"scattercarpet"}],"scattergeo":[{"marker":{"colorbar":{"outlinewidth":0,"ticks":""}},"type":"scattergeo"}],"scattergl":[{"marker":{"colorbar":{"outlinewidth":0,"ticks":""}},"type":"scattergl"}],"scattermapbox":[{"marker":{"colorbar":{"outlinewidth":0,"ticks":""}},"type":"scattermapbox"}],"scatterpolargl":[{"marker":{"colorbar":{"outlinewidth":0,"ticks":""}},"type":"scatterpolargl"}],"scatterpolar":[{"marker":{"colorbar":{"outlinewidth":0,"ticks":""}},"type":"scatterpolar"}],"scatter":[{"fillpattern":{"fillmode":"overlay","size":10,"solidity":0.2},"type":"scatter"}],"scatterternary":[{"marker":{"colorbar":{"outlinewidth":0,"ticks":""}},"type":"scatterternary"}],"surface":[{"colorbar":{"outlinewidth":0,"ticks":""},"colorscale":[[0.0,"#0d0887"],[0.1111111111111111,"#46039f"],[0.2222222222222222,"#7201a8"],[0.3333333333333333,"#9c179e"],[0.4444444444444444,"#bd3786"],[0.5555555555555556,"#d8576b"],[0.6666666666666666,"#ed7953"],[0.7777777777777778,"#fb9f3a"],[0.8888888888888888,"#fdca26"],[1.0,"#f0f921"]],"type":"surface"}],"table":[{"cells":{"fill":{"color":"#EBF0F8"},"line":{"color":"white"}},"header":{"fill":{"color":"#C8D4E3"},"line":{"color":"white"}},"type":"table"}]},"layout":{"annotationdefaults":{"arrowcolor":"#2a3f5f","arrowhead":0,"arrowwidth":1},"autotypenumbers":"strict","coloraxis":{"colorbar":{"outlinewidth":0,"ticks":""}},"colorscale":{"diverging":[[0,"#8e0152"],[0.1,"#c51b7d"],[0.2,"#de77ae"],[0.3,"#f1b6da"],[0.4,"#fde0ef"],[0.5,"#f7f7f7"],[0.6,"#e6f5d0"],[0.7,"#b8e186"],[0.8,"#7fbc41"],[0.9,"#4d9221"],[1,"#276419"]],"sequential":[[0.0,"#0d0887"],[0.1111111111111111,"#46039f"],[0.2222222222222222,"#7201a8"],[0.3333333333333333,"#9c179e"],[0.4444444444444444,"#bd3786"],[0.5555555555555556,"#d8576b"],[0.6666666666666666,"#ed7953"],[0.7777777777777778,"#fb9f3a"],[0.8888888888888888,"#fdca26"],[1.0,"#f0f921"]],"sequentialminus":[[0.0,"#0d0887"],[0.1111111111111111,"#46039f"],[0.2222222222222222,"#7201a8"],[0.3333333333333333,"#9c179e"],[0.4444444444444444,"#bd3786"],[0.5555555555555556,"#d8576b"],[0.6666666666666666,"#ed7953"],[0.7777777777777778,"#fb9f3a"],[0.8888888888888888,"#fdca26"],[1.0,"#f0f921"]]},"colorway":["#636efa","#EF553B","#00cc96","#ab63fa","#FFA15A","#19d3f3","#FF6692","#B6E880","#FF97FF","#FECB52"],"font":{"color":"#2a3f5f"},"geo":{"bgcolor":"white","lakecolor":"white","landcolor":"#E5ECF6","showlakes":true,"showland":true,"subunitcolor":"white"},"hoverlabel":{"align":"left"},"hovermode":"closest","mapbox":{"style":"light"},"paper_bgcolor":"white","plot_bgcolor":"#E5ECF6","polar":{"angularaxis":{"gridcolor":"white","linecolor":"white","ticks":""},"bgcolor":"#E5ECF6","radialaxis":{"gridcolor":"white","linecolor":"white","ticks":""}},"scene":{"xaxis":{"backgroundcolor":"#E5ECF6","gridcolor":"white","gridwidth":2,"linecolor":"white","showbackground":true,"ticks":"","zerolinecolor":"white"},"yaxis":{"backgroundcolor":"#E5ECF6","gridcolor":"white","gridwidth":2,"linecolor":"white","showbackground":true,"ticks":"","zerolinecolor":"white"},"zaxis":{"backgroundcolor":"#E5ECF6","gridcolor":"white","gridwidth":2,"linecolor":"white","showbackground":true,"ticks":"","zerolinecolor":"white"}},"shapedefaults":{"line":{"color":"#2a3f5f"}},"ternary":{"aaxis":{"gridcolor":"white","linecolor":"white","ticks":""},"baxis":{"gridcolor":"white","linecolor":"white","ticks":""},"bgcolor":"#E5ECF6","caxis":{"gridcolor":"white","linecolor":"white","ticks":""}},"title":{"x":0.05},"xaxis":{"automargin":true,"gridcolor":"white","linecolor":"white","ticks":"","title":{"standoff":15},"zerolinecolor":"white","zerolinewidth":2},"yaxis":{"automargin":true,"gridcolor":"white","linecolor":"white","ticks":"","title":{"standoff":15},"zerolinecolor":"white","zerolinewidth":2}}},"title":{"text":"average processing time for different categories in Sanya 12345 (round to hours)"},"xaxis":{"anchor":"y","domain":[0.0,1.0],"title":{"text":"category"}},"yaxis":{"anchor":"x","domain":[0.0,1.0],"title":{"text":"average processing time (hours)"}}},                        {"responsive": true}                    )                };                            </script>        </div>

Because we didn't get the data from Zhongtian Community, we used Sanya's data.

With this function, residents just need to choose the type... click! Getting the average time required, they will have a general idea of how long their complaints will be resolved.

Of course, there's still room for improvement, the current categories are not so clear that can help residents as expected. They might be confused sometimes: 
![imagetime1](wp-data1.jpg)

So a possible solution is that we can make new specified categories for residents. Using keywords such as "rubbish(垃圾)", "parking(停车)", "cube(管道)", etc, to do the classification might have a better effect. 
![imagetime2](wp-data2.jpg)


##### 3. Automatic classification and assignment of cases
For this part, we used machine learning to get the work done. Basically our thought is to identify the importance of each word for each text and the probability that the text belongs to each category, to get the final results.

We first divided the whole content into many word blocks. 

![imagefck](fck.jpg)

Then calculate the TF-IDF value of each block. Here, TF-IDF(Term Frequency-Inverse Document Frequency) is a statistical measure that evaluates how relevant a word is to the content of one case in a collection of cases. This is done by multiplying two metrics: how many times a word appears in one case, and the inverse frequency of the word across a set of . 放图

For more details, please refer to https://monkeylearn.com/blog/what-is-tf-idf/

At next step, MNB(Multinomial Naive Bayes Classifier) plays the critical role. Briefly, with the calculated TF-IDF value, MNB helps us compute the conditional probabilities of occurrence of different events based on the probabilities of occurrence of each individual event. Actually, Naive Bayes classifiers have worked quite well in many real-world situations, famously document classification and spam filtering. They require a small amount of training data to estimate the necessary parameters.

For more details, please refer to https://www.geeksforgeeks.org/naive-bayes-classifiers/

The method is completed, problem comes behind:
放一些图
- When we use Bayes Classifier, if the numbers of training samples of different categories in the classification task vary greatly, i.e., imbalanced datasets, the result will be biased towards large categories. 

  For example, our dataset is imbalanced. If we classify complaint information in “你呼我应” according to the type of incident, we can observe a big difference that "小区管理类" accounts for 63.3% of the total samples, while "消防安全类" only accounts for 2.9%. After calculating the error rate of predicting each category, the error rate of predicting "街面秩序类" is the largest, which is 32.4%. Besides, 81.8% of the wrong predictions are "小区管理类", so this category imbalance has a negative impact on the classification results. (It is worth mentioning that "消防安全类", the category with the smallest percentage, is not the category with the largest error rate, probably because the vocabulary used in the "消防安全类" has great characteristics that clearly distinguish this category from other categories. For future improvement, we can adopt undersampling, oversampling, or changing the model to solve the sample imbalance problem. 

  For more details, please refer to https://www.cnblogs.com/zhangxianrong/p/15214399.html
  
- TF-IDF is not perfect. It only uses word frequency information as a measurement of the importance of feature items in the data set. This results in the inability to correctly reflect the differences between documents of different categories. As we said above, TF-IDF doesn't work well when it comes to unbalanced data. Therefore, we introduce an improved method, FDCD-TF-IDF, based on word frequency distribution and category distribution, proposed by Haoying Wu and Na Yuan from Wuhan University of Technology. The experimental results show that this improved algorithm can "achieve better classification results on both balanced and unbalanced text data sets" (Wu and Yuan 212).

  FDCD-TF-IDF reflects the correlation between the feature items and the categories, and the category information of the feature items, thus solving the limitations of the original TF-IDF algorithm. The flow chart is given below (Wu and Yuan 213).
  
  ![imageflow](flow.jpg)
  
  For more details, please refer to https://doi.org/10.1145/3232116.3232152

- MNB Classifier can be improved as well. Eibe Frank from University of Waikato and Remco R. Bouckaert from Xtal Mountain Information Technology proposed an appropriate correction by "adjusting attribute priors" (Frank and R. Bouckaert 503). With this correction implemented as another data normalization step, they showed that "it can significantly improve the area under the ROC curve" (Frank and R. Bouckaert 503).

  For more details, please refer to https://doi.org/10.1007/11871637_49

### Conclusion
Basically, we proposed three suggestions to the current functions of "你呼我应", two for improving residents' convenience, monthly summary of cases closed and quick access to the average time required for each type of case; one for increasing the work efficiency of community workers, automatic classification and assignment of cases. All three still has a lot to improve, but we hope that currently these three functions can really help a bit.

### Works Cited
1. Frank, Eibe, and Remco R. Bouckaert. "Naive bayes for text classification with unbalanced classes." European Conference on Principles of Data Mining and Knowledge Discovery. Springer, Berlin, Heidelberg, 2006.
2. Wu, Haoying, and Na Yuan. "An Improved TF-IDF algorithm based on word frequency distribution information and category distribution information." Proceedings of the 3rd International Conference on Intelligent Information Processing. 2018.



