# Study Planner

A single-page web application that helps university students plan work around
assessment deadlines and track their grades.

University coursework, Liverpool John Moores University. Awarded 90%.

## What it does

- Shows every coursework and exam deadline in a calendar view you can cycle
  through month by month
- Lets you add revision tasks with a description, optional resource link and a
  due date, sorted automatically by when they are due
- Flags anything overdue, and anything due in the next 30 days
- Takes your actual marks and works out your final module grade from the
  component and module weightings
- Lets you set a target classification and shows live visual feedback on
  whether you are on track for it
- Includes a study focus timer from 15 to 40 minutes with a sound at the end

## The part worth looking at

Most of the care went into input handling rather than features. Due dates are
rejected if they are in the past, marks are restricted to integers between 0
and 100, and any HTML tags typed into a task description are stripped before
the text is rendered, so a description cannot inject markup into the page.

Grade calculation reads the component and module weightings from the data file
rather than hardcoding them, so the maths stays correct if the assessment
structure changes.

## Running it

Open `index.html` with Live Server in VS Code.

## Note on data

The module and assessment data file was supplied by the university as part of
the brief and is not included here. The application reads it at startup.

## Built with

HTML, CSS, JavaScript and JSON. No frameworks, no build step.
