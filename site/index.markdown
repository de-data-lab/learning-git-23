---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: home
title: home
---

# Welcome! 

During this exercise, you'll use version control and [markdown](https://www.markdownguide.org/basic-syntax/) to build out a simple fellow profile page. You will practice key steps of the Git workflow such as cloning repositories, creating issues, making pull requests, and merging. 

## Prerequisites

1. You must have Git [installed on your machine](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git).
2. You must have been added as a collaborator on the [Github repository](https://github.com/de-data-lab/learning-git-23).

--- 

# Building Your Profile Page

## The Workflow

At the Lab, we typically use a modified version of [Git Feature Branch Workflow](https://www.atlassian.com/git/tutorials/comparing-workflows/feature-branch-workflow). The idea behind this workflow is that every new feature/fix should be 1) documented in a [Github issue](https://docs.github.com/en/issues/tracking-your-work-with-issues/creating-an-issue), 2) developed in a separate branch based on the issue, and then 3) merged into `main` via a pull request. Let's get started! 
  
 <br/>

### 1. Clone the Github repo 

Go to the [Github repository](https://github.com/de-data-lab/learning-git-23) and clone it to your machine: `git clone [REPO_URL]`. You will find the URL under **Code** at the top of the repo. Where possible, we recommend using SSH to clone Git repositories. After cloning the repo, be sure to `cd` into it. 

--- 

### 2. Open an issue on the repo 

Next, you'll create and submit an issue to tell everyone that you are adding your profile to the website. An issue should: 
* Have a descriptive title 
* Include a comment that describes what needs to be done and why
* Be assigned to a member of the repo (or to yourself)

![Adding a new issue](/assets/homepage/issue.png)

--- 

### 3. Create a new feature branch from the issue 

Github allows you to generate a new branch from an issue in just a couple of clicks. To do so, click **Create a branch** under "Development" on the issue page you just created. A modal will appear in which you can enter the details for your new branch. Leave everything as-is except the **Branch name**. The branch name should be preceded by your first name and a `/`. This will help other members of the repo keep track of who is working on what. Your new branch should be titled something like `yourname/add-my-profile-page`. 

After creating your branch, return to your terminal or IDE and switch to it by running the following lines of code: `git fetch origin` and then `git checkout [YOUR BRANCH NAME]`.

![Creating a new branch](/assets/homepage/createabranch.png)

--- 

### 4. Create your profile

Now we'll finally build out a profile page. 

You can follow along using 1) an IDE such as [Visual Studio Code](https://code.visualstudio.com/), 2) a basic text editor (such as TextEdit for Mac), or 3) any other program that allows you to edit `.md` files. 

1. Locate the `site/profiles` directory. Copy the file named `_template.md`. 
2. Rename the copied file to `[firstname].md` (e.g., `john.md`). 
3. Fill out the YAML heading (the portion at the top in between the `---`). Do not change the `layout` field.
4. **To add a link to your headshot**: Add your photo to the `/assets/headshots` directory. Then under the `image` field, add the path to your photo, e.g., `/assets/headshots/example.png`.

Next, fill out the rest of the template. After you're done, be sure to save the file. 

---

### 5. Commit and push your changes 

You can make commits as you edit your profile or make one single commit after you're done. Once you're satisfied with your work, push your changes to the remote repository by running `git push`.   

