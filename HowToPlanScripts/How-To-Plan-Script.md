# How-To Plan and Write a Script
A lot of online tutorials use super-basic examples to illustrate concepts. When I first started writing scripts, I would make connections to real-life use cases, but I worked somewhere that had a lot of different use cases begging for someone to automate something. 

I know a lot of people interested in learning how to write scripts can't find inspriation after watching an explainer and applying it to a real-life situation. 

## What is your idea?
I work in IT, but I'm also a pretty hardcore computer power user, too. And I watch a lot of TV and movies in my spare time. I use Plex at home for my media consumption. Plex has a movie preroll option that allows me to select short videos to show before a movie is played. It's a personalizatoin feature in the media server, and if you haven't heard about it before, it's not a terrible difficult concept to wrap your head around. 

Whatever your idea is, write it down so that you can come back to it later to keep yourself on task. I don't know how many times I've had an idea, then started researhin git only to find some other idea and before you know it I'm 6 feet down the rabbit hole and I forgot what my original idea was. Keeping a journal of your ideas is a good way to make them come to life. After all, an idea in your head is pretty worthless if that's where it's going to stay forever. 

My plan for today will be to create an automatic updater for my Plex Media Server's pre-roll list of video files. This is a list of semicolon-separated file paths that Plex randomizes and uses to play before a movie is shown. I've seen a version of this online written in bash, but I wanted to do a much more complex version, and use PowerShell Core to do it. 

I host my Plex server on a CentOS VM, but I plan to make the script compatible enough that someone with a Windows Plex server can also reuse my work. 

I've gone ahead and [downloaded](https://prerolls.video) a bunch of files I'd like to use as pre-rolls. There are some seasonal-themed ones like Christmas and Halloween, Winter and Summer. I have sorted them into folders based on when I'd like to show them: 
- 2020
- Autumn
- Christmas
- Classics
- Halloween
- Misc
- PlexBrand
- Spring
- Summer
- Winter

My idea is to select a portion of the videos in these folders based on the current date and time of day, and use that list to populate the pre-roll option. Basically I want Christmas stuff to play at Christmas time and I want to come up with rules for all types and seasons. Within the last few months I've gone into this setting to update it a few times and it's a real pain in the neck. 

This project has a little bit of everything: simple file/folder manipluation, loops and conditionals, and a slightly complex action that I need to do a bit of research to figure out. 

## What steps would you take to do this manually?
Do you need to copy files from one place to another. Do you need to find a line in a config file and change a false to a true, or a 0 to a 3? Do you need to download a file from a webpage? Are there any actions you have to take only if conditions are met? 

Write everything down and read it back to yourself. These should be instructions that anyone can use to perform your task without any other information. 

## How would you describe these steps logically?
Think like a computer. You can't drag and drop a file from one folder to another in a script, but you can use cp or Copy-Item. You can't make an educuated decision about which files to move so that they are properly sorted in a script, but you can use a loop with an if statement. 

## Write out your comments 
Convert your written instructions into logical statements, in English (or your native language). Keep everything very brief, one action per line. If you can separate your action into two, then do that. 

## Write Psudo-Code 
