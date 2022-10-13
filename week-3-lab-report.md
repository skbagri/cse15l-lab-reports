# Week 1 Lab Report
## Part 1: Simplest Search Engine  

## Part 2: Debugging    
**ArrayExamples - averageWithoutLowest Bug**  

Failure-Inducing Input  
![Image](ArrayExamplesTests.png)  
Symptom  
![Image](ArrayExamplesFailure.png)  
Fix  
![Image](ArrayExamplesFix.png)  
As we can see with the first test for the averageWithoutLowest method, it failed to show a symptom of the bug and therefore, passed. The second test, however failed due to the bug which resulted from the fact that the method did not take into account if there were two lowest numbers. In other words, did the lowest number appear twice in the given array? In the second test, the given array has a lowest number of 2.0 which appears twice. The method, as a result, excludes both of these when calculating the sum of the doubles but then only excludes one of them when calculating the mean. Thus, an input of array {2.0, 4.0, 2.0} gives an average of 4.0/2 = 2.0 instead of (2.0+4.0)/2 = 3.0.  
To fix this, I created a new integer variable, index, set to 0 and used this to keep track of the index of lowest number that would be excluded from the sum. Then, in the for loop, I had it skip the sum step for the value at that index.  
  
**ListExamples - merge Bug**  

Failure-Inducing Input  
![Image](ListExamplesTests.png)  
Symptom  
![Image](ListExamplesFailure.png)  
Fix  
![Image](ListExamplesFix.png)  
Again, the second test failed while the first one passed. This is because of a minor bug in the merge method, even though it resulted in an infinite loop when I tried to test it (the infinite loop is represented by the .. in the Symptom photo -- I had to press Ctrl-C to exit it). This is caused by the last while loop in the method. The code would increment index1 by 1 each time the loop ran until index2 was greater than or equal to list2.size(). Since it was index1 being incremented instead of index2, this condition would never be met, resulting in a loop that would go on forever and whatever element in list2 at index2 to be repeatedly added to the merged list. I fixed this by updating index2 to increment by 1.