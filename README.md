# Single Page Phasmophobia Nightmare Journal

## Table of Contents
1. [Introduction](#Introduction)
2. [Installation](#Installation)
3. [ethos](#Ethos)
4. [SoftwareGuideBook](#Software)
5. [Personal aspect](#Personal-aspect)
6. [End](#Conclusion)

## Introduction
This page is meant to help with nightmare mode in the video game [Phasmophobia](https://www.kineticgames.co.uk/phasmophobia)

## Installation
Simply download the HTML file and run it in the browser of your choice. You can open it by simply dubbel clicking on it.
> note: if it does not open in a browser instead of dubbel clicking you can open it by right clicking and selecting "open in" and then selecting your favourite browser.

## Ethos
This software had a few core philosophies:
### Single page application.
For user convenience and accessbility this program was meant to be a single file. This means that the CSS, JS, HTML and other data is all in the same file. 
### Semi-experienced Users
The usage of the page is obviously meant to aid in Phasmophobia, but it is not meant to help people who are new at the game, simply people who already understand the basics but don't know every ghost indepth by heart.
### Offline accessible
Since this is supposed to help a single person in a game that can be played offline the page is required to not only work without wifi but not use any online resources. The only exception made to this is the font.
### Looks like the game
The looks of the page are meant to be similar to that of the game. However this is made harder due to the fact we cannot use other files since it is a single page or use online resources for offline accessibility. 

## Software

### Discounting ghost
In the table shown under we have on the top the evidence values: -1 means it's discounted, 0 means unknown and 1 means its proven
On the left we have the evidence of the ghost values: 0 means it does not have it, 1 means it does, 2 means it is required
|   | -1 | 0 | 1 |
|---|----|---|---|
| 0 |    |   | X |
| 1 | ?  |   | ? |
| 2 | X  | ? |   |

The X means that in that case they are discounted. 
- (1,0) we have an evidence that the ghost does not have
- (-1,2) We discounted an evidence the ghost needs
- Empty space means we don't need to do anything
- The question mark means we might need to do something: A ghost can have evidences hidden which means it will have 2 out of 3.

So in this example we only look at ghosts with 3 evidences and one will be hidden.
First we look at a ghost that does not have required evidence
If 2+ of their 3 evidences are discounted it means it cannot be that ghost since at least 2 need to be proven.
Then if a ghost has a required evidence if the 2 evidences that are not required are proven it means it cannot be the ghost
since there wont be a third proven evidence so the required evidence is impossible, this means it cannot be the ghost.
The code for this is quite simple: does it have required and is the required evidence unknown then we look. How many correct evidences does it have correct. The max is how many evidences it has - the amount of hidden evidences - 1. 

### Booting up
Since this game is still actively worked on and updated. (for example the first version of this tool had 6 less ghosts) we need to make sure we can update and add new data easily, for this we save the data of the ghosts in an array and generate the HTML based on that. Same goes for the evidences tho it is unlikely to be changed.


## Personal aspect
This project started because despite there being many similar tools, none were what I wanted. I decided that I would make my own version that would have a focus on overview, simplicity and ease of use. I used the previous version of this tool for many many games and it proved very useful. After a few updates to the game, new ghosts and more experience I decided to start from scratch with the project and see where I would end up. While a lot of concepts and principals stayed the same everything else changed. The code is more readable, the UI is more immersive and the ghost info is up to date. This is a passion project of mine where I want to be able to use everything I learned in code. As such I will start using this tool myself the most but I hope that others can also find it useful.

## Conclusion
This program was written soley by Blossom with no AI used.
