---
topic: "github: branch protection"
desc: "making sure PRs to master get code reviewed, for example"
indent: true
category_prefix: "git: "
category_prefix_alt: "github: "
---

In professional software development settings, it is a common practice to *protect the master branch*. 

That is, there may be some policy rules about merging changes into master:
* The code should be on a feature branch, and it should go into master via a pull request
* The code should be code reviewed
* If there are CI/CD scripts set up (e.g. GitHub actions), those should be passing, not failing
* The branch should be up-to-date with the changes in Master (not *behind* master)
* The merge should be done by someone with admin authority.

GitHub allows you to enforce some or all of these rules with branch protection.

Branch protection is configured in
* the `Settings` menu of the repo,
* under `Branches`
* then select `Branch Protection Rules`

Note that an empty repo has no commits, and therefore no branches.  So you must have at least one commit (e.g. a README.md file) before you can define branch protection rules.
