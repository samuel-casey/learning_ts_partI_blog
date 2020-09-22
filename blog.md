# Learning TypeScript: Part I

This week, I built and deployed my first TypeScript project: a new [portfolio site](https://samcasey.life). Up until two weeks ago, I had only used JavaScript, JQuery, and React for web-development, but after watching [this video by Ben Awad](https://www.youtube.com/watch?v=bAB_nNf8-a0) where he mentions that after you learn TypeScript, developing in JavaScript will feel like "playing web-dev on hardcore mode", I decided it was worth learning. This blog covers how I've been teaching myself, what I've learned so far, and how I'm going to continue learning TypeScript.

## How I've been learning

I'm currently enrolled in a General Assembly (GA) Software Engineering Bootcamp. The focus of Unit 1 was HTML, CSS, and JavaScript. Given that I have a fair amount of experience with JavaScript, I decided to teach myself TypeScript alongside our JavaScript lessons. My workflow for teaching myself had four steps:

**1. Take notes during my GA lectures focused on the fundamentals data types of JavaScript, Object Oriented Programming, and ES6 syntax.**

- While I was doing this, I also had the TypeScript docs open on my other monitor so I could compare how data types work in JavaScript with how they work in TypeScript

Here's a snippet from my lecture notes on Arrays:

![Screenshot of Notes](https://res.cloudinary.com/scimgcloud/image/upload/v1600800329/images-for-blogs/Screen_Shot_2020-09-22_at_2.43.43_PM_xpmimb.png)

**2. Do my homework assignments in JavaScript first to think through the logic of the assignments.**

- I find it easier to focus on learning the idiosyncrasies of a new language or library when I don't have to think about both the new syntax and the actual application logic

**3. Refactor my homeworks into TypeScript**

- When I was first learning React, I started by rebuilding a tic-tac-toe game that I originally had built in JQuery, and found that process to be a great way of learning
  <br>
- This homework [a random tarot card generator](https://github.com/samuel-casey/random-tarot) is an example of one of the homeworks I refactored

**4. Google every single error I get and allow myself to go deep down rabbit holes while exploring solutions**

- Usually when I come across errors while developing, I look to find the quickest fix to my errors and keep moving forward once I find a fix
  <br>
- While learning TypeScript, however, I've been exploring multiple possible fixes, testing them more thoroughly, and making sure that I understand _why_ the solutions I find are fixing my errors, not just considering it "good enough" when I stop seeing error messages

## What I've learned so far

The main things I've learned about TypeScript so far is how beneficial it will be for building larger scale applications, and that I'm a fan. My portfolio site is built with TypeScript, Sass, JQuery, and a Google Sheets API, but even though it's small and serverless, building it with TypeScript allowed me to see some of the benefits of a strongly-typed language. Below are two examples of things I learned about TypeScript while building my portfolio site, and the issues I faced that led to me learning them.

**1. Type-checking is about more than just checking primitive data types (interfaces are a wonderful thing)**

- The projects and blogs listed on my portfolio site are stored in a Google Sheet, per the requirements of my GA assignment
  <br>
- When first making AJAX requests to the Sheets API, I attempted to assign object properties for each project/blog to a new object without defining an Interface for what a Project or Blog object should look like
  <br>
- This resulted in a series of errors as I got further in my code, and helped me fully understand the purpose and benefits of Interfaces

**2. Functions in TypeScript should to have an explicitly defined return type in order to harness the full benefits of using TypeScript**

- On my second go around with AJAX, after I had defined Interfaces for my Projects and Blog objects, I kept getting the error: `TS2355: A function whose declared type is neither 'void' nor 'any' must return a value`
  <br>
- The error arose when I tried to map the Array of entries in my Google Sheet to an array of ProjectSheetRow/BlogSheetRow objects
  <br>
- I originally solved the bug by setting the return type for my `.map()` callback to `any`, but after reading some Stack Overflow articles and the TypeScript docs, I realized that returning `any` from a function in my situation was a cop-out. You might as well use JavaScript if you're going to just return `any` from all of your functions
  <br>
- To fix this error, I returned {_object properties_} as ProjectSheetRow or BlogSheetRow, which were the names of my Interfaces

## Next steps in my TypeScript education

**1. Build a project with TypeScript + React**

- I was required to use JQuery for my portfolio site because of my GA assignment, but I don't think I'll ever use JQuery + TypeScript ever again, as React is a better front-end library
  <br>
- The next project I want to build in React will consume data from a public API, and display it without much manipulation. I'll be building this project mainly to bolster my React skills and learn the intricacies of this specific API, but I'm going to use TypeScript for it as well

**2. Build a fullstack project using TypeScript**

- TypeScript is great for front-end development, but I'm most excited to start using it for the backend. A few months ago, I built an [app to help visualize realtime tide-levels](https://tides-vis.herokuapp.com) at any beach around the United States which probably would have been much easier in TypeScript.
  <br>
- The app is built in JavaScript, uses two APIs, and a Postgres database to find the closest beach that has reliable tide-level projections to any user-inputted location.
  <br>
- When writing the function to compare the timezone from the user's inputted location to the list of tide stations in my database, I spent hours debugging an issue that stemmed from me trying to compare a `number` to a `string`. If I had been using TypeScript for this project, I probably would have discovered this error sooner and saved myself a lot of time and a major headache.

**3. Get involved in the TypeScript community online**

- I'm certain there are still things I do not fully understand about TypeScript yet, and while I'm confident in my abilities to teach myself new concepts, I think I'll learn much faster with help from others. I plan on posting StackOverflow questions, commenting on some Dev.to blogs about TypeScript, and eventually contributing to an open-source TypeScript project.

In conclusion, if you're reading this blog and have any suggestions for how to become a TypeScript pro, or want to hear more about my TypeScript journey, please reach out! My dms are open on twitter [@\_samcasey](https://twitter.com/_samcasey), and I welcome any comments on this blog as well.
