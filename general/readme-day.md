# Readme Day

## Goals of the Readme Day

The general idea is that every project has a regular day when the local development setup as well as the documentation to set up, run, develop and test the project (usually found in the README.md) is tested. In many cases it is useful to test the deployment and other project specific documentation as well. The goal is to have **well maintained documentations with all necessary and up-to-date information**.

## Necessity and Frequency

The lifespan of a project, the frequency of code contributions as well as the number of contributors are factors for the necessity and frequency of a Readme Day. If the development from start to finish is about 3 weeks or code contributions are not regular enough, a Readme Day is not necessary.

If the number of developers contributing code 

* **is 2** a Readme Day should be planed every **4 weeks**,
* **is up to 6** a Readme Day should be planed every **3 weeks** and
* **is larger than 6** a Readme Day should be planed every **2 weeks**.

## Who and How

Assigning all involved developers to execute a Readme Day, one after another, is a good idea. Introducing new developers by having them execute the Readme Day will provide great insight and valuable feedback, as well as asking developers who are not involved in the project.

The following steps are one possible way for the Readme Day:

1. Revert your project to a blank slate by either
   1. Deleting the whole project code from your local machine and geting a fresh copy from your git repository _OR_
   2. Running `git clean -xdf` to delete any and all untracked files from the repository. __Make sure that you can recover any deleted secrets or similar data before you do this!__
2. Follow the steps in the README to set up the project for development
3. Check if everything works as documented

If possible, fix all identified problems directly and update the README regardingly. Otherwise try to schedule the issues to have them fixed at least until the next Readme Day.
