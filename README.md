## LeetCodeNotes
## My Own LeetCode Notes (Most are written in Python and C) :)
#### This project includes all my thoughts while I am solving problems. I would not say my solution is the best and beat 99% of the submission, I aim to solve the problems in reasonable time.
#### Find Problems [here](https://leetcode.com/problemset/all/)
### 1. Two Sum:
#### Given a list of nums and a target, return a list where contains two digit whose sum is equal to target.
#### e.g.[1, 2, 3, 4] target = 7.

1. Create a [dictionay](https://docs.python.org/3/tutorial/datastructures.html)[Dictionary is very useful data structure you may use it from time to time].
2.   For each digit y in list, cast it as value in dictionary, and caculate number x as key to that key so that x + y = target e.g. {"6": 1, "5": 2, "4": 3, "3": 4} [{"key": vale}]. 
3. Use for loop to generate a dictionary, once you found digit y exists in dictionary as a key, you found the demand pair. You can simply return [dict[x], i]

### 2. Add Two Numbers:
#### Given two linked list, each linked list representing two non-negative integers but in reverse order.
#### [2->3->4 stands for 432] you need add thoses two integers and represent result in linked-list in reverse order. 
#### [(2 -> 4 -> 3) + (5 -> 6 -> 4) result: 7 -> 0 -> 8. 342+564=807] 
#### Personal speaking, I would use C to implement this. But using Python to implement linked list worth trying. Because you probably never use python to create class or struct in school.

The implementation is quite straight forward. 
1. First, parallelly go through each node in LL1 and LL2
2. Add two node up, if the sum is greater than 9, there is carry. To track carry digit, use module to get the last digit. (21/10 = 1, carry is 2). Then put the last digit into result Linked-list.

### 3. Longest Substring Without Repeating Characters
##### I just realize I should include my bad approach so that you can avoid it.
#### Given a string, you need to find the length of longest substring which does not contain repeated characters: 
#### e.g.["pwwkew" return 3("kew")]
#### Again, I use dictionary to implement this. 

1. First of all, you need a mark M to track the first character without any repeating character before it. You need to dictionary to check if there is a character exists in previous substring. 
e.g.["abba", {"a": 0} -> {"a": 0, "b": 1} -> in the third iteration, program would add the index of the second "b" to dictionary, but dictionary already has "b" in it. So you need to store this b's index and assign it to M] 
2. The length of current valid substring can be written as [i-M +1 why plus one? I think you can figure out by yourself].
3. Since this problem requires the length not the substring, you can simply compare the current length to maxLength for each iteration.

### 4. Median of Two Sorted Arrays
#### I do not even know how I made it work. BRB
