# Repository setup

## Permissions

* Repositories should be public
* Access should be granted using GitHub's "Teams" feature:

    ![Maintainers have "admin" rights, all CUDEM team members have "write" access](/assets/images/repo-permissions.png)


## Documentation

Set up ReadTheDocs for each software repository.

Config:

* Enable PR previews
* Create an [automation rule](https://docs.readthedocs.com/platform/stable/guides/automation-rules.html)
  to automatically active a new version for each software release.
  * Description: "Release new docs version"
  * Match: "Any version"
  * Version type: "Tag"
  * Action: "Activate version"


### Automation

Ensure a GitHub Action is setup to add a link to PR previews for each PR.

Follow [this example](https://github.com/continuous-dems/fetchez/blob/2eafbd42456e490fc2766ce6c5b5def4dc08684d/.github/workflows/pr-rtd-link.yml)!


## Branch protection

The `main` branch should be protected.

* Under repo settings > Rules > Rulesets, create a new branch ruleset
* Name it "Protect main"
* Set enforcement to "Enabled"
* In target branches, add a rule "Include default branch"
* Under rules, select:
  * Restrict deletions
  * Require a pull request before merging
    * Set 1 required approval (this can be bypassed if needed)
    * Set allowed merge methods to "squash" only
  * Block force pushes


## Merge strategy

Only allow squash merging.
Disable merge commits and rebase merges in repository settings.

To some, [this is a controversial choice](https://www.youtube.com/watch?v=5_8FTivl8Vs).

Squash merging is ideal for community health, as we can't expect perfect commit hygiene
from folks who are new to open source, and welcoming those people is key to our
community health.


## CI

* Enable [pre-commit.ci](https://pre-commit.ci) for automating checks and fixes.
* Ensure GitHub Actions is enabled.
  Click the Actions tab and, if present, click the button to enable Actions for this
  repository.
* Configure GitHub Actions following our
  [software quality policy](/policies/software-quality.md).
