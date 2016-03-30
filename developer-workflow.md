# Developer Workflow

This is an overview of the developer process at Mondo Robot. This overview is intended to capture the work-flow of stories moving from the 'To Do' status to the 'Done' status in Jira. It is assumed that all stories and bugs have been written with enough detail to allow a developer to implement a solution and for QA to understand when a story or bug has been successfully implemented.

All stories and bugs move through the following pipeline:

* To Do
* In Progress
* Dev Review
* Producer Review
* Backstage QA
* Staging QA
* Production QA

These statuses are detailed below:

### To Do
**Objective:** The **To Do** column provides a list of work that needs to be done ordered by priority and dependency.

The **To Do** status is a list of stories that have been scheduled for a sprint. The order of the list matters. Top priority stories are at the top of the list, lower priority stories, or stories with a dependency on another story in the sprint are toward the bottom of the list.

Optionally, stories may be assigned to a particular developer. If this is not the case, stores should be grabbed in the order listed, unless the top story has a dependency on a story that another developer is actively working on.

If nothing is assigned to you, and you're not sure what you should work on next. Please talk to your project lead.

### In Progress
**Objective:** The **In Progress** column provides an overview of what each member of the team is currently working on.

When a developer starts working on a story, they should drag it to the **In Progress** status. As a general rule, try to only work on one story at a time.

For highly dependent stories, instead of starting multiple stories, focus on implementing the smallest set of features required to complete the story.

As you implement a solution for a story, focus on implementing a defensive solution. Developers are ultimately responsible for seeing a story through to it's release into production. As such, think about the different ways QA will try to break your solution. Your solution should be robust within the context of the story. Above all, our goal is to ship high quality code.

### Dev Review
**Objective:** The **Dev Review** column provides an overview of completed work that needs to be reviewed and deployed by senior developers and/or team leads.

When a developer feels that they've provided a sound solution the story, written tests to verify that story, verified that all tests are passing and there are no Code Climate warnings, and have opened a Pull Request with the team and any additional developers requesting a code review, their story should be moved to the **Dev Review** column.

The team should provide feedback to the approach and implementation of the proposed solution. Peer review and constructive feedback is an important step in the development of healthy code, and provides the opportunity for developers to grow in their craft. Our goal at Mondo Robot is to produce high quality, clean code that solves our client's challenges.

Once all feedback has been reviewed and incorporated, a senior developer or team lead should merge the proposed change into the 'develop' branch, and ensure the code is successfully deployed to the backstage environment. Once the change is in backstage, it should be verified by the developer before being moved to the **PO Review** column.

### PO Review

**Objective:** The **PO Review** column provides on overview of completed work to the Producer on the project. This allows the producer to maintain an understanding of completed work.

Once a story moves to the **PO Review** column, it is the responsibility of the Producer on the project to verify the story was completed in a satisfactory nature in regards to the desire of the client. All review will take place on that projects Backstage environment. If there are any issues with the way the story was implemented, comments should be added to the story to clarify the desired results. If the story was implemented as desired, the Producer should move the story the to **For QA (Backstage)** column for QA review.

### For QA (Backstage)

**Objective** The **For QA (Backstage)** column provides an overview of stories that need to be put through QA review.  The objective is for QA to review stories in a timely fashion to limit developer context switching.

Once a story moves to the **For QA (Backstage)** column, it moves into the domain of the team's QA member(s).  QA should insure the story was completed as described, and run an exhaustive test on the story.  Consideration should be given to ensuring the visual presentation is very similar across the supported web browsers, and edge cases are handled appropriately.  If issues or concerns are found, first verify a solution is not part of a future story.  If not, if the issue or concern is part of the story definition, a comment should be added to the story.  The story should then be moved to the **To Do** column and assigned to the original developer.  Additionally, reach out to that developer via Slack to let them know an issue has been found on their story.

When in doubt, over communicate.  Utilize Slack or ask if more information or clarification is needed.  We're a team and this is a team effort.

Once QA passes a story, it should be moved to the **For QA (Staging)** in preparation for the push to the Staging environment.

### For QA (Staging)
**Objective:** **For QA (Staging)** holds stories in preparation for the push to the Staging environment.

The **For QA (Staging)** is a holder for all stories that are part of a sprint release. Once we're code frozen on a sprint (end of the day, three days prior to production release) and all stories have been cleared from the sprint, a senior developer will merge the develop branch into staging and deploy the staging branch to the Staging environment.  Once the staging deploy is complete,
