# Testing-React

In this project, you will demonstrate proficiency by writing unit tests for an existing React application. Your tests should verify the behavior listed in the _Minimum Viable Product_ section.

Some of the topics covered were:

- Testing a React application.
- Using the `@testing-library/react` testing framework.
- Testing asynchronous calls made inside your React application

## Instructions

**Read these requirements carefully. Understand exactly what is expected _before_ starting.**

You are allowed, and encouraged, to collaborate with your peers while working on this assignment. Remember to follow the _twenty-minute rule_ and post questions to your cohort's help channel before seeking support from your PM and Instructor.

## Commits

Please push your code often and use descriptive commit messages, this helps you and your project manager.

## Project Description

In this project, you will **write tests** for an existing React application that queries data from the Star Wars API, and renders a list of Star Wars characters. The app also has buttons called `Next` and `Previous` to query the API again for the next or previous data sets. You will need to write tests for those buttons to ensure that they are working as expected.

## Project Set Up

Follow these steps to setup your git _fork_ and _branch_.

- [ ] Fork this repository.
- [ ] Use GitHub's website to add your project manager as collaborator on **your fork**.
- [ ] **Clone your forked version** of the repository (**Not Lambda's**!).
- [ ] Create a new branch: `git checkout -b <firstName-lastName>`.
- [ ] Commit changes to your `<firstName-lastName>` branch.
- [ ] Push often to your branch: `git push origin <firstName-lastName>`.

Follow these steps for completing your project.

- [ ] Submit a Pull-Request to merge the `<firstName-lastName>` branch into the master branch on your fork. **Please don't merge your own pull request**
- [ ] Use GitHub's website to add your project manager as a reviewer on the pull-request.
- [ ] Your project manager will count the project as complete by merging the branch back into the master branch of your forked repository.

## Note

The React app here was created with the latest version of `create-react-app` which now comes with `@testing-library/react` already included. When you create your own apps with the new CRA version, you won't need to add that library anymore!

## Minimum Viable Product

Your job is to write tests to ensure that the application behaves as expected.

## Stretch Problem

This section is **optional** and not counted towards MVP. Start working on it after you're done with the main assignment.

- Add a dropdown that has values for these strings: `'people', 'planets', 'starships', 'vehicles', 'species'`. When selected, the URL that is fetched will change to fetch the chosen data. Update your tests to test the dropdown input.





## !!!!!!!MVP!!!!!!!
## Questions:

## QUESTION 1: Explain (in detail) why automated testing is important to writing quality code. Provide a site of your choice and identify five items that what would be good to test, and why should it be tested (cannot include obvious tests like “did it render”, or “includes logo”). 
Automated testing is important to writing quality code because it helps developer/developer teams be proactive about bugs, errors and potential security issues during development instead of discovering them after the app has been deployed to the public. In a lot of ways I equate it to having scientific data/evidence to support your claim that the app does actually in fact work. Additionally testing can also help in making your code more re-usable and understandable to other developers.
The site I chose to examine is for S1 Helmets:
https://shop.s1helmets.com/
I would think that it'd be good to test the search function - 1. does the search pop up when you click the magnifying glass; 2. does the search form take an appropriate input and return information; and 3. given a search term does it return relevant search information.
The bag component would be another piece that would be a good candidate for testing: 1. do items get added when "add to bag" is clicked 2. does the total increase as an item is added, 3. and does it increase by the item price and not some other increment.
The add qty on an individual item could be tested by verifying if the qty increases or decreases on button click - 1. expect count to increase by one on click (fireevent.click); 2. does the appropriate qty get added to the cart with click of add to bag - if I add 2 of something does qty 2 get added to the bag.
Perhaps the menu could be tested - clicking on "Kneepads" from the menu would expect to display products/information containing Kneepads, vs directing to the helmets information.
Additionally, there could be other testing done regarding orders: testing that the "call" to get the order information of an already placed order works (async testing)


## QUESTION 2: Find a testing library other than Jest that would be good to use for automated testing. Back up your findings with code-snippets, or a working test. Ideally a library that has great, easy to understand documentation.
Mocha: https://mochajs.org/
I think Mocha could be a decent library as it has access to a lot of the same assertions we've been working with, expect(), should() etc.
It looks like it has a way to handle asynchronous testing, as well as other options. The big draw back I see is with arrow function (lambdas) testing, but it seems to be something that may be able to be avoided. I particularly like the hooks that can be used to further specify testing: before(), after() etc.