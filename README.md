# GitHub Guidance
_Guidance and best practice rules for using GitHub within the Public Health Scotland organisation_

## Contents
- [Set up](#set-up)
- [Workflow](#workflow)
- [Top tips](#top-tips-for-following-the-github-flow)
- [Security](#security)
- [Style Guide](#style-guide)

## Set up
In order to use the Public Health Scotland organisation account, you will need to sign up for a personal GitHub account. You can do this using your PHS/NHS email address or a personal email address if you prefer. If you are using your PHS/NHS email address then **ensure that you do not also use your PHS/NHS password**. You should then send your GitHub handle/username to the Transfroming Publishing mailbox (phs.transformingpublishing@phs.scot), where one of the owners will add you to the organisation. Please make your **profile name your full name**, and if you are happy to do so make your profile picture a photo of yourself - often handles are a random assortment of letters and numbers so this allows your collaborators to know instantly who has edited their code. It also helps to make GitHub a friendly place to work! :family:

## Workflow
For writing and editing code, we recommend using the **GitHub Flow** method of working (see image below). This is a branch-based workflow and involves keeping the master branch clean and 'production ready' at all times. This means that the code is fully functional i.e. ready to be deployed if the project is a Shiny app or runs correctly if it is an analytical piece of work. When making changes to a repository, analysts should create a branch per person, carry out the required changes and then merge these back to the master branch via a pull request. Pull requests should be approved by at least one collaborator - we recommend you assign a specific reviewer(s) to check your work. In order to ensure that the master branch remains 'production ready' we also recommend that changes are tested by the reviewer before approving. GitHub provides excellent functionality for dialogue between collaborators on a pull request, until all are happy with the final code. There is no need to have lots of long-living branches - in other words, after a specific change or set of changes have been made and merged back into the master branch, delete your personal branch. 

![](https://i.imgur.com/LVTwlEE.png)
*Original image from https://guides.github.com/introduction/flow/*

Following this workflow is most important when working collaboratively on code which is intended for publication and applies even to minor, low-risk changes. There may be instances when you are working alone, and on code which is very developmental, in which case you may not need to follow this workflow. There are also specific repositories which do not require this workflow such as this repository and the [resources repository](https://github.com/Public-Health-Scotland/resources) - this is because changes to these repositories do not affect code for publications. 

## Top tips for following the GitHub Flow
- In order to ensure that this workflow is followed we recommend **protecting the master branch** via the settings on a repository. In the Branches tab, check the box _Protect this branch_ and then the box _Require pull request reviews before merging_. This means that code can only be added to the master copy of the code via a branch. You can also set a minimum number of reviewers required for changes to be merged.
![](https://i.imgur.com/b6EqJ7W.png)
- In order to avoid merge conflicts as much as possible, **keep branches short-lived** (i.e. delete a branch after merging with the master) and **pull from the origin (GitHub) regularly, particularly before creating a pull request yourself**. Note that pulling will not overwrite local changes you have made, so you should feel confident that you can pull regularly in order to keep up to date with any changes made directly on GitHub, or by other contributors (e.g. the creation of new branches directly on GitHub).
- **Commit and create pull requests early and often.** This will create a helpful audit trail of your project. It also makes the review process more managable for those assigned to the task.
- Note that when you make changes to the code, you should clone a repository to your home drive or local files and work on it there.

## Security
The following rules should be followed in order to adhere to security and confidentiality guidelines in PHS:
1. Use your .gitignore file to make sure that **no data files are ever uploaded to GitHub**. At a minimum, ensure that your .gitignore includes common text files, excel files, SPSS formats, R data files and any folder called 'data'. An [example .gitignore file](https://github.com/Public-Health-Scotland/GitHub-guidance/blob/master/.gitignore) can be found inside this repository with code to ignore these main file types. However, be aware that data may be saved in other formats so you may need to add to these for certain projects. Options for additional file types can be found [in this excellent GitHub repository](https://github.com/ukgovdatascience/dotfiles). 
2. Ensure that **usernames and passwords are never embedded in your code**. 
3. Ensure that **comments within code do not contain any confidential information** such as CHI numbers or other patient identifiable information.
4. It is fine to embed filepaths in your code, but make sure that these do not include **sensitive folder names** (e.g. customer names).

## Style Guide
To ensure consistency of use within the organisation, some guidance on styling while using git and GitHub is outlined below:
- **Repos names** should be lowercase with hypens, descriptive and unique. For example, if you need a repo for _time series_, the repo name should be specific enough to highlight the publication or team name, e.g. `tpp-time-series`.
- **Commit messages** should be concise and meaningful. If you need to raise awareness of something particular, the pull request commentary could be a better place.
- **Teams** can be used, although consider how broad the team can be to be most effective. Instead of creating a team for a publication, does the team or health topic have better coverage?
- **README files** are automatically rendered on the first page when visiting the repo on GitHub. They are the perfect place to provide users an overview of the project and how to get involved, an example is given in the [r-project-structure repo](https://github.com/Public-Health-Scotland/r-project-structure/blob/master/README.md). Where possible, README files should be generated for each public repo.
- **Private and public repos** are available in the PHS organisation. We encourage coding in the open with the above [security](#security) guidelines in practice. However, if you have the need for a private repo you can use them on GitHub or consider the use of Gitea. 
