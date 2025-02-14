# Project 3: Full-Stack Game

## Introduction

This app is a continuation of [Project 2: Server Side App](project-2-server-side-app.md). We are spreading the logic and computation across 2 computers, the server computer and the user's computer. The underlying mechanic of request and response happening across the network is still the same.

You will implement a card game or turn based card-type game. The user or users will be identified by the system and be able to play a game where the server remembers something about the user and the game cannot be cheated by opening the browser dev tools.

## Requirements

1. Features
   1. Single or multi player is ok
   2. The gameplay should happen on a single HTML page
   3. Interactivity using client-side JS
   4. Users cannot cheat by looking in the browser console
   5. Some game state must be saved in the database server-side
   6. User login \(full-stack or server-side\)
2. Technologies
   1. Use CSS
   2. Use Express.js
   3. Use Webpack

The game you implement does not have to have a score or winners. It must be completely playable for the stated rules. i.e., if a rule of the game is stated, the game must implement it.

If you choose to implement a card game with a known set of rules, you as the game implementer can state a lesser set of rules if you want.

Note that you can choose to implement user authentication completely in AJAX requests, or you can choose to implement user authentication as in Project 2, where the user is restricted from visiting the game page.

Your app must be complete in the sense that it cannot rely on the theoretical existence of another system, e.g. an API that doesn't exist. You are free to use any 3rd-party APIs available on the internet, e.g. NPM libraries.

## Starter Code

Consider starting with this starter repo: [https://github.com/rocketacademy/webpack-mvc-base-bootcamp](https://github.com/rocketacademy/webpack-mvc-base-bootcamp). Don't fork the repo because we may be using it for multiple projects and exercises. You can copy the code to a new repo, or clone it and remove the `.git` directory to create a new repo.

## App Ideas

### General Ideas

Here is a list of card games: [https://bicyclecards.com/rules/](https://bicyclecards.com/rules/)

Also acceptable are turn based board type games such as Battleship or Connect Four.

Avoid any ideas the depend on timing between players or if another player must be immediately notified of some game state.

## Project Timeline

### Summary

<table>
  <thead>
    <tr>
      <th style="text-align:left">Course Day</th>
      <th style="text-align:left">Deliverable</th>
      <th style="text-align:left">Instructor Feedback</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">CD10.3</td>
      <td style="text-align:left">
        <p><b>Start: Ideation Phase 1.</b> 
        </p>
        <p>Introduce project, post project ideas in Slack for feedback</p>
      </td>
      <td style="text-align:left">Instructor to share feedback on project ideas in Slack.</td>
    </tr>
    <tr>
      <td style="text-align:left">CD11.1</td>
      <td style="text-align:left">
        <p><b>Start: Ideation Phase 2. </b> 
        </p>
        <p>Create planning docs: user stories, wireframes, and DB ERD.</p>
      </td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">CD11.3</td>
      <td style="text-align:left">
        <p><b>Due: Ideation Phase 2. </b> 
        </p>
        <p>Finalise project idea and share planning docs in GitHub repo over Slack.</p>
      </td>
      <td style="text-align:left">Instructor to review planning docs over Slack and over Zoom if necessary.</td>
    </tr>
    <tr>
      <td style="text-align:left">CD11.3</td>
      <td style="text-align:left"><b>Peer Planning Review.</b>
      </td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">CD11.3</td>
      <td style="text-align:left"><b>Start: Project Start.</b>
      </td>
      <td style="text-align:left">Begin Project Implementation</td>
    </tr>
    <tr>
      <td style="text-align:left">CD12.3</td>
      <td style="text-align:left">
        <p><b>Due: MVP deadline.</b> 
        </p>
        <p>Users should be able to perform the primary user story. Please deploy
          your app to Heroku. Students to review code in pairs during class.</p>
      </td>
      <td style="text-align:left">Instructor to review code on GitHub, share feedback in Slack and Zoom
        if necessary.</td>
    </tr>
    <tr>
      <td style="text-align:left">CD12.5</td>
      <td style="text-align:left">
        <p><b>Due: Feature freeze.</b>
        </p>
        <p>No more developing new app functionality. Use remaining time to focus
          on polish, i.e. fixing UX/UI, refactoring code.</p>
      </td>
      <td style="text-align:left">Quick project review in class to discuss improvements post-feature freeze.</td>
    </tr>
    <tr>
      <td style="text-align:left">CD13.2</td>
      <td style="text-align:left"><b>Due: Project presentations.</b>
      </td>
      <td style="text-align:left">30-minute post-mortem with instructor. Instructor to review code in PR
        on GitHub.</td>
    </tr>
    <tr>
      <td style="text-align:left">CD13.3</td>
      <td style="text-align:left"><b>Project Peer Review exercise.</b>
      </td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">CD13.5</td>
      <td style="text-align:left"><b>Due: Video demo.</b>
      </td>
      <td style="text-align:left"></td>
    </tr>
  </tbody>
</table>

### Recommended Order of Implementation

Implement the core user story first. What are users coming to your app to do? Make sure they are able to accomplish that, before adding authentication and nice-to-have features.

1. CRUD functionality
2. Login functionality
3. Any stretch functionality, e.g. AI APIs or file uploading

## Ideation Phase 1

Brainstorm app ideas. What problem does the app solve, for whom? How does the app solve the problem? What data does the app handle?

## Ideation Phase 2

Plan the app implementation with the following planning docs.

1. [User-flow diagram](https://careerfoundry.com/en/blog/ux-design/what-are-user-flows/)
2. Wireframes of minimal UIs that enable our user flows
3. Database ERD to support our user flows and wireframes.

Save these planning docs in a project GitHub repo and share it in Slack. Instructors will review these planning documents with you before you begin implementation.

## MVP Deadline

A user should be able to play the game through once without encountering errors. App should be deployed to Heroku. Peer code review during class.

## Feature Freeze

The app and all its features should run without errors. Brief demo in class to demonstrate user experience and clarify work to do before presentations. Latest app should be deployed.

## Project Presentations

Presentations should cover the [topics in this list](../course-logistics/course-methodology.md#project-presentations).

## Post-Mortem Meeting

Please answer the [project post-mortem questions](../course-logistics/course-methodology.md#project-post-mortem-meeting) before the post-mortem meeting with your instructor. These questions will be similar to the presentation questions, but we will dig deeper into your code.

## Video Demo

Please follow [video demo guidelines here](../course-logistics/course-methodology.md#project-videos).

