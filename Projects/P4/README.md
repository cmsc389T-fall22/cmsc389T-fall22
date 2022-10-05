# Project 4: PacMan CI

Due: 10/19, 11:59pm EST

Late: 10/26, 11:59pm EST

## Before You Start

Make sure you have completed P3 before you start this project.

**This project will require collaborating among 2 teams (8 people)**. Some key initial steps to take are,

- Create cards for Part 1, 2, and 3 and assign deadlines. **This should be compled during class on 10/05**
- Ensure that you communicate with the team you have been paired with. **A slack channel for both teams will be created. We strongly encourage you to use it**
- Each team will need to complete Part 2 before the other team can fork their repository. The deadlines on your cards will help communicate this.

## Team Pairings

- Teams 1 and 3
- Teams 2 and 4
- Teams 5 and 7
- Teams 6 and 8
- Teams 9 and 10

## Introduction

**READ THE BEFORE YOU START SECTION BEFORE CONTINUING**

In this project, you will adding Continous Integration pipelines to your PacMan project. This project has three parts:

- GitHub Actions - FTR-actions
- Sabotage - FTR-sabotage
- Good Samaritan - FTR-fix

Instead of creating a feature-item branch for each function, create one for each member:

```
├── FTR-actions
│   ├── actions-sagar
│   ├── actions-nandhini
│   ├── actions-joe
│   ├── actions-may
...
```

## Part 1: GitHub Actions

**Only one person** from each team needs to take the following steps:

1. Create 2 Feature branches, `FTR-actions` and `FTR-sabotage`, from the `main` branch
2. Checkout a new branch from the `FTR-actions` branch that is titled `actions-setup`
3. Add a `main.yml` file to your feature-item that uses the `openjdk` image and compiles all of your files
4. Create a pull request, add a reviewer, and have the reviewer merge the feature-item to `FTR-actions`

Once the steps above have been completed, you should be able to see a workflow show up on the Actions tab on GitHub. Now that the project is configured to work with GitHub Actions, each team member should

5. Create a feature-item branch `actions-{your_name}` (as shown above)
6. Modify the `main.yml` file to include a job for each test that you wrote
7. Create a pull request, add a reviewer, and have the reviewer merge your feature-item to `FTR-actions`

Once all feature-items have been completed

8. Submit a pull request to merge `FTR-actions` with the main branch
9. Add all group members as reviewers
10. Once the merge is complete, you should be able to see all of your jobs passing on the Actions tab

**Note** Your tests must run be able to run headless (i.e. without a Java Display). Make sure to include the `-Djava.awt.headless=true` flag when running tests both locally and on Actions. You should also use the **NoFrame** class instead of the MainFrame class to avoid a `java.awt.HeadlessException`. It has the same functionality as MainFrame but it doesn't create a JFrame for the display.

## Part 2: Sabotage

<p align="center">
<img src="https://i.redd.it/n0cz029px3q51.jpg"/>
</p>

1. Checkout a new branch from the `FTR-sabotage` feature branch that is titled with `sabotage-{your name}`
2. Change your **function** so that it will fail the test you wrote previously. **Do not change your test**
3. Create a pull request, add a reviewer, and have the reviewer merge your feature-item to `FTR-sabotage`

**Any 'mistakes' that you have intentionally made MUST be reversible**

Once the steps above have been completed, your team should

4. Submit a pull request to merge `FTR-sabotage` with the `main` branch
5. Add all group members as reviewers
6. Once the merge is complete, check that all of your tests are now failing on the Actions tab

## Part 3: Good Samaritan

<p align="center">
<img src="https://wallpapercave.com/wp/wp7559354.png"/>
</p>

Now its time to fix these sabotages!

You and your team will be assigned a sabotaged repository of another team. You must fork the repository, identify the mistakes and fix the code.

Only one person from each team needs to

1. Fork the assigned repository
2. Create a feature branch titled FTR-fix
3. Give your team access to collaborate on the repository (including your assigned TA!)

Once the repository has been forked, the team should

4. Analyze the tests failing the issues
5. Divide and conquer the necessary fixes (you may want to fix the same functions you sabotaged in Part 1 and wrote for Project 2)

Each member should

6. Create a branch that is titled `fix-{your_name}` and fix the issues
7. Create a pull request, add a reviewer, and have the reviewer merge your feature-item to `FTR-fix`

Once all members have made their changes,

8. Submit a pull request to merge `FTR-fix` with the `main` branch
9. Add all group members (of your own team) as reviewers
10. Once the merge is complete, check that all of the tests are passing on the Actions tab

After FTR-fix has been merged with main, one person from each team needs to

11. Open a pull request to merge the forked repository with the original repository
12. Add all members of the **other team** as reviewers to this PR

Finally, the other team needs to

13. Review the pull request and merge the forked repository with the original repository

## Academic Integrity

Please **carefully read** the academic honesty section of the course syllabus. **Any evidence** of impermissible cooperation on projects, use of disallowed materials or resources, or unauthorized use of computer accounts, **will be** submitted to the Student Honor Council, which could result in an XF for the course, or suspension or expulsion from the University. Be sure you understand what you are and what you are not permitted to do in regards to academic integrity when it comes to project assignments. These policies apply to all students, and the Student Honor Council does not consider lack of knowledge of the policies to be a defense for violating them. Full information is found in the course syllabus, which you should review before starting.
