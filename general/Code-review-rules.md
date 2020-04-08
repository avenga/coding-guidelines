What's in a code review?
------------------------

The goal of a code review is to prevent errors and problems, improve code quality and enable everyone to learn and improve themselves.  
There is no bad code! Always use constructive criticism to help people learn and improve them and their code.  
Praise every once in a while is a good motivation and will be received thankfully.

### A review consists of two parts:

*   **Test functionality and report problems**  
    Does the Code correctly solve the ticket? Do new problems arise because of the new code?
    
*   **Read the code and propose improvements**Is there a way to write the code in a more elegant, readable, preformant or maintainable way? Is it appropriate to refactor the code or other parts of the existing code?
    

When to code review?
--------------------

Code needs to be merged, changes don't age well, therefore **code reviews have priority** above other development tasks.  
A code review that is assigned to you should be resolved before you begin a new task.  
First thing in the morning you should check for open code reviews if code reviews don't have an assignee go get 'em, tiger!

Who is reviewing?
-----------------

Ideally, someone who knows the project and the code base gets selected by you to do the code review.  
If there is no such team member available, get a developer from another team. That also proves whether your project is **properly documented** and working as intended (on another machine).

How exactly does a code review work?
------------------------------------

When you're done with the code for a feature

1.  create a merge request for the branch.
2.  Select a reviewer (see **Who is reviewing?**) and assign the merge request and the ticket accordingly.
3.  Create a comment on the ticket with the URL to the merge request.
4.  The reviewer tests the functionality of the code, reviews the code and creates suggestions for improvement (see What's **in a code review?**),
5.  then the reviewer reassigns both the ticket and the merge request back to you.
6.  You're applying the suggestions, solve the merge conflicts that meanwhile have arisen and restart the review cycle.
7.  Once there are no further improvement suggestions the reviewer creates a comment that unmistakably marks it as approved and finished.
8.  Now everyone involved may merge the branch and add a comment in the ticket that the feature is merged.

All important milestones are commented in the merge request and the ticket, which means the complete life cycle of every feature can be comprehended after the fact if necessary.

Which information do I need for a code review?

If you're supposed to test a feature for functionality, you have to have a description of the feature and exact instructions on how to reproduce the old and new behavior.

Tips & Tricks
-------------

*   create merge requests only when a feature is complete
*   comments are more explicit than "thumbs ups" and WIP (work in progress)
*   reviews are an additional safety net for you
*   reviews are a chance to learn
*   arguments > emotions
