F431103
Daniel Lean

List of files in repository

  Daniel_Lean_ARDUINOSETUP - an image file containing a picture of an arduino and temperature sensor plugged into a laptop
  
  24WSA024_JNB_Arduino_Coursework_Final_2025S2(V1).ipynb - The notebook containing the entire coursework brief
  
  README.md - A file containing documentation of the coursework tasks

Task 1

  Task 1.1 

    Why cant the student find their private repository when trying to save their notebook to github?

      This could be because the student skipped a step to authorize private repository access when they first connected colab to github

    How does google colab access repositories and how can the level of access by decided?

      Google colab interacts with github through OAuth tokens and API requests. The level of access depends on the permissions granted on the OAuth page

    How can you verify that your authentication settings are working correctly?

      If authentication is working, a selection from a list of both public and private respositories should appear when saving to github
      

  Task 1.2

      A Github action for Automated task tracking using codespaces was implemented
      

  Task 1.3

    What did i do?
    
      I started by creating a new branch using "git checkout -b test-branch"

      I then immediately tried to delete it with "git branch -d test-branch"

      It returned the error message "error: cannot delete branch 'test-branch' used by worktree at '/workspaces/improved-pizza'"

    What does this mean?
    
      This error message means Git is trying to delete a branch but cant do so because a worktree is using that branch. In this case "/workspaces/improved-pizza" is using "test-branch". Git will not let you  delete a branch that is being actively used by a worktree to avoid losing uncommited changes

    How is this fixed?

      This is fixed by using a different branch within that worktree using "git checkout main"

      After that, "git branch -d test-branch" can be used to delete the branch as the branch that is being deleted is no longer being used by another worktree
      

  Task 1.4

    What did i do?

      I started by creating a new branch by running "git checkout -b feature-branch"

      I created a new markdown file named "project-notes.md" by running "echo "Initial notes for the project." > project-notes.md"

      I then opened the markdown file in a text editor and modified it by typing "This is an update from feature-branch."

      I then staged and commited the change using "git add project-notes.md" and "git commit -m "Updated project-notes.md from feature-branch""

      After that, I pushed the branch to github with "git push origin feature-branch"

      Following on, I switched back to the main branch using "git checkout main" and created a markdown file called "project-notes.md" in the main branch

      I modified this file by adding "This is an update from main." and commited the change by running "git add project-notes.md" and "git commit -m "Updated project-notes.md from main""

      I pushed the changes using "git push origin main"

    At this point i have two conflicting changes in the same file but it different branches

      I then attempted to merge feature-branch into main using "git merge feature-branch" however Git displayed an error indicating a merge conflict in project-notes.md 

      This happens because the same file was modified in different ways across different branches. When a merging of these branches is attempted, Git does not know which version to keep

    How to solve the merge conflict?

      Start by opening the conflicted file in the codespaces editor to see the conflicts. 

      Then remove or alter the conflicts

      In order to mark the conflict as resolved, run "git add project-notes.md"

      Then continue the rebase process with "git rebase --continue"

      Then push the resolved changes back to the remote

      Finally, commit the message "git commit -m "Resolved merge conflict in project-notes.md""

      It should return "Resolved merge conflict in project-notes.md"

    What caused the merge conflict in this scenario?

      There were contradictory changes to one file in two different branches. merging these branches was not possible as it didn't know which changes to keep

    Why does Git prevent automatic merging when conflicts occur?

      Two or more people have made changes to a file. Git cant decide which change is correct as it is a computer therefore it does nothing. This is done in order to prevent data loss. As during the merging process, changes are overwritten. Furthermore, only a developer can decide how to combine or prioritize conflicting changes.

    How can you prevent merge conflicts when working in a team environment?

      Merge conflicts can be prevented by communicating effectively among team members. This could include assigning specific tasks to different people as to dissalow more than one person from working on the same task. Additionally, if changes are pulled regularly from the remote, It is ensured that the team is working with the latest base code. Furthermore, if branches are kept short lived and focused this can help prevent merge conflicts as there is less contained within the branch and a lower chance of a conflict.

    What steps can you take to check for conflicts before merging changes?

      First, make sure you have the latest version of the remote branch

      Simulate the merge locally without pushing

      After a test merge, run: git status

      Compare your branch with the target branch

      Open a pull request to trigger automatic merge checks
      
      GitHub will show if the branch can be merged automatically or if conflicts exist

    What are the consequences of forcing a push without resolving a merge conflict?

      This can lead to serious and sometimes irreversible problems within a Git repository such as: loss of others work (may overwrite commits made by team members), broken history (breaks continuity of the project), team disruption (anyone who pulled the branch before the forced push will have a diverged history), unresolved conflicts remain (conflict markers remain in code causing build or runtime errors.
      







  

      


    



     
