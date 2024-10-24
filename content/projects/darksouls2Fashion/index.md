---
title: "Dark Souls 2 Fashion Viewer website."
description: "Hosting Apelabs website using Hugo/Blowfish and GitHubPages"
tags: ["new", "webDev"]
#series: ["Website Documentation"]
date: "2024-08-28T00:00:00"


---
{{< lead >}}
A website project to create an armour viewer for DS2
{{< /lead >}}

---

## What is it?

In its simplicity, it's a JavaScript and PHP website that displays images of different armor pieces overlayed on top of each other.  
With this, I can create a simple and fast way of seeing how different armor pieces look together.

## Getting the images of the armor

Here I ran into a bit of a dilemma: how could I do this without taking too much of my free time, which I could be spending procrastinating?  
In *Dark Souls 2*, there is thankfully a window where you can look at your character, and they always have the same pose.  
So I decided to use that to my advantage. I started by taking screenshots while wearing different pieces of an armor set: boots, gloves, chest, and head. Then I made a Python script that goes through these screenshots and crops them to only include the character.  

Then I ran into the issue of actually cropping the armor by hand. I had to meticulously go through each screenshot and crop the armor piece out so I could make it into an image that I could overlay on the character. I soon realized this would take too much time.

## How to improve my workflow?

I started thinking of ways to make my job easier and faster.  
First, I realized if I could make the background of the character in the window a solid color, cropping would become much easier. So, I did just that. How, you might ask? Simple—I used a tool to decompile the whole game, looked through the texture files, and after an embarrassing amount of time, I found the right texture. I painted it solid green, and it worked.

After that, I had the idea of using AI to crop the character off the green background, reducing my workload. I made a Python script that used some AI libraries, and I wrote it to crop out the green background. Honestly, it works great.  
This is still in progress, and I've cropped about 50% of the sets in the game.

## The website

I wanted the website to be simple: four different lists on the left side to choose from—head, chest, gloves, and boots—and the character being displayed on the right. Picking an armor piece from the list would display it on the character.

I wrote a PHP script using JavaScript to dynamically display the data from the database (armor images). This means that the moment the user picks an item from the list, it appears on the display. After making that work, I began creating a script to help me populate the database.

## MySQL Database

I decided on a simple MySQL implementation. I used AI to generate a list of all the armor sets in the game, categorized into different lists. 
{{< screenshot src="gptList.jpg" alt="ChatGPT generated list" >}}

After a few iterations, I managed to get all the armors into four different lists: head, chest, gloves, and boots. Nice. Now I have a simple script that goes through the data and populates the database with the correct armor, along with its corresponding name and picture.

---