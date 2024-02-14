# Week 1: Setting up GitHub and Conda

## GitHub

GitHub is a web-based platform that allows you to store and manage your code. It is widely used by developers and data scientists to collaborate on projects and share their work with others. In this course, we will be using GitHub to store and share our code, both for the exercises as well as the milestones and final assignment.

### 1. Create a GitHub account
Go to the [GitHub website](https://github.com) and sign up for an account if you don't have one already.

<details>
<summary>Detailed steps</summary>

1. Open your web browser and navigate to https://github.com/.
2. Click on the `Sign Up` button located in the top right corner of GitHub’s homepage.
3. On the next page, provide the required details including a new `Username`, a `valid Email Address` (EPFL address recommended for step 8.), and a `Password`. Make sure to verify that the password is at least 15 characters long or at least 8 characters long with a combination of letters, numbers, and symbols.
4. Review GitHub’s Terms of Service and Privacy Statement, and if you agree, click on `Create an account`.
5. Next, you might be guided through a few survey questions. You can answer them or directly click on `Complete Setup`.
6. You’ll be sent an email to the address you provided. In that email, click `Verify email address`.
7. That’s it! You should now have a GitHub account.
8. (Optional) The GitHub Student Developer Pack is a free offer from GitHub specially for students. It provides access to a variety of premium development tools and services free of charge for as long as you’re a student. [GitHub Student Developer Pack](https://education.github.com/pack)
</details>

### 2. Configuration: Command Line Git
We usually use the command line to interact with GitHub. We will look at the most common actions but here is a [cheat sheet](https://about.gitlab.com/images/press/git-cheat-sheet.pdf) for the most common commands. Make sure you have Git installed on your computer by typing `git --version` in your terminal.

<details>
<summary>Detailed steps</summary>

#### MacOS

1. Open the Terminal app (`cmd + space` and type `terminal`). Alternatively, you can use iTerm2 or any other terminal emulator.
2. Type:
```bash
xcode-select --install
```
3. Follow the instructions to install the command line developer tools.

#### Windows

% TODO: should download interface for linux?
1. Download Git from the [official website](https://git-scm.com/download/win) (choose the 32 or 64-bit version depending on your system).
2. Open the downloaded file and follow the installation instructions.
3. Launch the Git Bash terminal.

#### Both: Final steps
4. Check that Git is installed by typing `git --version` in your terminal.
5. Configure your username and email address by typing the following commands in your terminal:
```bash
git config --global user.name "Your Name" # Replace with your GitHub username
git config --global user.email "user@epfl.ch" # Replace with the associated email address
```
6. Check that your configuration was successful by typing (leave file by pressing `q`):
```bash
git config --global --list
```
</details>

### 3. Create a Profile README
A profile README is a special repository that is automatically displayed on your GitHub profile. It is a great way to introduce yourself and showcase your work. Take your time to create such a README on the GitHub website.

<details>
<summary>Detailed steps</summary>

1. On GitHub, in the upper-right corner of any page, click on the `+` and then click `New repository`.
2. Name the repository with your GitHub username (must match exactly!).
3. Select the `Public` option.
4. Check the box to `Initialize this repository with a README`.
5. Click `Create repository`.
6. Above the right sidebar, click on `Edit README` and start editing the file.
7. You can use the [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/) to format your README.
8. Once you are done, click on `Commit changes`.
</details>

### 4. GitHub Basics: Create a Repository
% TODO: creating, cloning, pushing, pulling, forking, pull requests, issues, etc.
Finally, we will create our first repository and update it via the command line. Please make sure to create a public repository (so the TAs can see it) and to add a README file.

#### Creating a new repository

1. Go to the GitHub website and click on the `+` in the top right corner and then `New repository`.
2. Name the repository `ppchem` and select the `Public` option. Also check the box to `Initialize this repository with a README`.

#### Cloning the repository

3. Open your terminal and navigate to the directory where you want to store the repository.
4. Type the following command to clone (download) the repository to your local machine:
```bash
git clone https://github.com/username/ppchem.git # Replace with your GitHub username
```
4. Navigate into the repository by typing `cd ppchem`.

#### Making changes and committing them

Whenever you make changes to your repository, you need to commit them to save the changes to the repository's history.

5. Open the README file in your favorite text editor and name your favorite molecule. Your TAs recommend `Caffeine` including a picture of the molecule.
6. Save the file and go back to your terminal.
7. Type the following command to stage the changes:
```bash
git add README.md # stages only the README file
git add . # stages all changes if you adapted more files
```
8. Type the following command to commit the changes:
```bash
git commit -m "Some message" # Replace with a meaningful message
```

#### Pushing the changes to GitHub

For now, we only made changes to the local repository and committed them (prepared them for upload). We need to push the changes to GitHub to make them available to others.

9. Type the following command to push the changes to GitHub:
```bash
git push origin main # Replace with the branch name if you are not on the main branch
```

You can check the status of your repository at any time by typing `git status` in your terminal in the folder of the repository. This will also show you the changes you made and the files you staged as well as the branch you are currently on.

#### Working with branches

10. Type the following command to create a new branch:
```bash
git checkout -b new-branch-name
```
11. Type the following command to switch to an existing branch:
```bash
git checkout branch-name
```
12. Publish the branch to GitHub by typing:
```bash
git push origin new-branch-name
```

#### Pulling changes from GitHub

If you are working on a repository with others, you might want to pull the changes they made to your local repository. You can do this by typing `git pull` in your terminal in the folder of the repository.

## Conda
% TODO

1. download miniconda
2. init
3. create env
4. install some stuff
5. export env to yml
6. push to github

## Milestone
% TODO: Add link to milestones repo and explain how to use it; here learn to fork; adapt milestones repo too!

% lots of milestones from github section above

% TODO Conda: create a env.yml file from the created env and push it to the created repo
