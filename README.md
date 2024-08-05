# Credit-Card-Customer-Clustering

## I. Background:
The objective of credit card customer clustering is to segment the customer base into distinct groups based on spending patterns, transaction behaviors, and demographic characteristics. By identifying these clusters, the company aims to tailor marketing strategies, enhance customer satisfaction, and improve product offerings, ultimately driving customer loyalty and increasing profitability. This data-driven approach will enable more personalized and efficient targeting of customers, optimizing resource allocation and maximizing the return on marketing investments.

## II. Conclusion:
To find the segmentations of credit card customers, first you will have to understand the data and clean it well. From knowing the types of data, cleaning the empty values data, finding out how spread out of the data are, handling the outliers, feature selection and using the clustering model well.
The data that is used have 18 columns with 4475 entries and 155 empty values. The credit card limit ranges from 0 to 20000, peaking at 2500. Mainly credit card customers pay in 12 months tenures. The balance of the customers ranges from 0 to 17500 and peaking at a little over 0.
After erasing the empty datas, there is still a lot of information that will be valuable for the model to read. As all of the data are numerical with encoded categorical values, the skewness will be checked for dealing with the outliers. There are different methods to be used based on the skewness of the columns. Though after handling the outlier, there doesn't seem to be a lot of differences with the data before outlier handling.
Based on the graph and plots that are shown, some of the clusters are very visible and easy to read. Though some of the graphs are hard to read and/or some are quite similar to one another. Which means the number of clusters may have been too much or less than ideal. Nevertheless, the elbow and silhouette shows that it seems to be quite ideal.
The advantages of the K-means models in this case are that it scales well for data that has a large number of samples, it loads fast (important for big datas), and can be interpreted easily. The disadvantages are that it need to manually search for the number of clusters. Which means that the number of clusters that we put may or may not have been accurate. Its initial centroid points are quite sensitive, with different placement, the outcomes might be different. It's also outlier sensitive, which means that the final placement of centroid can be affected by the outliers.
To improve the model, it needs another model to check for a more accurate clustering. For example using DBSCAN might help to check for the ideal number of clusters. Maybe the pca or the dimensionality reduction number is also not that compatible with the data.
There are 6 clusters that we get from our model with different characteristics. The data mainly grouped in cluster 1. This imbalance data might affect the performance in identifying the clusters.
Based on the elbow method, 6 clusters are ideal for the customers segmentation. Due to the decrease difference in in the distance between each point and the centroid in a cluster. This decision is also strengthened by the silhouette score that Silhouette scores are nearing the number 1, along with the silhouette plot that shows evenly clustered data. The 6 clusters would look better.
Cluster 1 has a small balance with a small credit card limit. Cluster 2 has lower medium balance with a medium credit card limit. Cluster 4 has a higher medium balance with a higher medium credit card limit. In summary, the higher the balance, the higher its credit limit and vice versa.
Cluster 5 has the most purchases, followed by cluster 2, and cluster 0 has the least purchases. Cluster 4 has a decent amount of purchases. Cluster 1 and 3 have a similar amount of purchases.
As cluster 5 has the most purchases, cluster 5 also has the most payments. Cluster 4 also pays a good amount of payments. Cluster 2 also pays decently. Meanwhile cluster 3 pays the least amount. Cluster 2 might have more purchases compared to cluster 4, but cluster 2 has a more pricey credit usage compared to cluster 4.
Cluster 5 often purchased in installments. Cluster 2 is quite often purchased in installments. Cluster 4 is somewhat often at purchasing in installments. Cluster 1 and 3 are quite similar in ways of purchasing installments. Most in cluster 0 doesn't purchase installments quite often.
Cluster 4 frequently pays cash in advance, unlike cluster 0 who rarely pays in advance. Cluster 5 doesn't seem to either pay cash in advance or avoid it. Meanwhile cluster 1, 2, and 3 don't pay cash in advance frequently.
Clusters:
- 0: 
    * Least purchase
    * Don't really like to purchase in installments
    * Rarely pays in advance
    * Small in numbers


- 1:
    * Most customer in this data
    * Small card limit and balance
    * Quite small purchases
    * Quite small installment purchases
    * Doesn't pay cash in advance frequently
- 2:
    * Second largest part of data
    * Low medium balance with low medium card limit
    * Second most purchases
    * Decent amount of payments
    * Purchase installments quite often
- 3:
    * Fourth largest part of data 
    * Small amount of purchases
    * Small payments 
    * Quite small installment purchases
    * Doesn't pay cash in advance frequently
- 4:
    * Third largest part of data
    * High medium balance with a high medium credit card limit
    * Decent amount of purchases
    * Pays a good amount of payments
    * Somewhat often at purchasing in installments
    * Cluster 4 frequently pays cash in advance
- 5:
    * Small part of data
    * Purchase a lot
    * Have lots of payments
    * Often purchase in installment
    * An ok amount of cash advancement
Cluster 0 doesn't seem to like using credit cards. Majority of customers are cluster 1, seems to use credit card frugally. Cluster 2 seems quite lavish. Cluster 3 seems trying to limit use credit card. Cluster 4 are customers that seem knowledgeable in using credit cards. Cluster 5 seems to be the most lavish customers to use credit card. Cluster 4 prefers cash in advance for their pricey purchases rather than installments. Cluster 0 doesn't seem to like paying their purchases in cash advancement, seems to like installments better.

## III. Recommendations:
For customers on cluster 0, we can offer introductory rewards or cash backs on the initial purchases to encourage card usage. Since based on what we see they hardly use credit cards, we can assume that they don't really understand the credit card benefits, that’s why we could provide education campaigns for product benefits, information, and safety in using credit cards. Other than that, we could give them a free annual fee to reduce usage barriers.
For customers on cluster 1, we could increase their credit card limit gradually to encourage more usage. We could also provide targeted promotions with small, manageable rewards for them. Educational contents like tips on maximizing credit card benefits for them are also useful.
For customers on cluster 2, we could offer rewards programs that match their spending habits like higher points for specific categories. We can also give them access to exclusive deals and experiences. Loyalty program rewards for frequent and larger purchases can also be beneficial.
For customers on cluster 3, offer tools and resources to help manage spending and budgeting. Low-interest rates to reduce the cost of occasional purchases might be suitable for them. Lastly, promoting responsible credit use through educational materials might give improvement in their purchases.
For customers on cluster 4, offer premium services such as concierge, travel insurance, and extended warranties. Other than that, we could provide flexible payment options, installment plans with low-interest rates. Inviting them to exclusive events and providing personalized experiences can make their credit card usage more enjoyable.
For customers on cluster 5, develop high-end rewards programs with luxury benefits such as travel, fine dining, and exclusive experiences. A personalized service and support by assigning dedicated account managers can induce more credit card usage by them. Lastly, offering exclusive access to premium events and products would be suitable for this cluster of customers.

