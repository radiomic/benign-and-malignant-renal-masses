We provided four different random forest models.
1.Random forest model with five features and normalized feature values.model >>> This model uses all five selected texture features with normalized values. The normalization was done 0 to 1. 
2.Random forest model with five features and without normalized feature values.model >>> This model uses all five selected texture features without normalized values. In other words, the feature values are original.
3.Random forest model with four features and normalized feature values.model >>> This model uses four selected texture features with normalized values. One of the features was excluded due to collinearity. The normalization was done 0 to 1. 
4.Random forest model with four features and without normalized feature values.model >>> This model uses four selected texture features without normalized values. One of the features was excluded due to collinearity. In other words, the feature values are original.

How to use these model files:
1. Prepare your data frame using .csv format.
2. For models with five features, the columns in the first row should be coded as F27, F84, F193, F203, F245, BenignMalign. F27 represents S(0,1)SumVarnc. F84 represents S(2,2)Entropy. F193 represents S(5,0)SumEntrp. F203 represents S(0,5)SumVarnc. F245 represents 135dr_RLNonUni.
3. For models with four features, the first row should be coded as F27, F84, F203, F245, BenignMalign. F27 represents S(0,1)SumVarnc. F84 represents S(2,2)Entropy. F203 represents S(0,5)SumVarnc. F245 represents 135dr_RLNonUni.
4. Please be careful about the lower and upper cases in coding. Otherwise, it will not work.
5. The last column, namely BenignMalign, is the target in the classification tasks. It should be coded as Benign or Malign.
6. In models with normalization, please be careful about the normalization procedure used. It should be between 0 and 1.
7. In models without normalization, please do not use any feature scaling technique.
8. An example for the data frame in .csv format should be like the following:
	F27,F84,F193,F203,F245,BenignMalign
	0.759777,0.915896,0.985679,0.677315,0.286099,Malign
	0.424911,0.457583,0.373749,0.289107,0.022402,Benign
	0.471292,0.732684,0.72789,0.422797,0.086583,Malign
	...
9. The simplest way to use all these model files for the external validation is to use WEKA explorer application.
