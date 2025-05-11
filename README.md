F431103
Daniel Lean

List of files in repository

  Daniel_Lean_ARDUINOSETUP - an image file containing a picture of an arduino and temperature sensor plugged into a laptop
  
  24WSA024_JNB_Arduino_Coursework_Final_2025S2(V1).ipynb - The notebook containing the entire coursework brief
  
  README.md - A file containing documentation of the coursework tasks

Task 1

  Task 1.1 

    Why cant the student find their private repository when trying to save their notebook to github?

      This could be because the student skipped a step to authorize private repository access when they first connected colab to github.

    How does google colab access repositories and how can the level of access by decided?

      Google colab interacts with github through OAuth tokens and API requests. The level of access depends on the permissions granted on the OAuth page.

    How can you verify that your authentication settings are working correctly?

      If authentication is working, a selection from a list of both public and private respositories should appear when saving to github.
      

  Task 1.2

      A Github action for Automated task tracking using codespaces was implemented.
      

  Task 1.3

    What did i do?
    
      I started by creating a new branch using "git checkout -b test-branch".

      I then immediately tried to delete it with "git branch -d test-branch".

      It returned the error message "error: cannot delete branch 'test-branch' used by worktree at '/workspaces/improved-pizza'".

    What does this mean?
    
      This error message means Git is trying to delete a branch but cant do so because a worktree is using that branch. In this case "/workspaces/improved-pizza" is using "test-branch". Git will not let you  delete a branch that is being actively used by a worktree to avoid losing uncommited changes.

    How is this fixed?

      This is fixed by using a different branch within that worktree using "git checkout main".

      After that, "git branch -d test-branch" can be used to delete the branch as the branch that is being deleted is no longer being used by another worktree.
      

  Task 1.4

      


    



     
