# **Lab Report 5**
by Eduardo Lopez

## Part 1:
## 1.1(Student Question): 
![Image](image1.1.png)

Hello my name is Eduardo, I am having trouble figureing out what's creating this failure on my code. The Junit test says my ListExamples.java file is failing a test relating to a TestTimedOutException. I have a feeling it's related to the merge method where something isn't adding up or merging correctly resulting in the Junit test timing out. 

## 1.2(TA Response):
Hello Eduardo, thank you for making your question private. From the looks of the symptom, there is a timeout error meaning a possible while loop condition isn't being met, resulting in an infinite loop. With that in mind, take a look at your while loops. What would need to be done in order for the while loop or loops to eventually break(conditions met) and return the proper results.

## 1.3(Student Response):
![Image](image1.22.png)
![Image](image1.3.png)

Thank you. I found the bug. It makes sense why there would be a timeout error. The conditions of my last while loop in my method would have never been met because instead of updating index2 of the second list for the loop, I was updating the index1 which was already being done with the while loop above it. That's why the loop never broke because the proper indeces weren't even being updated/iterated for it to move onto the next index on the second list. 

## 1.4(Information):
File and Directory Structure:
![Image](image1.4.png)
![Image](image1.5.png)

Contents of each file before fixing bug:
``

``

Commands ran to trigger bug:
``

``

What to edit top fix bug:
