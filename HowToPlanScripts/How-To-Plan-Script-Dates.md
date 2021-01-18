# How-To Plan and Write a Script
A lot of online tutorials use super-basic examples to illustrate concepts. When I first started writing scripts, I would make connections to real-life use cases, but I worked somewhere that had a lot of different use cases begging for someone to automate something. 

I know a lot of people interested in learning how to write scripts can't find inspriation after watching an explainer and applying it to a real-life situation. 

## What is your idea?
I work in IT, and I'm constantly writing script that require me to manipulate dates. Sometimes I want to avoid sending out emails to people if it's a holiday. Our office follows that same holiday schedule as the NYSE, since a lot of our business is in the financial sector and we're in the city. I have tried a few different solutions for getting a current list of haliday dates (heretofore known as Holidates (c) tonypags 2021). I've tried to scrape the website, which worked but not for long. I've resorted to keeping a Get function with hard-coded dates. 

Whatever your idea is, write it down so that you can come back to it later to keep yourself on task. I don't know how many times I've had an idea, then started researching it only to find some other idea and before you know it I'm 6 feet down the rabbit hole and I forgot what my original idea was. Keeping a journal of your ideas is a good way to make them come to life. After all, an idea in your head is pretty worthless if that's where it's going to stay forever. 

My plan for today will be to create a new version of this function by manifesting dates based on the holidays themselves, instead of relying on a third party's website. These dates are common and easil calculated, so we're going to write logic to calculate the next holiday, and it's gonig to support observed days, if the holiday falls on a weekend. 

This project is a good example of a simple idea that can be broken down into logical steps. 

## What steps would you take to do this manually?
Do you need to copy files from one place to another. Do you need to find a line in a config file and change a false to a true, or a 0 to a 3? Do you need to download a file from a webpage? Are there any actions you have to take only if conditions are met? 

Write everything down and read it back to yourself. These should be instructions that anyone can use to perform your task without any other information. 

I want to consider the current date and find the next holiday on the NYSE calendar. For this I need a list of all of the holidays for a given year and how those are determined by society at large. 

## How would you describe these steps logically?
Think like a computer. You can't drag and drop a file from one folder to another in a script, but you can use cp or Copy-Item. You can't make an educuated decision about which files to move so that they are properly sorted in a script, but you can use a loop with an if statement. 

I want to calculate the actual "holidates" and then see if those dates are weekends or not. If they are I want to pick Monday or Friday instead of the actual date. 

## Write out your comments 
Convert your written instructions into logical statements, in English (or your native language). Keep everything very brief, one action per line. If you can separate your action into two, then do that. 

## Write Psudo-Code 
