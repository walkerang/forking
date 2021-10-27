# Lab Activity: Forking

In this lab, we will be simulating the experience of contributing to an open source project on GitHub using the [Forking Workflow](https://www.atlassian.com/git/tutorials/comparing-workflows/forking-workflow). Recall from the previous lab that Branching requires "read-write" access a central, server-side repository on GitHub. Forking is a method of collaboration that allows anyone to contribute to an open source project **without** read-write permissions to a GitHub repository. 

> A "Fork" is a copy of a server-side Git repository (i.e. on GitHub) on another user's account. This allows the original repository owner to maintain their project without granting repository permissions to anyone else, while also giving users a copy of a project that they can manage on GitHub on their own. The benefit to open source communities is that data can be pushed and pulled between Forks through Pull Requests.   

By the end of this lab, you will have experience with the following:

- Forking a repository from GitHub
- Cloning a forked repository to your computer
- Making commits to your forked repository
- Creating pull requests from your forked repository
- Linking specific Github Issues to pull requests

This particular simulation is for contributing to [a recipe website](https://chrisdaaz.github.io/forking/). Your task will be to contribute a recipe to the website so that the entire class can have new recipe to experiment with in their own kitchen! While I am exciting to read the recipe you will be contributing, you will not be graded on the quality or sophistication of the recipe! 

By completing this lab, you will have a copy of all of the code and files required for a [Jekyll](https://jekyllrb.com/) website using the [Chowdown](https://github.com/clarklab/chowdown) theme. You **do not** need to have Jekyll installed on your machine to complete this lab. You just need the ability to add files to the repository, edit them in VS Code (or your preferred plain text editor), and push `commits` to GitHub.

## Prerequisites

- Have a recipe in mind, specifically a title, list of ingredients, and steps to make it. It can be anything you want.
- Have an image of the finished dish. You can contribute your own photo, or search [Creative Commons](https://search.creativecommons.org/) for a generic photo of the dish that is licensed for re-use.

## Getting Started

1. [Fork this repository](https://github.com/chrisdaaz/forking) to your GitHub account: Click on the `Fork` button near the top-right of this page. This will create a copy of the repository to your GitHub account. At the end of the process, you should be at the GitHub version of your forked repository. The URL will look something like this: `https://github.com/USERNAME/forking`

2. Open the repository in the online text editor (VS Code) by pressing the period key `.` on the repository home page.

## Writing a Recipe

To complete this assignment, you only need to add two files. The first file will be a recipe file within the `_recipes` subfolder; the second file will be an image file (`.png | .jpg | .gif`) added to the `images` subfolder. Here's how:

4. Create a new markdown file within the `_recipes` directory named after your dish. Use [Kebab case](https://en.toolpage.org/tool/kebabcase) for the file name. and `.md` as the file extension. For example, a recipe for Banana Bread would be `banana-bread.md`. It's very important that this file is save to the `_recipes` directory.

Recipes are written in [Markdown](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet) and contain a few special sections:

- The frontmatter, which contains:
    - Title, Image, and Layout (which is "recipe")
    - Ingredients (a list of things in the dish)
    - Directions (a list of steps for the dish)
- Body content (for intros, stories, written detail, credits)

You can an example on the Red Berry Tart recipe. 

- [example Markdown](https://raw.githubusercontent.com/clarklab/chowdown/gh-pages/_recipes/red-berry-tart.md)
- [example recipe page](http://chowdown.io/recipes/red-berry-tart.html)

Or you can see the example in the `_recipes/bagels.md` file (you can copy the contents of the file to your new file and swap out the content with your recipe information).

5. Save the file when you're finished writing the recipe.

## Adding an Image

_You can find free-to-use images at [Creative Commons](https://search.creativecommons.org/)._

6. Save the image file (`.jpg`, `.png`, or `.gif`) to your computer and upload it to the `/images` folder of the repository by right-clicking the `/images/` folder and selecting "Upload...". Make sure that the image file name and extension matches the value for the `image` filed in your corresponding markdown file. For example, if you're adding an image file called `bagels.jpg` to the `/images` folder, the `bagels.md` markdown file for the _recipe_ should also include the line `image: bagels.jpg` near the top of the file.

> If you're using the command line, see "Command Line Workflow" below for the git work flow.

7. Commit the changes to your repository using the same steps from the [first lab activity](https://angry-varahamihira-f6a405.netlify.app/2-setup.html). Skip ahead to the Pull Request section.

## Command Line Workflow

- Open your terminal in VS Code (`File menu > Terminal > New Terminal`) or terminal program (e.g. Git Bash). 

- Run `git status` to make sure that Git is aware that you've created two new untracked files: a markdown file (`.md`) and an image file. 

- Commit the files to your repository: `git commit -am "adds a new recipe"`

_Note: you are not making a new branch for this commit. You are committing directly to the `main` branch of your `Fork` of the `forking` repository._

- Push the `commit` to your `Fork` on GitHub: `git push`

## Pull Request

- Now, when you visit your `Fork` on Github, you will notice that your repository is one commit ahead of `https://github.com/chrisdaaz/forking`. GitHub will be aware of this and will ask you if you'd like to `Compare and Pull Request`.

- Create a Pull Request from **your** forked version of `forking` to **my** original version of `forking` on GitHub [[help guide](https://docs.github.com/en/free-pro-team@latest/github/collaborating-with-issues-and-pull-requests/creating-a-pull-request-from-a-fork)].

> Contributions to projects through pull requests are usually linked to [Issues in the target repository](https://github.com/chrisdaaz/forking/issues). GitHub provides ticketing system (called "Issues") in every repository. This helps repository contributors keep track of work that needs to get done on the repository. Please reference [Issue #1](https://github.com/chrisdaaz/forking/issues/1) in the Description of your Pull Request. 

13. In the `Title` field of the Pull Request, enter the name of your recipe. In the `Description` of your recipe, reference the GitHub Issue number in order to link your contribution to the requested work in the Issue tracker [[here's a help guide on linking pull requests to issues](https://docs.github.com/en/free-pro-team@latest/github/managing-your-work-on-github/linking-a-pull-request-to-an-issue)].

```
TITLE: Buffalo Chicken Recipe
DESCRIPTION: references #1
```

14. When you're ready, click on `Create Pull Request`. This will notify me that your work is complete. If the recipe looks good, I'll add it to the book and you will see it available here:

**You're done!**
