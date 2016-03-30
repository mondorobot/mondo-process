## User Story Guidelines

#### Objective
A well written story should define a desired outcome from an interaction perspective.

#### Examples
Let's look at two examples of stories describing the feature of a welcome email upon signup.

Bad:
```
Email should get sent after signup.
```

Good:
```
As a new Fox Insight signup
After I signup [1]
Then I should receive a Welcome Email [2]
So that I feel welcomed to the community

[1] /register
[2] Email content attached to epic as: Welcome-Email.docx
```

Let's look at what makes the 'Good' story good:
* Line 1: We clearly define the type of user for whom this story will apply.  This helps the Dev and QA understand the context.
* Line 2: Define the step(s) that need to be taken to bring the Dev and QA to the new feature. Footnotes can be used to provide addition information without polluting the story.
* Line 3: Define the desired outcome of the feature. Assets (whenever relevant), should be referenced. Assets should be attached to Epic and referenced in the story.
* Line 4: State the objective of this feature (why it matters). This provides the 'Why' context to the developer.

It's important to note that this story lacks any implementation detail.  This is by design.  Stories should focus only on the desired outcome.  Development implementation details should be left to the developer responsible for completing the story. This means a variety of team members can contribute stories without intimate technical knowledge.

It's also important to clearly define a successful outcome of a story. A clear definition of success helps the developer and QA understand the scope of work necessary to define success. If an interaction has multiple outcomes, separate stories should be written for each outcome.  As you write stories, it helps to think about the story from a QA perspective:
* How would I tell Todd how verify the feature was implemented correctly?
* Was I specific about edge cases?

Strive to keep stories as concise as possible. It's preferable to create a number of smaller, more concise stories and group them in an Epic instead of one large, multi-day story.  If you find a story is getting long (more than 5-6 lines), it may be better to break it into smaller stories.

#### Additional Conventions
* Notes intended to guide QA or clarify success should be put below a story with a *QA Notes* heading:
```
*QA Notes*
Notes to guide QA
```
* Notes intended to guide a more junior developer on implementation details should go below the story with a *Dev Notes* heading:
```
*Dev Notes*
Notes to guide implementation details
```
