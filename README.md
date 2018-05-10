# GitHub-guidance
_Guidance and best practice rules for using GitHub within the Transforming Publishing team_

## Set up
In order to use the Transforming Publishing organisation account, you will need to sign up for a personal GitHub account. You can do this using your NHS email address, unless you already have a GitHub account which you would like to use. You should then send your GitHub handle to Anna Price (anna.price5@nhs.net) or David Caldwell (david.caldwell1@nhs.net), who will add you to the organisation. Please ensure that your **profile name is your full name**, and if you are happy to do so make your profile picture a photo of yourself - often handles are a random assortment of letters and numbers so this allows your collaborators to know instantly who has edited their code. It also helps to make GitHub a friendly place to work! :family:

## Workflow
For writing and editing code, we recommend using the **GitHub Flow** method of working (see image below). This is a branch-based workflow and involves keeping the master branch clean and 'production ready' at all times. When making changes to a repository, analysts should create a branch, carry out the required changes and then merge these back to the master branch via a pull request. Pull requests should be approved by at least one collaborator - we recommend you assign a specific reviewer(s) to check your work. There is no need to have lots of long-living branches - in other words, after a specific change or set of changes have been made and merged back into the master branch, delete your personal branch. 

![](https://i.imgur.com/LVTwlEE.png)
*Original image from https://guides.github.com/introduction/flow/*

Following this workflow is most important when working collaboratively on code which is intended for publication and applies even to minor, low-risk changes. There may be instances when you are working alone, and on code which is very developmental, in which case you may not need to follow this workflow. There are also specific repositories which do not require this workflow such as this repository and the [resources repository](https://github.com/NHS-NSS-transforming-publications/resources) - this is because changes to these repositories do not effect code for publications. 

#### Top tips for following the GitHub Flow:
- In order to ensure that this workflow is followed we recommend **protecting the master branch** via the settings on a repository. In the Branches tab, check the box _Protect this branch_ and then the box _Require pull request reviews before merging_.
- In order to avoid merge conflicts (as much as possible), **keep branches short-lived** and **pull from the master branch before creating a pull request yourself**. Both these measures will ensure that your branch is kept up-to-date with the master branch.
- **Commit and create pull requests early and often.** This will create a helpful audit trail and also reduce the chance of merge conflicts.

## Security
The following rules should be followed in order to adhere to security and confidentiality guidelines in PHI:
1. Use your .gitignore file to make sure that **no data files are ever uploaded to GitHub**. At a minimum, ensure that your .gitignore includes common text files (`*.[cC][sS][vV]` and `*.[tT][xX][tT]`), excel files (`*.[xX][lL][sS][xXmMtT]?`), SPSS formats (`*.[sS][aA][vV]`), R data files (`*.[rR][dD][aA][tT][aA`] and `*.[rR][dD][sS]`) and any folder called data (`data/`). However, be aware that data may be saved in other formats so you may need to add to these for certain projects. An [example .gitignore file](https://github.com/NHS-NSS-transforming-publications/GitHub-guidance/blob/master/.gitignore) can be found inside this repository and options for additional file types can be found [here](https://github.com/ukgovdatascience/dotfiles). 
2. Ensure that **usernames and passwords are never embedded in your code**. 
3. Ensure that **comments within code do not contain any confidential information** such as CHI numbers or other patient identifiable information.
4. It is fine to embed filepaths in your code, but make sure that these do not include **sensitive folder names**.
