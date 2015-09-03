# dimeSocial-best-practices
best practices &amp; process outlines for development at dimeSocial.

## Statement of Purpose
This document is born out of a need to create process standards at dimeSocial, shorten development cycles, enhance codebase quality, eliminate communication issues, keep the team on the same page, and ensure long-term codebase viability. By creating a culture of engineering, we will achieve not only superior codebase quality and efficiency, but will learn best practices that can apply to our future endeavors as well!

## Scope of this Document
There are a two key areas for which this document attempts to develop standards.These are **project management** and **code review** procedures at dimeSocial. This document does not attempt to define standards for any other practice, procedure, or system; however, team members are encouraged to submit as issues any suggestions, additions, or improvements that could be made to this document (see Contributing to this Document). There is no potential limit to the scope of this document; however, it is meant primarily as a means of organizing our efforts and maximizing our efficiency as a dev team. Other team members are encouraged to utilize the spirit of this document to create standards for their own projects and tasks. 

## Contributing to this Document
Any member of the dimeSocial team is allowed to submit suggestions for improvements to this document. The process for doing so is as follows: First, open an issue, being as descriptive as possible. It's imperative that you add tags like 'enhancement', 'invalid', or something relevant that clearly denotes the type of issue you are creating. Your issue will be reviewed by the person in charge of administering this document (hereafter referred to as 'admin') - currently that person is Justin Sofia. If approved, the admin will assign the issue to the appropriate person, who will create a branch with a descriptive name such as 'new-feature/<feature-name-goes-here>'. Once the branch has been completed, it will be reviewed by the administrator and, if approved, the branch assignee will submit a pull request to the master document. Upon successful merge, the issue will be closed. Voila! :smile:

## Table of Contents

1. Project Management Best Practices
  * Creating New Features
  * Developing On Approved Features
  * Submitting Approved Features When Completed
2. Code Review Best Practices
  * Pre-Review Engineering Standards - Engineer's Responsibility
  * Post-Commit Code Review - Reviewer's Responsibility

## 1.0 Project Management Best Practices

dimeSocial uses a project management model based on Git and other SCM tools, and applies them to all aspects of dimeSocial product development. We believe that the Git protocol is a powerful tool for ensuring teams are in-sync and on-message, making sure that all of us are on the same page with regards to feature development and specs, as well as getting rid of problems caused by design teams being out of sync with developer teams. Our process includes all people involved with product development- and yes, software engineers are just as much product people as UI designers - and ensures that all teams have a central location and a say in what goes into the product. 

##### 1.1 Creating New Features

When a new feature is desired, create an issue from the main project specification repo and assign to 1 person from each aspect of the product development - back-end, front-end, UI design, and the CEO. The assigned person on each team is given the responsibility to speak with all members of their team and get their thoughts on the feature, and synthesize their team's perspectives into a single "team statement" (see 'Writing Effective Team Statements'). The team statement is the definitive opinion of each team on a specific feature, and should be taken seriously. Teams are encouraged to issue a team statement within 2 business days of the issue being opened. Once all teams have issues a team statement, the issue is reviewed and a decision is made by the CEO, whose decision is final. The issue is then marked as closed, with the necessary tags for things like 'featured adopted', 'feature dropped', 'revisit in product v2.0', etc. Finally, the feature is assigned to a team. 

**No feature** will be approved without a robust set of specifications. If the feature in question is a visual element, UI design must supply an example image before the feature is assigned to the front-end developer. This is another reason why all teams must be involved with this process - features often have dependencies that span across teams.

This reduces unnecessary feature creep, and problems that may arise when a certain feature bundle is added, for example, to the UI design without regard to development time on the back-end. 

##### 1.2 Developing On Approved Features

Each feature will be assigned to one person or a team, who may then pass primary responsibility to another individual within the team. The individual assigned to a feature will henceforth be referred to as the 'assignee'. The assignee is responsible for creating a new branch with a descriptive name, such as 'features/new-share-button-iOS', and descriptive tags as necessary. The assignee is also fully responsible for implementing the feature, making necessary adjustments to the specification, coordinating with other teams to ensure the feature can actually work in production, unit testing the feature. 

##### 1.3 Submitting Approved Features When Completed

Once the feature is complete and tested, the assignee will submit a pull request to the master branch, a code reviewer will review the request, and the feature will either be merged or sent back to the assignee with a descriptive message regarding what fixes must be made.

## 2.0 Code Review Best Practices

At dimeSocial, we embrace a pre-deployment code review model. This means that all code is reviewed for quality and readability before being pushed to production. Code that is not up to dimeSocial's standards will be rejected until it is deployment quality. Most importantly, this allows a second layer of bug prevention and ensures that our production code is as robust as possible. 

##### 2.1 Pre-Review Engineering Standards - Engineer's Responsibility
As an engineer, it is imperative that your code be carefully commented and formatted for easy reading, reducing developer onboarding times, increasing the usability of legacy software, and many other reasons. Simply put, well-documented code is good code. Before deploying your code, ensure that it is well-documented and easy to read. Make sure you are following styling conventions that have been established by other developers (see __'Styling Conventions'__). Code that is messy or unreadable will be rejected and resent to the original developer for cleanup before it is allowed to go into production. Just like high school, if it's not done right the first time, you will be doing it over again. 

##### 2.2 Post-Commit Code Review - Reviewer's Responsibility
Once you believe your code is up to par, commit it to the development repo with a descriptive message. Your code will be reviewed, tested and either rejected and sent back to you, or approved and merged into the development branch, which will then be integrated with the production branch. 

*Note: Developers are responsible for their own __unit tests.__ Code reviewers are responsible for integration tests, app functionality tests, component tests.*

*Note: We are still developing our code review practices. Code reviewers, commit best practices, and testing best practices are still being created. If you have suggestions, please use the guidelines under __'Contributing to this Document'__ to open an issue. Thanks!*

