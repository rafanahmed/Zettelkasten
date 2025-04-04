
Tags: [[Neural Networks]], [[Trading]], [[Finance]], [[RNN]], [[LSTM]], [[Technical Analysis]], [[Portfolio Management]], [[Hyperparameter Tuning]], [[Machine Learning]], [[Data Science]], [[Quantitative Finance]], [[Predictive Analytics]]

## Reference:
https://www.youtube.com/watch?v=Kqs8TR2HJEk


## Notes:

The following video is marked with time stamps

**What is Neural Network**
0:59 - The Video creator establishes and compares a neural network to a brain. Our brain has neurons, so when we see a number (for example, 3), our brain will identify the curves and the shape of the numerical notation itself, pass those signals on in our brain, and then decide that it is the number 3. 

1:17 - Take this image of a cat in the video
![[Screenshot 2025-03-03 at 8.59.32 PM.png]]
The neural networks can identify that the image is that of a cat based on different kinds of training regimes. 
With this structure of neural networks come different types of neural networks


**Feed Forward Neural Network (FNN) with Example**
1:27 - The cat image above is an example of a feed-forward neural Network:
- Input layer (Cat image and grey dots) 
- Hidden layers (blue dots), each with information (aka hidden weights) added to it. Those weights are initially set at random weights.
- Output (orange dot) is what the random weights from the hidden layers have identified from the input layer
  
Say the initial identification of this neural network was a cheetah: 
- This cat image does not represent a cheetah, which is an error value. This error value will then go BACK into the weight/hidden layers area and then will adjust the weights based on the error value.
- This action of going BACK into the hidden layer to fix and adjust the weights/information is called back propagation
  
This process continues, and as there's another error value that pops up, the hidden/weights layer will promptly adjust until it finally gets the fact that it is a cat. 
- When the value goes forward into the output layer coming from the hidden layer, it is called forward propagation (or forward pass)
  ![[Screenshot 2025-03-03 at 9.42.00 PM.png]]

The number of times this process goes over and over again is called iterations or, in neural network terms, epochs. 
This type of neural network does NOT have a memory. In other words, once the model is created as the example shown above, it identifies a cat as a cat. 


**Recurrent Neural Network Structure (RNN)**
3:35 - Recurrent Neural Networks (RNNs) have a fundamental advantage over FNNs in the fact that it has memory; they will remember things. This can be applied and used in a sequence of data. 
Another advantage RNNs have over FNNs is that they have back propagation not only through hidden layers but also back propagation through time, aka back propagation through hidden states. 

5:01 - Let's take a look at an example of the sentence "I like to drink (blank)" and how it can predict the next word, "coffee":

![[Screenshot 2025-03-03 at 9.49.11 PM.png]]

- In time step t1, the first input word we have is "i". There is no previous hidden state, and the current hidden state, which is created in this first time step, is designated as h1.
- In time step t2, the second input word we have is "like". The previous hidden state is h1, and the current hidden state is then designated as h2. The current hidden state of h2 has gotten information from the previous state, h1, as well. This is how RNNs fundamentally have memory. 
- In time step t3, the third input word we have is "to". The previous hidden state is h2, and the current hidden state is then designated as h3. We are seeing again that the current state h3 is carrying that memory from previous hidden states. The previous FNN with the cat example did not have this memory functionality. 
- Finally, skipping to step t5, we do not have an input word. The previous hidden state is h4. Based on H4's data, which has accumulated the memory from H1-H3, we can predict that the next input word will be something that can be drunk, like coffee.


**RNN for Trading**
6:03 - Like how the example RNN was used to predict the next word for the sentence "i like to drink (blank)", you can use RNNs to predict stock prices
- Just like the prediction the RNN made for the word "coffee", you can use it to predict stock prices
- Instead of the input values being the words "i", "like", "to", and "drink" like the last example, the input values could be the yesterday's price for a stock (and the days before), RSI, Volume, and other 
	- Relative Strength Index - a technical analysis indicator used to measure the speed and change of price movements. RSI oscillates between 0 and 100 and is typically used to identify conditions where a financial asset might be overbought (often above 70) or oversold (often below 30). This can help traders and investors make more informed decisions about entering or exiting positions.
- The target value (aka the h5 value that was in the last RNN example, the current hidden state that was going to be predicted) for stock trading RNN could be a 5th-day return. 

Here is an RNN example in the context of trading:

![[Screenshot 2025-03-03 at 11.53.06 PM.png]]

- In time step t1, the first input is the stock price of the first day and the RSI of the first day. There is no previous hidden state, and the current hidden state, which is created in this first time step, is designated as h1. This continues all into t4 like the last example. 
- As each hidden state passes by, the memory is being stored, and the new information is carried over. This helps predict certain things in the stock market. We can predict if the market is going to be positive or negative based on all the RSI and price data of the past. 


**Problems of RNN** 
6:59 - The RNN has certain fundamental problems. 
- RNNs have a computational problem as they require a lot of computational power, unlike a decision tree or regression models. 
In the model shown in the video, they use a resource called QuantConnect, in which they don't use GPUs but use CPUs and still have been able to make an RNN. 
As we get to more complex models like LSTMs, it takes longer and more computational power to process these models. 
The Neural network model in the video is going to have a 64-bit memory vector. We can change and customize the amount of memory in a memory vector to create more complicated memory vectors that could go from 64 to 128 to 256. In the video, the model they make will have a memory vector of 64. 


**Hyperparameter Tuning**
 8:09 - With our trading model, we can implement many different ways of tuning, also known as Hyperparameter Tuning:
 - Input Features
 - Epochs
 - Hidden Vector Size
 - Learning Rate


**LSTM (Long Short-Term Memory)** 
10:02 - Another fundamental problem with RNNs is that they have what is called the Vanishing Gradient Problem. RNNs tend to get stuff that is kind of in the past. It is similar to when a human reads a very large book with a lot of characters, we tend to forget some of those characters just because of how many there are in that really big book. Likewise, neural networks tend to forget because of the back-propagation errors and the weights. Long short-term memory (LSTM) is a type of neural network that can learn and remember sequences of data.

To avoid forgetting information, LSTMs have a thing called a "forget gate". Along with the hidden layers of the neural network, which takes care of the problem of things that they forget and can take the important information in the past into consideration that is required to be remembered for a more accurate model. 

LSTMs have a fundamental problem in that it is extremely computationally intensive. It takes a while to back-test the video's quant strategy in LSTM. 


**Use case for RNN and LSTM** 
11:15 - Neural networks can be used not just for trading strategies but also to rebalance your portfolio. 
Take this image as an example for a reference:

![[Screenshot 2025-03-04 at 2.25.11 AM.png]]

Imagine you have a value investing portfolio and you need to adjust the allocation of the portfolio, you could use a machine learning model to allocate how much money you need to allocate to SHY, GLD, SPY and TLT and get good returns while minimizing the draw down. 
	"Draw down" refers to the decline in a portfolio's value from its highest point (peak) to its lowest point (trough) over a specific period. Essentially, it's a measure of the potential loss or the worst-case drop you could see in your portfolio.

RNN and LSTM models can be used for the following:
1. Entry or Exit trading condition
2. Improve on existing strategy
3. Rebalance Portfolio




 

  
  
  







