# Data Skills – Week 3 Worksheet

## Managing a project with Git

<YOUR NAME>

*Total: 20 points (point values for each question shown below)*

### Part 2: Core Git workflow

1.  (1 pt) During Part 2, step 4, you viewed your repository on GitHub.com after committing the addition of DataSkills_Week3_Activity.md. Was the file `DataSkills_Week3_Activity.md` present on the remote?

> The file `data/DataSkills_Week3_Activity.md` was not present on the remote. 

2.  (1 pt) During Part 2, step 5, you pushed the commit to the GitHub remote. After this action, was the file `DataSkills_Week3_Activity.md` present on the remote?

> The file is now present on the remote. It does not have my answer to quetion 1 in it, because I wrote that answer after the commit was made.

3.  (2 pts) Explain the reason for any difference between your answers to questions 1 and 2. Make sure you understand the difference between committing locally and pushing changes to the GitHub remote.

> When I added the file and made a commit, git packaged the changes (adding the file) along with the commit message, but left it on my local machine. I could make multiple commits with different changes all kept locally as little snapshots of the changes I have made, but none of them would show up on the remote until I pushed those changes. Then, the commits that I choose to push (usually all of them) are reflected on the remote.

4.  (2 pts) During Part 2, step 7, you examined the History panel. What do you see shown for DataSkills_Week3_Activity.md? Is the entire file shown? What do the colors mean?

> When I open up the history for the worksheet file, I see a git diff. This shows the old version (on the left) and the version with the changes applied (on the right). I see red highlights on the right showing the lines that I deleted. in this case, I deleted three lines that all say `<YOUR ANSWER>`. There are also dashed areas with no line numbers under these red areas that show the space that is taken up by the incoming edits which are shown to the right. On that right side I just see my three answers highlighted in green. These areas show the additions I made to the file. In addition to the red and green highlights, the diff shows little + and - symbols next to the line numbers. 

5.  (1 pt) During Part 3, step 4, you toggled between branches on GitHub.com. What differences did you see between `main` and `new-analysis` branches?

> When I toggle the branch to `new-analysis` then I see a new push and it says that it is '1 commit ahead of `main`'. When I go into the `src/` folder, I can see `src/main.py` with my 'analysis code'.

> After switching back to the `main` branch, I can no longer see the `src` folder that holds `main.py` on my `new-analysis` branch. I can't see the folder because it only contains one file (`main.py`) on the local machine, and git does not track the folder before it has a file inside of it that git is tracking. The reason that `main.py` is not available is because the commit that I made was created on the `new-analysis` branch, so when I pushed that commit, it only exists on that branch. This means that `main` is 1 commit behind `new-analysis`. However, it doesn't say that like it did when I was in that branch because `main` is the default branch so the other branches are tracked compared to it.

6.  (2 pts) During Part 3, step 5, you changed your local branch from `new-analysis` to `main`. After doing this, look at the location where you had saved your new script. What do you see? Why? What happened?

> When I clicked back to checkout `main`, I saw the `src` folder disappear, but the `data` directory still exists which is interesting. The `src` folder and `src/main.py` are both gone, which makes sense becauase those changes were not sent to the main branch since that commit was made on the `new-analysis` branch. I find it interesting that local folders like `data` still exist even though they are not tracked by the branch, but the `src` folder was removed because it is not tracked. I am guessing this is because when I committed `main.py` to the `new-analysis` branch, it saved the operation of creating `main.py` in `src/`. Then, when I did git checkout to the `main` branch, it saw that the difference between the branches was to create that folder & file, so it undid that change (thereby deleting the directory as well as the file) in order to match my local files to the remote.

7.  (1 pt) During Part 3, step 6, you changed your local branch back to `new-analysis`. After doing this, look at the location where you had saved your new script. What do you see? Why?

> The script is back, along with the `src/` folder. This is because it redid the committed operation that separates `main` from `new-analysis`. In other words, the difference between `main` and `new-analysis` is one commit, and the change saved by that commit is to create `src/main.py` and add the one line of code `print("HELLO DATASKILLS")`. When I did checkout to `new-analysis` it restored my local state to that of the branch by making those changes that differentiate the two branches. If the branches were separated more, such as if I had made commits on main as well, then it may have to undo local changes to revert back to where they were the same, then redo the changes that separate the two branches.

8.  (1 pt) During Part 3, step 8, you created a pull request. Describe what you see on the pull request page.

> On the Pull Request page, I see a page titled 'Comparing changes'. It has a little box that shows `base:main` <- `compare:new-analysis` and 'Able to merge'. This shows me which branch I am merging with which, and that they do not have any comflicts. It also allows me to add a title and description. Below the description box is a 'Create pull request' button that also lets me create a draft pull request if I wish. Underneath is some more information about the new-analysis branch that I am merging. This includes the number of commits, files changed, contributors, and the commits and file changes in question are shown below that.

9.  (2 pts) During Part 3, step 11, you have merged your branches and are back on the `main` branch. Look again at the location where you had saved your new script. What do you see? Is your answer any different to your answer to question 6?

> it looks great. It looks like how my local files looked when I was on the new-analysis branch, not the main branch, since they are merged and there is currently no difference between them.

10. (1 pt) To be answered by your neighboring collaborator: What is your name?

\<COLLABORATOR'S NAME\>

11. (1 pt) To be answered by you (repo owner): After pulling changes, what do you see as the answer to question 10, above? Did you write those answers?

<YOUR ANSWER>

12. (1 pt) What is the best flavor of ice cream?

<ANSWER>

13. (2 pts) During Part 4, step 7, you attempted to push changes that likely conflicted with changes your collaborator had made. What happened? Explain, step by step, what you had to do to resolve the merge conflict.

<YOUR ANSWER>

14. (1 pt) During Part 5, step 1, you chose to ignore a file by choosing one of three options. Explain how you would envision using each of these three options in practice. Which one did you choose in this case, and why?

<YOUR ANSWER>

15. (1 pt) Please provide the URL to your (private) GitHub repository:

<YOUR ANSWER>
