# Enara Health • Backend Interview • Time Tracker

_Version 1.1.0_

## This is a coding challenge for applicants interested in joining Enara Health as Backend Engineers.

We ask you to _read this file carefully_ **before** you begin writing a solution.

If you decide to continue with this process, **write us back WHEN** you expect to submit your solution before you begin implementing it.
This is really important so we can better arrange to wait for you, specially if you want to take a little bit longer.

If you decide NOT to continue with this process, let us know! ... So we stop spamming you with reminders.

We sincerely thank you for your interest and your time.

Best,
The Enara Health team!

## Submit the minimum posible

- You should **not implement features not required explicitely**.
- Coding more than required will waste your time, and waste our time. Please, don't.

## Challenge: Create an API server/application

Write a REST-ful API that allows to start and stop a timer to track time spent in different projects.
Each project has a unique text-based identifier (example `backend-interview`).

The API should offer 2 endpoins for tracking:
- Start the timer for project XYZ
- Stop the timer for project XYZ

The API should offer 2 endpoints for reporting:
- All projects: Report the list of projects and total time for every project
- **Extra goal**: One project: Report the total time and list the individual time segments for a project

### Pay attention to details

- The API should error with the corresponding code if the call is invalid (i.e. starting twice, ending twice, ending an unknown project).
- Report should only consider closed segments (ignore if the current time segment has started but it hasn't ended).

## Reporting output

Your API should output JSON results.

For all projects:
- List each project with its total minutes spent

**Extra goal**: For individual reports, you should include
- Total minutes spent in the project
- List of time segments (start-end) and minutes

## Code

- You can use any boilerplate or start project. If you need help with this, let us know and we will share a quick-starter project promptly.
- Keep your code **separated from the boilerplate**, so it's easier to review your work.
- We prefer TypeScript or typed JavaScript, or Ruby on Rails.


### Implementing your code

- Your app should satify the requirements above and follow a well defined API design.
- Your API routes should be documented (including parameters), implicitely (in code) or explicitely. 
- You can use any type of persistance (app memory, in-memory database, database engine, etc).

### Testing

- Describe your testing strategy.
- Implement a **single** test as an example of your testing strategy.
  - You can submit more tests if it is required to demonstrate different aspects of your strategy.

#### Example

In the following example, 2 projects are tracked:
```
curl ... # Start  tracking for project abc.
curl ... # End    tracking for project abc. (5 minutes later)

curl ... # Start  tracking for project xyz.
curl ... # End    tracking for project xyz. (15 minutes later)

curl ... # Start  tracking for project abc.
curl ... # End    tracking for project abc. (20 minutes later)
  
curl ... # List times for all projects:
                - 2 projects:
                    - abc ... 25m
                    - xyz ... 15m

# ** Extra points **:

curl ... # List times for project abc:
# Should list:  - Total 25 minutes
                - 2 segments:
                    - ... 5m
                    - ... 25m
```

---

## Submitting your work

Your deliverable should satisfy all these requirements:

- Describe what features you've implemented, included optional stretch goals.

- It should include _instructions on how to run_ (installing dependencies, starting it, etc) and it shouldn't have any obscure environment requirements.

- It should include _instructions on how to test_ (only **one test** is required).

- Describe your endpoints, and how to use them.

- It should be submitted via bitbucket.org or github.com repo (_Note: Do NOT clone our repo because other candidates can find it_).
  - _Note: Do NOT include `node_modules` or any other files that will be auto-generated_.

---

## Frequently asked question

- Q: Can I use external libraries (npm)?
  - Of course you can!
  - However, if some functionality is very easy to implement, try to implement it yourself (i.e. Don't install a library to figure out if a number is odd/even).
  - Choosing *when* to use libraries and *what libraries* you imported will speak about your judgement.
- Q: This coding challenge is too long. Is it OK if I implement it partially?
  - Although we recognize this exercise may take some time, it does measure if you have the skills we need to work together.
  - Submitting an incomplete solution is acceptable, specially if you explain the reasons.
  - However, a complete solution will increase the likelihood of being selected to continue our process, and it will save time during our in-person interview.

## Thanks for your time!

The Enara Health team!
