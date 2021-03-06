# Data Intelligence Applications Exam Project - Social Influence & Pricing

In this repository you can find our project about Social Influence and Pricing for the "Data Intelligence Applications" exam. 

***

The request for the project follows:

The goal is modeling a scenario in which a seller is pricing some products and spends a given budget on social networks to persuade more and more nodes to buy the products, thus artificially increasing the demand. 
The seller needs to learn both some information on the social networks and the conversion rate curves.

1. Imagine:

	1. Three products to sell, each with an infinite number of units, in a time horizon T; 

	2. Three social networks composed of thousands of nodes, such that each social network is used to sell a different product;

	3. The activation probabilities of the edges of the social networks are linear functions in the values of the features (>3), potentially different in the three social networks;

	4. Three seasonal phases such that the transitions from a phase to the subsequent one are abrupt;

	5. A conversion rate curve for each social network and each phase, returning the probability that a generic node of the social network buys a product (notice that the phases affect the conversion rate curve, but not the activation probabilities of the social networks).

2. Design an algorithm maximizing the social influence in every single social network once a budget, for that specific social network, is given.
Plot the approximation error as the parameters of the algorithms vary for every specific network.

3. Design a greedy algorithm such that, given a cumulative budget to perform jointly social influence in the three social networks, finds the best allocation of the budget over the three social networks to maximize the cumulative social influence. 
Plot the approximation error as the parameters of the algorithms vary for every specific network.

4. Apply a combinatorial bandit algorithm to the situation in which the activation probabilities are not known and we can observe the activation of the edges. 
Plot the cumulative regret as time increases. 

5. Design a learning pricing algorithm to maximize the cumulative revenue and apply it, together with the algorithm to make social influence, to the case in which the activation probabilities are known. In doing that, simplify the environment adopting a unique seasonal phase for the whole time horizon. The daily number of customers interested to buy each product is the number of nodes of the corresponding social network activated by social influence.
For simplicity, imagine that every day the seller makes social influence to convince the nodes to buy the products and the activated nodes are the users that will try to buy the product. The actual purchase depends on the price charged by the seller and the conversion rate curve. 
For simplicity, assume that a node that has bought a product in a day can buy it also the subsequent days if activated by social influence. Plot the cumulative regret.

6. Design a learning pricing algorithm to maximize the cumulative revenue when there are seasonal phases and apply it, together with the algorithm to make social influence, to the case in which the activation probabilities are known.
The number of customers interested to buy each product is the number of nodes of the corresponding social network activated by social influence, as in the previous step. Plot the cumulative regret.

7. Plot the cumulative regret in the case the seller needs to learn both the activation probabilities and conversion rate curves simultaneously.

***

You can find 3 Python files and a pdf:
- The pdf file contains the presentation of the project where you can find our final plots and results shown to the professor at the moment of the project submission.
- The python files are the core of the project:
	- *network* contains all the classes that are used to define the graphs used in the experiments.
	- *mab* contains the classes about the learners used for the requests of the project.
	- *main* contains obviously all the code to be run in order to produce the results shown in the presentation; for each point in the requests we run a specific function contained in this file.

***

Note that for each function called at the end of the file we specify the size and the complexity of the graphs used by the functions. Feel free to change this parameters in order to try different configurations but pay attention to the time to process big and complex networks.
