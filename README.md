# codefundo
code.fun.do++ idea for disaster management

 Objective:
 
During and after natural disasters, basic requirements like food, clothing, shelter, electricity and communication systems are handicapped.

 We are building a machine learning model for the distribution of relief items in an optimal way, after any natural disaster, over regions of affliction. 
 
 ALGORITHM:
 
 The afflicted region will be divided into N segments using clustering algorithm to get similar regions in the same cluster.
The similarity of regions is measured in terms of:

1. Population density of that region

	- The mean population density of the segmented region can be obtained easily from census data. Different population densities among the regions should affect the distribution.
2. Degree of Damage
	- It can be subdivided into many measurement categories. Our model focuses on these five. However, it can be extended for more categories.
	
 		a. Communication strength:
		
			It can be measured as any metric of strength of cellular and land-line networks in that region.
 		b. Electricity:
		
			It can be measured as a binary value: 1 for available and 0, otherwise in that region.
 		c. Potable water availability:
		
			It can be measured as mean number of days before the amount of potable water goes below a threshold(water reserve).
 		d. Food availability:
		
			It can also be measured as mean number of days before the food reserves in the region exhaust.
 		e. Transportation:
		
			It can be measured as mean time required to transport items to the segment. For regions with lesser mean time of transportation,items can be re-distributed easily.
			
 Taking mean of all features over the segments,N feature vectors (one vector 
corresponding to each of the segmented regions) is obtained. Let this input be
X.

 The basket of items of distribution can be classified into following bins:
 
1. Water, Food

2. Non-essentials

3. Hygiene items

4. Funds

5. Other essentials

6. Miscellaneous

A vector Y, where each element is total quantity of item available in the bins
given above is also given as input.

We can also assign priority indexes to each element of X, like, Potable water availability would have higher index than food, higher than communication, etc.

Now, we can train the model by generating data for optimal distribution to set the unknown parameters in the model using machine learning techniques.

 Output:
 
N vectors of dimensionality of Y. i-th vector has the distribution of items in the i-th segment.


 Practical issues in implementation and proposed solutions:
The data collection for training the model is an issue because determining features like Water reserve, food reserve is difficult. We can use legitimate approximations for such features.

On every application of model, we can use reinforcement learning techniques for improvement of model's performance.

Due to limited experience in Machine Learning and unavailablity of Training Data, we faced issues in Model Selection for the problem and after trying Linear Regression Models, we got pretty poor performance of model due to very limited data.
Hence, we submit one page slide with video explaining our idea.
