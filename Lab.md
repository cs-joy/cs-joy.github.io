H  e  l  l  o    W  o  r  l  d  !

# Perceptrons

What is a neural network? To get started, I'll explain a type of artificial neuron called a perceptron. Perceptrons were developed in the 1950s and 1960s by the scientist Frank Rosenblatt, inspired by earlier work by Warren McCulloch and Walter Pitts. Today, it's more common to use other models of artificial neurons - in this book, and in much modern work on neural networks, the main neuron model used is one called the sigmoid neuron. We'll get to sigmoid neurons shortly. But to understand why sigmoid neurons are defined the way they are, it's worth taking the time to first understand perceptrons.

So how do perceptrons work? A perceptron takes several binary inputs, $x_1,x_2,…,$ and produces a single binary output:

![Perceptrons]("http://neuralnetworksanddeeplearning.com/images/tikz0.png")

In the example shown the perceptron has three inputs, $x_1,x_2,x_3$. In general it could have more or fewer inputs. Rosenblatt proposed a simple rule to compute the output. He introduced weights, $w_1,w_2,…,$ real numbers expressing the importance of the respective inputs to the output. The neuron's output, $0$ or $1$, is determined by whether the weighted sum $\sum_jw_jx_j$ is less than or greater than some threshold value. Just like the weights, the threshold is a real number which is a parameter of the neuron. To put it in more precise algebraic terms:

$$
\begin{equation}
\text{output} = 
\begin{cases} 
      0 & \text{if } \sum_j w_j x_j \leq \text{threshold} \\
      1 & \text{if } \sum_j w_j x_j > \text{threshold} 
   \end{cases}
\end{equation}
$$

That's all there is to how a perceptron works!

That's the basic mathematical model. A way you can think about the perceptron is that it's a device that makes decisions by weighing up evidence. Let me give an example. It's not a very realistic example, but it's easy to understand, and we'll soon get to more realistic examples. Suppose the weekend is coming up, and you've heard that there's going to be a cheese festival in your city. You like cheese, and are trying to decide whether or not to go to the festival. You might make your decision by weighing up three factors:

1) Is the weather good?
2) Does your boyfriend or girlfriend want to accompany you?
3) Is the festival near public transit? (You don't own a car). 

We can represent these three factors by corresponding binary variables $x_1,x_2,$ and $x_3$. For instance, we'd have $x_1=1$ if the weather is good, and $x_1=0$ if the weather is bad. Similarly, $x_2=1$ if your boyfriend or girlfriend wants to go, and $x_2=0$ if not. And similarly again for $x_3$ and public transit.
