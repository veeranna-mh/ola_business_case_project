Hi,

The files that I had uploaded yesterday had bigger fonts in the markdown cells and these markdown cells were not looking good.
I have reduced the font size wherever necessary. looks better now. I have uploaded these new set of files today in the same folder.

Other than that no changes done.

25.08.2024:
1. it was observed that while plotting decision trees, feature names were taken as feature_names=df.columns[:-1], 
	which actually is wrong since two more features are added after "Terget" feature. I thought of correcting it and uploading the new version of files after corrections.
	But, the execution times of some of the cells (like grid searchCV and randomizedsearchCV and model.fit in some cases are taking hours of time. 
	Even though time difference calculated using time.time() functionality shows a max of roughly 3 hours in one case, I feel it took 5-6 hours in reality.
	Due to these heavy execution times, I am not uploading the new versions with corrections.

27.08.2024:
1. I completely missed the instruction saying to aggregate the data in order to remove multiple occurrances of the same driver. 
	I realised this when I was doing peer review of one of the submission.
	Later I went through the data to do the aggregations. what I see is, there are multiple occurrances of the same driver ids but the months are different in reporting day column (MMM-YY).
	The day on which the driver reports to duty in a month can have impact on earnings, ratings etc. Even age is changing every 12 months (it can be seen in the given data).
	I feel it is not appropriate to aggregate these records for analysis / to create the dataset for machine learning. I feel it is better to keep these records as individual records for the analysis as well as model building.
	So, decided not to do the aggregations based on multiple occurrances of same driver Id.
	
2. There is one other mistake. I did imbalance treatment (using smote) on the whole data; I should have done it only on training set (i.e., after train-val-test splitting).

...........
thanks and regards
veeranna
