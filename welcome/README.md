# Welcome

Welcome to CS 24!  This assignment will make sure you have  Git set up correctly
and are ready to submit your programming projects to Gradescope.


## Git Repo Setup

This class  will use a  single Git repo  for the whole quarter.  Each assignment
will get its own folder within  that repo.  You'll create  a private fork of the
main class repo;  I'll push code to the class repo  as assignments are released,
and you can pull to get the code.

Normally you'd  fork the class repo on GitHub,  but GitHub doesn't allow private
forks of public repos, so this'll be a little more complicated.

First, get a copy of the class repo onto your local machine:

- [Install and configure Git][git-setup] if you don't have it already.
- Clone the class repo somewhere on your local machine.

Then create an empty repo on [GitHub][github]:

- Create a GitHub account if you don't already have one.
- Create a new repo on GitHub.
  - Don't initialize it with any files.
  - Make sure it's private.

Configure your local repo to talk to both GitHub repos:

- The class repo will be at a remote named `origin`; rename it to `upstream`.
- Add a new remote for your GitHub repo; call it `origin`.
- Push your local `master` branch to your GitHub repo.
- Your files should now be visible in the GitHub web UI.

Then check that you have everything set up correctly:

- Make sure the output of `git remote -v` makes sense.
- Save the output of `git remote -v` as `welcome/remotes.txt`.


## Git Branches

Now that your repo is set up, get some practice merging:

- The class repo contains three extra branches:
  - `fishwife`
  - `jabberwocky`
  - `shi`
- Merge all of these into your `master` branch.
  - If you use a GitHub PR, make sure you pull from GitHub afterwards.
  - If you don't use a PR, make sure you push to GitHub afterwards.


## Some Code

Then write some code.

- Create the folder `welcome/code`.
- Create an `olleh.cpp` file in that folder. It should compile to a program that
  reads a single  line from the console,  then prints that line with the letters
  of each word reversed.  Words are separated by whitespace and/or punctuation:
  ```
  [user@host code]$ ./olleh
  It cost $349.95, but I bought it anyway.
  tI tsoc $943.59, tub I thguob ti yawyna.
  [user@host code]$ 
  ```
- Create a `Makefile` inside your `welcome/code` folder.
  - Running `make` in that folder should compile `olleh.cpp` to `olleh`.
  - Running `make clean` in that folder should the executable and any object files.
  - Running `make clean` should succeed even if there is no executable.


## Commit and Submit

- Commit all your changes and push them to GitHub.
- Submit your GitHub repo to Gradescope.
  - You'll be asked to connect your GitHub account to Gradescope if you haven't already.
- Make sure all the tests pass.


## Git Hints

- A Git cheatsheet that may prove helpful:\
  https://xavierholt.github.io/cheatsheets/git.html
- It's always a good idea to run `git status` and see what state your repo is in.


## Code Hints

- Whitespace and punctuation are defined as in the [cctype][cctype] header.  Everything
  that isn't whitespace or punctuation is considered to be a "word" character.
- Your code should always print exactly one newline, regardless of the input.
- Your code must compile with no warnings (see the syllabus).
- Don't check executables or object files into Git.


[github]: https://github.com
[git-setup]: https://help.github.com/en/github/getting-started-with-github/set-up-git
[cctype]: https://cplusplus.com/reference/cctype/
