## Workflow

Our development workflow uses a feature branching model. **tasks**.
A well written task using non-technical terms often serves as the first, best documentation for any new feature.
Following the workflow described below ensures that features are implemented, reviewed, and deployed efficiently.

### Create a PR

All branches must have a single corresponding task.
Once the task exists, perform at least the following steps to create your PR:

1. Create a branch off `master`
1. Open a PR based on the branch giving detailed answers to the questions in from the pull request template.

### Add category label and assign reviewers.

Add `category:minor`, `category:medium`, or `category:major`.

Assign reviewers based on the labeled `category` of the change (see [change management guidelines](https://opn-ooo.atlassian.net/l/c/swoCQqi6)).

* `category:minor`: Team members
* `category:medium`: Team members + affected teams
* `category:major`: Team members + affected teams + @omise/quality, @omise/devops, and @omise/security

### Reviews and sign-off

Developers reviewing PRs use GitHub's reviewing system to approve once they are happy with the changes proposed.
As you update the PR in response to feedback, make sure the PR description continues to describe the changes introduced in the PR.

Branches are squash merged (`git merge --squash`) into the `master` once signed off by one of the team leads.

### Deployment

Once a PR is merged into `master`, it is automatically deployed to production.

#### Staging environment

To test changes in the staging environment, merge your branch into the `staging` branch and push it to GitHub, this will deploy automatically to the staging environment.
