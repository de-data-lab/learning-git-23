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

You can make commits as you edit your profile or make one single commit after you're done. After committing, it's a good idea to make sure your local branch is still up to date with `main` by running `git pull origin main`.  Once you're satisfied with your work, push your changes to the remote repository by running `git push`.   

---

### 6. Make a pull request 

After a successful `git push`, go back to the repository on Github and you should see a message that looks like the below. Click **Compare and pull request**. 

![Making a pull request](/assets/homepage/create-pr.png)

Then, create your pull request (PR). You'll need to: 
* Name your PR. It should start with a verb that describes what the PR accomplishes (e.g., "**add** profile page", "**fix** carousel component memory leak"). 
* Inside the description box, add any additional context needed to understand what the PR does or why it is necessary.
* Click **Reviewers** and then locate the username of your partner. 
* Submit the PR. Your partner will receive a notification that your PR is awaiting their review. 

--- 

### 7. Review and merge another person’s pull request

Once you receive an invitation to review another person’s pull request, go to the pull request and review the changes.

1. Go to the **Files changed** tab. There should be two changed files (the `.md` file containing the new profile and the image file). 
2. Review the code. If everything looks good, click **Review changes**, write any comments you have, check **Approve**, and then **Submit review**.
3. After approving the changes, go back to the PR and click **Merge pull request**. This will merge your partner's changes into the main branch. 

![Pull request review](https://user-images.githubusercontent.com/17035406/184684017-4b191515-90e5-4828-b872-f2f6daa38041.png)

<br/> 
After the PR has been merged, the site will rebuild and you should see a new page added after a few moments. It will look something like this: 

![Example fellow page](/assets/homepage/examplefellow.png)