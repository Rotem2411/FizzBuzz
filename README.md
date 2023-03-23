# FizzBuzz
### Deep Learning EX1


1)	Take the FizzBuzz example and make it work.
2)	Add to the code a function that analyzes the results.
a.	Print the accuracy of the classifier.
b.	Generate a confusion matrix.
3)	Run it once and show the results.
4)	Rerun the algorithm 10 times and see if there are differences in the accuracy.
Generate a graph showing the differences in the results.
5)	Change the representation from binary to prime based. That means each number is coded by how many time each prime appears in the product. For large primes you can put them all in one bucket.
Example:  24 is coded as 2^3* 3^1 -   [3,1,0,0,0,0…]
Which of the algorithms (first and second) will work better? Run them and write the results and compare them.
6)	Find the smallest network for the prime representation that will yield perfect results
7)	Write a function that is given as input the prime representation and it classifies the number. It does not have to be a neural net classifier but works on the representation without any additional knowledge or data.
8)	Take the smallest classifier you built and instead of training it, hardcode the weights into it and show that it yields perfect results like in 6 & 7.
9)	Implement in Python a Neuron class. It should not be based on a well-known system like TF. Just pure code. Here is the main that uses it:

n = Neuron(10,0.1,RELU or SIGMOID)   # In this case the size of x is 10 and the std is 0.1
x = np.random.normal(0,0.1,10)  
res = n.forward(x)   #given x compute the result and maintain results in the object
db,dw,dx = n.backward(0.3) # Given the error (0.3 in this case) compute the derivatives
print(res,db,dw,dx)
x = np.ones(10)
w = np.array([1,2,3,4,5,6,7,8,9,10])
n.SetWb(w,3)  # change w and b
res = n.forward(x)
db,dw,dx = n.backward(0.3)
print(res,db,dw,dx)
            
Show the results obtained for both activation functions.
