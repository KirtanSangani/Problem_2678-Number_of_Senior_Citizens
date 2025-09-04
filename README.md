# Problem 2678: Number of Senior Citizens

09/04/2025

## Thought Process
My initial thought process was very close to the final solution. I saw that the age was at the same place for all Strings in the list. So what I did was just looked at that specific index to see if that number was greater than 60.

##  Initial Solution
I created a count variable to count the number of senior citizens. Then I started a for loop to traverse through the list. For each element of the list, I created an if statement that essentially saw the first digit of the age (which was at index 11) to see if it was greater than 6. To account for ages 61-69, I included an or into the if statement looking to see if the age at index 11 was equal to 6 and the second digit of the age at index 12 was greater than 0. If this was to go True, I would add 1 to count. After the for loop, I would return count. What I did to account for the list being a String was to put the list elements in an int typecast (int(people[11])). This was so that I can compare it to the ints 6 and 0. 

Initial solution - 3 ms 

Complexity - O(N)

## Final Solution
Even though the first solution worked, I wanted to see if I can get it to run faster. To do this, I wanted to test the difference between the lines int(people[11]) > 6 and people[11] > '6'. So I got rid of the typecasting in the if statement and replaced it with single quotes around the 6 and 0. I ran this code and it was able to run in 0 ms. 

Final Solution - 0 ms

Complexity - O(N)

## Takeaways
The takeaway is that typecasting essentially slows the program down slightly so only typecast where necessary and if there is another way to get around the type disparity, then test that first.