#  Mean and variance of a discrete  distribution


# Aim : 

To find mean and variance of arrival of objects from the feeder using probability distribution


# Software required :  

Python and Visual components tool

# Theory:

The expectation or the mean of a discrete random variable is a weighted average of all possible
values of the random variable. The weights are the probabilities associated with the corresponding values. 
It is calculated as,

![image](https://user-images.githubusercontent.com/103921593/192938463-e34177f4-f188-48a0-bda2-8f6d1d660ed2.png)

The variance of a random variable shows the variability or the scatterings of the random variables.
It shows the distance of a random variable from its mean. It is calcualted as

![image](https://user-images.githubusercontent.com/103921593/192938695-99fedc01-34d5-4d36-84df-5880e766ed0c.png)


# Procedure :

1. Construct frequency distribution for the data

2. Find the  probability distribution from frequency distribution.

3. Calculate mean using 
   
   ![image](https://user-images.githubusercontent.com/103921593/192940431-03b81777-c54d-4286-b4f4-82dfe7666b4c.png)

4. Find  
   
      ![image](https://user-images.githubusercontent.com/103921593/192940255-2d9dd746-6875-4a6d-877b-6da6cdb96ab1.png)

5.  Calculate variance using 
  
      ![image](https://user-images.githubusercontent.com/103921593/192942852-913550a9-fabe-4a55-b956-0487b18bbd97.png)

# Program :
NAME : SEKAR M

REG NO : 212225230257

SLOT NAME : T1-I5

```py
import numpy as np
data=[int(i) for i in input("Enter Arrival data :").split()]
Max=max(data)
lenth=len(data)
x=[]
freq=[]
for i in range(Max+1):
 c=0
 for j in range(lenth):
   if data[j]==i:
     c+=1
 x.append(i)
 freq.append(c)
sf=np.sum(freq)
p=[freq[i]/sf for i in range(Max+1)]
mean=np.inner(x,p)
ex2=np.inner(np.square(x),p)
var=ex2-mean**2
std=np.sqrt(var)
print(f"X\tP(x)")
for i in range(Max+1):
 if freq[i]>0:
   print(f'{x[i]}\t{p[i]:.3f} ')
print(f"mean: {mean}")
print(f'varience: {var}')
print(f"standard deviation: {std}")
```


# Output : 

<img width="673" height="299" alt="image" src="https://github.com/user-attachments/assets/81435ee3-9993-4da0-b63e-f5ff3b7e56cc" />

# Results :
The mean and variance of arrivals of objects from feeder using probability distribution are calculated.

