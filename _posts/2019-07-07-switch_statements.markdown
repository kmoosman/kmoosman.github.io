---
layout: post
title:      "Switch Statements"
date:       2019-07-07 21:31:45 +0000
permalink:  switch_statements
---


For my final blog I wanted to write about switch statements. There is one particular use of switch statements that I find myself using again and again and I often have to look it up each time. 

So I thought I'd take a second to document it here to come back to for easy reference and to help others who may find it useful. 

I often want to use a switch statement instead of an if else when I want to evaluate different expressons. In this example, I don't want to check if i is equal to a specific number, I want to check if the statement I write is true.  

Below is an implimenation of how to write a switch statement that evaulates to true, adding additional flexibility to the switch statement. 

```
var score = 82
var handicap = 20

switch (true) {
    case score >= 90:
    console.log("You're in the top of the field")
    break;
		
    case score <= 50:
		console.log("Practice a bit and try again")
    break;
		
    case score >= 70 && handicap > 10:
		console.log("Keep up the good work")
    break;
		default:
    console.log('We still need your scores');
```
