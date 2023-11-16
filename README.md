# MAX PROFIT PROBLEM


Intuition: 


-> Initially, I considered a greedy approach, where I would select the property with the highest earnings within a given time frame. However, this approach proved ineffective under certain conditions.

-> I then decided to explore a different strategy: trying out all possible combinations of properties to find the one that yielded the maximum earnings.

-> I developed a recursive approach to solve the problem (Solution 1). The solution being: I pick a property(Add the earnings of the property to the total sum) if the time taken to build is <= the timeUnit given, and similarly move on to the next one. And I don't pick one property and move on to next one, and at the end we take the max of both of them. Doing this recursively will give equal chance to all the properties whose time is <= given timeUnit. 

-> Afterward, I further optimized the space complexity by implementing dynamic programming (Solution 2).

-> I've documented both solutions in separate files, with Solution 2 being the most efficient, offering a time complexity of O(N*timeUnit) and a space complexity of O(N*timeUnit).

-> We can even cut down the space from O(N*timeUnit)+O(N) to O(N*timeUnit) by using tabulation. Since we have a fixed number of elements in our,i.e. 3(Theatre, Pub, Commercial Park), the space complexity stays to be constant.


**NOTE: I have written the code in C++ as it is my primary coding language. I have fair knowledge in javascript and java as well. **


-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------



_**Updated Solution:**_

-> I have to generate all the combinations of the property and not just the max one.

-> I have followed the same intuition as per my Solution 1 and 2. The only update I have done is I have added an extra array "currentCombination" and it contains the current combination of the properties. 

-> If we pick an element then it marks 1 and if we don't pick an element it marks 0. Similarly at the end it has the combination and we print it. We do it for all the possible combinations.

-> Time Complexity: O(2^N). Space Complexity: O(N). Since N is constant(i.e., 3) so overall time and space is also constant.


----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
_**Updated Solution:**_

-> **File name: Update2Code**

-> Along with the currentCombinations array, I carried a variable along to capture the earnings for every combination. 

-> Used backtracking for the earnings as well to manage calculating for all the combinations.

-> The time and space complexity stands O(2^N) and O(N) respectively.
