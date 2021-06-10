# Machine Learning

Below you will find anything and everything pertaining to the Machine Learning Portion of this project. Before reading, please the the ~5 minute overview video. Goals, Objectives,
and Implementations are explained their.  


### Introduction Video

Machine Learning Video Presentation  
<pre>
<a href="https://youtu.be/zTTHPHJ2c48" target="_blank"><img src="http://img.youtube.com/vi/zTTHPHJ2c48/0.jpg"
alt="IMAGE ALT TEXT HERE" width="350" height="250" border="10" /></a>
</pre>

### Demo Video of Inferenced Model Recommender

Posted by end of June 3rd, 2021  


### LSTM Model Explanation

The goal of LSTM netorks is to solve the issue of memory in both Regressive and Classification models. This is done by sequentially adding LSTM nodes that are meant to mimic human neurons. The following image is an example of an LSTM neuron.

<pre align="center">
  <img width="800" height="300" src="https://cdn.analyticsvidhya.com/wp-content/uploads/2017/12/10131302/13.png">
</pre>
<strong>sub_t</strong>: Is moment in time, remember that LSTM's are meant to make decisions based on previous inputs.<br>
<strong>h_t</strong>: Hidden Layer of LSTM<br>
<strong>C_t</strong>: Can be seen as the out for a given layer<br>
<strong>X_t-n</strong>: Is the input for that given layer in reference to time n. Again predictions are made by looking back in time. You can decide the N, which implies
 how much does the model  remember.<br>
 
#### Shortcomings
 While this model did serve to be dynamic, the given state is struggling to generalize. We believe this was because of the format of our given dataset. The given model was built as a multi-classification model which needs for any given input, please give me a vector of 0's and 1's. 1's implying a correct next chord, and 0's implying not a 'good' next chord. In its given state, each input only has one classifiction. (I.E. Only one, 1), but we have multiple inputs that are equal. We believe this was creating confusion, and requires tweaking to get better results.
 
#### Next Steps
 Along with updating the dataset, we would like to use a GAN approach to hopefully create a generator model that is even better than the LSTM. For more information on GAN's please click the following link.<br>
<a href="https://wiki.pathmind.com/generative-adversarial-network-gan#:~:text=Generative%20adversarial%20networks%20(GANs)%20are,video%20generation%20and%20voice%20generation.">GAN Basics Link</a>

### Static Binary Tree/Forest Model
As you learned from the video, the purpose of this model was to create a static, but 100% accurate music chord recommender. Unlike the LSTM model, this model lacks creativity, but is great for teaching less-experienced muscians both chord progressions, but also patters to stay in key. Key being defined as Major & Minor's. For example, for a chord recommendation in C Major, all chords recommended will be part of the C Major family. As you become more experienced in music, you learn that you can shift between certain majors and minors for specific shifts in sound, but before you can do that, you must first learn the Major/Minor Progressions. This model is perfect for this. The above demo showcases this model in actions.<br>

From a technical standpoint, the model was originally intended to be a pure forest model, but for inferencing reasons, we found that building and saving a time-sequential binary tree to be more successful. This tree is than loaded into a class that works with the Bela, to make recommendations for the user. Since binary trees and Forst Models have great documentation, I will leave a couple links if you want to learn more about these given data structures and models.<br>


<a href="https://www.baeldung.com/cs/binary-tree-intro">Binary Trees Explained</a><br>
<a href="https://towardsdatascience.com/understanding-random-forest-58381e0602d2">Random Forst Models Explained</a><br>
**Out model combines aspects of both to work. The biggest difference is that our Binary Trees support N-children per node, and we organize each tree based on starting chord options**

### Comment from Developer
On behalf of the entire team, I would like to thank you for reading. Our goal was to create something that is not only educational, but showcases how much music is correlated to your engineering studies. I believe that music is not only for entertainment, but is a teacher to better understand nature. If you have any questions, you can find my contact info on the team page. Thanks again!<br>
-James Elliott
