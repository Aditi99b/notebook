---
toc: True
comments: False
layout: post
title: Collegeboard MC Reflections 
description: Student teaching
type: tangibles
courses: {'compsci': {'week': 12}}
---

## Question 1
- QUESTION: Which of the following expressions represents the value stored in the variable x as a result of executing the program?
- CORRECT ANSWER: 2 * 3 * 3 * 3 * 3
- EXPLAINATION: My answer was wrong because it would only be true if the loop header was changed to REPEAT 3 TIMES. Instead the right answer was correct because the program initializes x to 2, then multiplies it by 3 a total of four times.

## Question 4
- QUESTION: In a certain computer program, two positive integers are added together, resulting in an overflow error. Which of the following best explains why the error occurs?
- CORRECT ANSWER: The program can only use a fixed number of bits to represent integers; the computed sum is greater than the maximum representable value.
- EXPLAINATION: This is because computers represent integers using a fixed number of bits, and there is a limit to the maximum value that can be represented with a certain number of bits. When the sum of two positive integers exceeds this maximum representable value, an overflow error occurs, meaning that the result cannot be accurately represented within the given number of bits.

## Question 18
- QUESTION: Which of the following replacements for CODE can be used to move the robot to the gray square?
- CORRECT ANSWER: B
- EXPLAINATION: This is the correct answer because it moves the robot forward whenever there is an open square in front of it. Once there is not an open square in front of it, the robot rotates right. The robot moves forward from its initial location to the upper right corner of the grid, then rotates right, then moves forward to the bottom right corner of the grid, then rotates right, then moves forward to the bottom left corner of the grid, then rotates right, then moves forward two squares to the gray square.

## Question 30 
- QUESTION: Which of the following is NOT a possible value displayed by the program?
- CORRECT ANSWER: out of range
- EXPLAINATION: This is the correct answer because the string "out of range" could only be displayed if the condition n ≥ 1 was false. If the initial value of n is at least 0, then n will be incremented by 1, making n at least 1. Therefore the condition n ≥ 1 will be true and "out of range" will not be displayed. If the initial value of n is negative, then n will be multiplied by -1, making n at least 1. Therefore the condition n ≥ 1 will be true and "out of range" will not be displayed.

## Question 34
- QUESTION: Which of the following code segments will move the robot to the gray square along the path indicated by the arrows?
- CORRECT ANSWER: C
- EXPLAINATION: This is the correct answer because in this code segment, the first call to BotMover moves the robot forward one square, rotates it right one time so that it faces right, and moves it forward one square. The second call to BotMover moves the robot forward one square, rotates it right 3 times so that it faces toward the top of the grid, then moves it forward one square. The third call to BotMover moves the robot forward one square, does not rotate it, then moves it forward to the gray square.



