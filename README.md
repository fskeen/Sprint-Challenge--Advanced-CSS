# Sprint Challenge: Advanced CSS - Space Walkers Web Page

This challenge allows you to practice the concepts and techniques learned over the past week and apply them in a concrete project. This Sprint explored advanced CSS techniques using Responsive Design and Preprocessing. During this Sprint, you studied how to use the viewport meta tag, media queries, setting up a preprocessor, and advanced use of preprocessing techniques. In your challenge this week, you will demonstrate proficiency by updating a website that is missing content as well as adding mobile styling.

## Instructions

**Read these instructions carefully. Understand exactly what is expected _before_ starting this Sprint Challenge.**

This is an individual assessment. All work must be your own. Your challenge score is a measure of your ability to work independently using the material covered through this sprint. You need to demonstrate proficiency in the concepts and objectives introduced and practiced in preceding days.

You are not allowed to collaborate during the Sprint Challenge. However, you are encouraged to follow the twenty-minute rule and seek support from your PM and Instructor in your cohort help channel on Slack. Your work reflects your proficiency in advanced css and your command of the concepts and techniques in responsive web design and preprocessing.

You have three hours to complete this challenge. Plan your time accordingly.

## Commits

Commit your code regularly and meaningfully. This helps both you (in case you ever need to return to old code for any number of reasons) and your project manager.

## Description

The client for this challenge is _Spacewalkers Magazine_. Spacewalkers needs your help to build a small proof of concept website for their marketing team. They have provided designs for both desktop and phone views. In addition to designs and content they have most of the home page coded for you. You just need to finish the navigation and header as well as the mobile styles.

In meeting the minimum viable product (MVP) specifications listed below, your web page should look like the solution design files of the desktop and mobile views:

[Click here to review the home design](design-files/home-desktop.png)

[Click here to review the mobile design](design-files/home-mobile.png)

## Self-Study Questions

Demonstrate your understanding of this week's concepts by answering the following free-form questions.

Edit this document to include your answers after each question. Make sure to leave a blank line above and below your answer so it is clear and easy to read by your project manager

### 1. What is the difference between an adaptive website and a fully responsive website?


An adaptive design includes breakpoints designed for specific device sizes. At those breakpoints, a different fixed layout is applied, but the design itself isn't normally responsive the the screen space changing. (I.e. if you make the browser larger or smaller, the elements do not readjust themselves to that -- you just transition between different fixed layouts at breakpoints.)

Responsive design is, as the name suggests, _responsive_ to the change in screen space. When screen space changes, the elements rearrange or resize themselves based on the screen real estate. Responsive design creates a single design for all screens and adjusts that design to fit different screen sizes at different breakpoints. It will respond if you drag your browser larger or smaller.

### 2. Describe what it means to be mobile first vs desktop first.

Mobile first means designing for the minimum screen size (almost certainly a phone or some kind of smart device) and growing your design from smallest to largest. Desktop first means starting at what you think your site would look like at maximum width (what you'd see on a desktop monitor) and sizing your design down from there. There are advantages and disadvantages to both, and it will affect how you write your code.

### 3. What does `font-size: 62.5%` in the `html` tag do for us when using `rem` units?

It changes the default font size in browsers from 16px to 10px for easier math.

### 4. How would you describe preprocessing to someone new to CSS?

With vanilla CSS, you have the power to define the ENTIRE look for your website. Your HTML is the content, and your CSS is how that content looks -- are buttons blue or green? How large is the text? Where do you want people to see your navigation menu -- on the top or to the side? That kind of stuff. CSS is very powerful, but there's a catch if you're just using vanilla CSS: you have to define a lot of these things individually, by hand, and once you've done so, it can be hard to navigate the GIANT file you've made if you need to make changes. It's not wrong to say it's like looking for a needle in a haystack sometimes! This is where something called a "preprocessor" comes in.

A preprocessor makes it easier to write your CSS by doing some of the work for you. It lets you nest your CSS a lot like you nest your HTML, so it's easier to see what CSS applies to what HTML element. It's also just easier to navigate because all CSS is grouped by the element it applies to.

A preprocessor also allows you to separate your stylesheets so that you don't have to work in one long file. Imagine trying to find your way around a book that had no chapters -- you'd have to memorize the page numbers and make lots of notes so you knew where things were. Using separate stylesheets is like putting chapters in that book -- if you want to get to the "About Me" section, you don't need to memorize where it is, you can just open the "About Me" sheet (the "chapter").

Preprocessors can also let you store values in variables and mixins (which are like variables that hold more than one value). Storing values in a variable means you can store things like different color schemes or layouts in one place. Imagine you have a website and you want to change one font color that appears all throughout your website from pink to green. With vanilla CSS, you might have to change all those instances by hand, but if you make all those instances reference the "font color" variable, you can just change the variable and all those instances will change, too. 

### 5. What is your favorite concept in preprocessing? What is the concept that gives you the most trouble?

I actually feel pretty solid with preprocessors, so nothing is really giving me trouble.

I ADORE the fact that I can use variables and mixins now. I knew there had to be something like this, and I'm happy that I can use such a flexible tool to more efficiently make and design website. What _can't_ you do with variables and mixins?

You are expected to be able to answer all these questions. Your responses contribute to your Sprint Challenge grade. Skipping this section *will* prevent you from passing this challenge.

## Project Set Up

Follow these steps to set up your project:

### Git Set up

- [x] Create a forked copy of this project.
- [x] Add your project manager as collaborator on Github.
- [x] Clone your OWN version of the repository (Not Lambda's by mistake!).
- [x] Create a new branch: git checkout -b `<firstName-lastName>`.
- [x] Implement the project on your newly created `<firstName-lastName>` branch, committing changes regularly.
- [x] Push commits: git push origin `<firstName-lastName>`.
 
Follow these steps for completing your project.

- [x] Submit a Pull-Request to merge <firstName-lastName> Branch into master (student's  Repo). **Please don't merge your own pull request**
- [x] Add your project manager as a reviewer on the pull-request
- [ ] Your project manager will count the project as complete by merging the branch back into master.
 

### Preprocessor Set up

* [x] Verify that you have LESS installed correctly by running `lessc -v` in your terminal, if you don't get a version message back, reach out to your project manager for help.
* [x] Open your terminal and navigate to your preprocessing project by using the `cd` command
* [x] Once in your project's root folder, run the following command `less-watch-compiler less css index.less`
* [x] Verify your compiler is working correctly by changing the `background-color` on the `html` selector to `red` in your `index.less` file.
* [x] Once you see the red screen, you can delete that style and you're ready to start on the next task

## Minimum Viable Product

Your finished project must include all of the following requirements:

### Import LESS Files

* [x] Navigate to your `index.less` file. Notice the file is blank. You have been asked to use a certain import order. That order is as follows:

```markdown
1.variables.less
2.mixins.less
3.reset.less
4.global.less
5.navigation.less
6.footer.less
7.home-page.less
```

_You will know everything is working properly when you see the styles enabled for the provided content._  

### Home Page - Desktop HTML & LESS

* [x] Take 10 minutes to review the code that has already been provided for you. Take time to see how the home page was built.

* [x] Add a viewport meta tag to the head of your index.html page

* [x] [Review the provided home desktop design file](design-files/home-desktop.png). You are to build the missing navigation system and header image. You have been provided all content necessary in the [index.html file](index.html)

* [x] Navigation Styles: Use the `navigation.less` file for styling.

* [x] Main Content Styles: Use the `home-page.less` file for styling

* [x] LESS Mixins: Create and use 2 different mixins to aid your styling. Use the `mixins.less` file for your mixins

* [x] LESS Parametric Mixin: create a parametric mixin that is used to create the `sign up` button styles.

* [x]  Use at least 2 parameters to create your button

* [x] Create a hover state that swaps the background color and font color of the base button styles.

### Mobile Design

* [x] Create a `@phone` variable that contains a `max-width: 500px` media query string. Use the `@phone` variable for all your nested mobile styling.

* [x] [Review the provided home mobile design file](design-files/home-mobile.png). Match your mobile styling the best you can using the design file.

* [x] Push your changes and create a pull request if you haven't already.

In your solution, it is essential that you follow best practices and produce clean and professional results. Schedule time to review, refine, and assess your work and perform basic professional polishing including spell-checking and grammar-checking on your work. It is better to submit a challenge that meets MVP than one that attempts too much and does not.

## Stretch Problems

After finishing your required elements, you can push your work further. These goals may or may not be things you have learned in this module but they build on the material you just studied. Time allowing, stretch your limits and see if you can deliver on the following optional goals:

* [ ] Build a page of your choosing from the navigation items. Come up with content and images that fit the theme.

* [ ] Introduce CSS animations to your site.

* [ ] Create a fixed navigation and add some opacity to the background

* [ ] Create a form that would allow someone to sign up for a Spacewalkers Magazine subscription