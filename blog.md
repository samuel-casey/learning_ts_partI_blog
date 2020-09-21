# Learning TypeScript: Part I

This week, I built and deployed my first TypeScript project: a new [portfolio site](https://samcasey.life). Up until two weeks ago, I had only used JavaScript, JQuery, and React for web-development, but after watching [this video by Ben Awad](https://www.youtube.com/watch?v=bAB_nNf8-a0) where he mentions that after you learn TypeScript, developing in JavaScript will feel like "playing web-dev on hardcore mode", I decided it was worth learning. This blog covers how I've been teaching myself, what I've learned so far, what I like about TypeScript and how I'm going to continue learning TypeScript.

## How I've been learning

I'm currently enrolled in a General Assembly (GA) Software Engineering Bootcamp. In Unit 1, which we just completed, we were taught HTML, CSS, and JavaScript. Given that I have a fair amount of experience with JavaScript, I decided to teach myself TypeScript alongside our JavaScript lessons. My workflow for learning was as follows:

**1. Take notes during my GA lectures focused on the fundamentals data types of JavaScript, Object Oriented Programming, and ES6 syntax.**
   <br>
   - While I was doing this, I also had the TypeScript docs open on my other monitor so I could compare how data types work in JavaScript with how they work in TypeScript
    <br>

**2. Do my homework assignments in JavaScript first to think through the logic of the assignments.**
<br>
**3. Refactor my homeworks into TypeScript**
   <br>
   - When I was first learning React, I started by rebuilding a tic-tac-toe game that I originally had built in JQuery, and found that process to be a great way of learning
   <br>
   - I find it easier to focus on learning the idiosyncrasies of a new language or library when I don't have to think as much about what I want the application to actually do as well
   <br>
   - This homework [a random tarot card generator](https://github.com/samuel-casey/random-tarot) is an example of one of the homeworks I refactored
    <br>

**4. Google every single error I get and allow myself to go deep down rabbit holes while exploring solutions**
   <br>
   - Usually when I come across errors while developing, I look to find the quickest fix to my errors and keep moving forward once I find a fix
   <br>
   - While learning TypeScript, however, I've been exploring multiple possible fixes, testing them more thoroughly, and making sure that I understand *why* the solutions I find are fixing my errors, not just considering it "good enough" when I stop seeing error messages

## What I've learned so far

The main things I've learned about TypeScript so far is how beneficial it will be for building larger scale applications, and that I'm a fan. My portfolio site is built with TypeScript, Sass, JQuery, and a Google Sheets API, but even though it's small and serverless, building it with TypeScript allowed me to see some of the benefits of a strongly-typed language. Below are two examples of things I learned about TypeScript while building my portfolio site, and the issues I faced that led to me learning them. 

1. Type-checking is about more than just checking primitive data types (interfaces are a wonderful thing)
    <br>
   - The projects and blogs listed on my portfolio site are stored in a Google Sheet, per the requirements of my GA assignment
    <br>
   - When first making AJAX requests to the Sheets API, I attempted to assign object properties for each project/blog to a new object without defining an Interface for what a Project or Blog object should look like
    <br>
   - This resulted in a series of errors as I got further in my code, and helped me fully understand the purpose and benefits of Interfaces

2. 

## What I like about TypeScript

TypeScript is great because it helps you catch errors earlier in the development lifecycle, can make it easier to remember how your code works when returning to it later, and _____.

## How I'm going to continue learning TypeScript
