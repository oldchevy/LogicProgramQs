# Logic or Programming questions
List of logic puzzles or programming questions that may show up in interviews

## Logic puzzles
#### The horses problem
There are 25 horses and your goal is to find the fastest 3 horses. You can race horses 5 at a time and compare their speeds relative to each other. How many races are needed to figure out the fastest 3 horses?

#### The 12 ball problem
There are 12 balls. All the balls appear identical to each other, but one of them has a different weight. How many weighings with a balance scale is needed to figure out which ball is the counterfeit AND determine if it's heavier or lighter than the other 11 balls?

#### The bucket problem
You have a 13 gallon bucket, an 18 gallon bucket, and an endless supply of water. You need to measure out exactly 1 gallon of water, using only these tools. How?

#### The locker problem
There are 100 lockers and 100 students. When a student visits a locker he will open it if it's closed, or he will close it if it's open. All lockers are initially closed. Student 1 visits every locker (so he will open them all). Student 2 visits every other locker (so he will close the 2nd, 4th, 6th...). Student 3 visits every third locker (so he will change the state of the 3rd, 6th, 9th...). This continues until all 100 students have had a turn with the lockers. Which lockers are still open? Can you write an algorithm to figure it out? In constant space?

#### The hat problem
100 prisoners stand in a line. A black or white hat is placed on each person. They don't know the color of their own hat or anybody's behind them, but they can see the hats of everyone standing in front of them. Starting from the back, a guard asks them for the color of their hat one by one. If they get it right they're free to go, otherwise they go to jail. What's a plan the prisoners can come up with (before they line up) to maximize their chances of guessing their hat color correctly?

#### 2 Player and N Coins
There are n coins in a line. (Assume n is even). Two players take turns to take a coin from one of the ends of the line until there are no more coins left. The player with the larger amount of money wins. Would you rather go first or second? Assume that you go first, describe an algorithm to compute the maximum amount of money you can win.
```javascript
/*
(Example) Coins: [18, 20, 15, 30, 10, 14]
First Player picks 18, now row of coins is: [20, 15, 30, 10, 14]
Second player picks 20, now row of coins is: [15, 30, 10, 14]
First Player picks 15, now row of coins is: [30, 10, 14]
Second player picks 30, now row of coins is: [10, 14]
First Player picks 14, now row of coins is: [10]
Second player picks 10, game over.

The total value collected by second player is more (20 + 30 + 10) compared to first player (18 + 15 + 14). So the second player wins.
Note that the strategy to pick maximum of two corners may not work.
*/
```

#### The lying neighbor
My next door neighbor lies a lot. In fact, he only tells the truth on one day of the week. One day he told me, "I lie on Mondays and on Tuesdays."
The next day he said, "Today is either Thursday, Saturday or Sunday."
The next day he said, "I lie on Wednesdays and Fridays."
On which day of the week does my neighbour tell the truth?

## Algorithms
#### Product Combination
Given an array of unique numbers, return an array of products from all possible combinations of three numbers.
```javascript
var numbers = [1, 3, 5, 9];

// 1 * 3 * 5 = 15
// 1 * 3 * 9 = 27
// 1 * 5 * 9 = 45
// 3 * 5 * 9 = 135

myFunction(numbers) = [15,27,45,135];
```

#### Rectangle intersection
Given two rectangles on a grid, return the area of overlap (or 0 if there is no overlap).
```javascript
var Rectangle = function(x, y, width, height) {
  // (x,y) represents the lower left corner
  // format coordinates as tuples
  this.LL = [x, y];
  this.LR = [x + width, y];
  this.UL = [x, y + height];
  this.UR = [x + width, y + width];
}

var rect1 = new Rectangle(0, 0, 3, 3);
var rect2 = new Rectangle(1, 1, 4, 1);

myFunction(rect1, rect2) = 2;
```

#### Find a dupe
You are given an array of length N that contain random integers from 1 to N-1 (inclusive). Write a function that will return a number that appears more than once in the array. There will always be at least one duplicate number in the array. Constraints: O(n log n) time complexity and O(1) space complexity, without mutating the original array.
```javascript
var list = [4, 1, 5, 2, 1, 2];

myFunction(list) = 1; // 2 is also an acceptable answer
```

#### Find Pivot
Given a sorted array that has been rotated, find the pivot point index. Constraint: O(log n) time complexity.
```javascript
var pivotArray = [5, 6, 7, 2, 3, 4];

myFunction(pivotArray) = 3 // the index of the pivot point
```

#### Water Towers
You are given a list of numbers that represents the heights of a line of towers. Each tower has a width of 1. It starts raining, and water will gather up between the towers. Write a function that calculates the amount of water collected.
```javascript
var towers = [5, 2, 3, 2, 1, 3];

// visualization:
// '-' is water
// '#' is a block
// 
// #
// #
// #-#--#
// ####-#
// ######

myFunction(towers) = 4;
```


#### Pascal's triangle
Write a function that returns n lines of Pascal's triangle
```javascript
// Pascal's triangle:
//         1
//       1   1
//     1   2   1
//   1   3   3   1
// 1   4   6   4   1
//        ...
```

#### 2nd largest node in a binary tree
Write a function that finds the second largest value in a binary tree

#### Sum pair
Given an unsorted array of integers and a sum value, write a function that finds the pairs of integers whose sum equals the sum value. There may be duplicate integers. Constraints: linear time complexity.
```javascript
myFunction([13, 13, 1, 1, 3, 4, 5, 8, 9, 10], 14) = [[1, 13], [1, 13], [4, 10], [5, 9]];
```

#### Distance between tree nodes
Find the distance between two nodes on a binary search tree (sorted) and on a binary tree.

#### Rectangle combinatinos
Given a N*M matrix, print all squares/rectangles of all possible sizes(all 1*1, then all 1*2…. 2*1… )