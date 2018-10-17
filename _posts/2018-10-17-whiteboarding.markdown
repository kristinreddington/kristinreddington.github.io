---
layout: post
title:      "Whiteboarding "
date:       2018-10-17 22:20:35 +0000
permalink:  whiteboarding
---


I think every developer can agree...whiteboarding is nerve-wracking. Standing in front of executives or senior level engineers with a given algorithm, a whiteboard and a marker, your first instinct is usually to whip out a solution to a memorized pattern in specific language. Having a couple of whiteboarding experiences now, I can say that the right way to handle whiteboarding is similar to how you would go about solving any problem. 

The first thing to remember is to take a deep breath. You don't have to come up with a solution right away. You're being tested on your problem *solving* skills, not how many patterns you've memorized. Coming up with a real-world, human interpretable way to approach the given problem is not only a logical way to start solving the algorithm, but it shows skills beyond coding and how you approach any problem. Once you can think of a situation, think about how you can break the problem into smaller sub-problems and solve each of those to result in a solution. 

Move from a verbal solution to pseudo-code. This may be the most important step because if you can reach a solution this way, you're halfway there. Once you're confident with the pseudo-code, translate it into your language of choice and finally, be sure to review your code for any bugs or misinterpretations. 

For example, if you're given an array of elements, (a list of activities, names, etc.) and parameters of an element to check if that element is within the given array, first think of a real-world example of this problem. If you've ever used a dictionary, this is the same issue we solve in every day life. If you have a word you're looking for, chances are, you're not going to start with the first word in the dictionary and scan the entire document until you've found your word. You would start somewhere in the middle, and if the word is alphabetically ordered higher than where you started, you would only look at the pages that follow where you started and repeat that process until you find the word. In order to follow this same procedure, you would firstly want a sorted array. 

Once the array is sorted, you can create three variables: one that represents the middle index of the array, one that represents everything to the left of that middle variable and another that represents everything to the right. 

If the element is less than the middle array's element, you can recursively call the algorithm with parameters of the element you're trying to find and the left variable array. Implement the same logic for a situation where the element is larger than the middle variable. Make sure to return the element you're trying to find. 

Approaching algorithms and whiteboarding in this way will calm your nerves and increase your confidence you're solving the problem correctly. If it makes sense in pseudo-code, your chances of being able to code it significantly increase. 

Lastly, don't forget to think outloud. This helps you organize your thoughts and helps your interviewers understand how you're approaching the problem and even help you if you're misinterpreting any instructions or syntax. 
