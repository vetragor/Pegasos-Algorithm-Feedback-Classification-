# Pegasos-Algorithm-Feedback-Classification-
This is Machine Learning Project. This code will convert review texts into feature vectors using a bag of words approach. We start by compiling all the words that appear in a training set of reviews into a dictionary , thereby producing a list of  d  unique words.  Then transform each of the reviews into a feature vector of length  d  by setting the  ith  coordinate of the feature vector to  1  if the  ith word in the dictionary appears in the review, or  0  otherwise. For instance, consider two simple documents “Mary loves apples" and “Red apples". In this case, the dictionary is the set  {Mary;loves;apples;red} , and the documents are represented as  (1;1;1;0)  and  (0;0;1;1) .
 The load data function, which can be used to read the .tsv files and returns the labels and texts. We have also supplied you with the bag_of_words function, which takes the raw data and returns dictionary of unigram words. The resulting dictionary is an input to extract_bow_feature_vectors which computes a feature matrix of ones and zeros that can be used as the input for the classification algorithms. Using the feature matrix and your implementation of learning algorithms from before, you will be able to compute  θ zero  and  θ .

Pegasos update rule (x(i),y(i),λ,η,θ): 
if  y(i)(θ⋅x(i))≤1  then
  update  θ=(1−ηλ)θ+ηy(i)x(i)  
else: 
  update  θ=(1−ηλ)θ  

The  η  parameter is a decaying factor that will decrease over time. The  λ  parameter is a regularizing parameter.

In this problem, you will need to adapt this update rule to add a bias term ( θ0 ) to the hypothesis, but take care not to penalize the magnitude of  θ0 .
