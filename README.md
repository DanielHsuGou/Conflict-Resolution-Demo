# Conflict-Resolution-Demo

Test Conflict

1. Create Fork, clone to own (SSH key) repo first
   - git clone <SSH key>
   - cd <cloned folder>
   - (README created)
   - (Now the org & own repo have the same README)
2. Change code in organization (in github)
3. Change code in local at same location as above // use own repo
4. git add, commit, push origin main code to own account
   - if not set public flag => follow instruction enter email/username
   - git log, git status to check
5. Try to create pull request from own account and fail to merge automatically // in github
6. git remote add upstream YOUR_ORG_SSH_KEY // login/connect to org repo to my repo
   - git remote -v // list all remotes
7. Pull org code with git pull --rebase upstream main // pull connected repo to my repo // ←rebase to resolve the github own repo’s ahead and behind
8. Resolve conflict // conflict occur
   - Choose any of current/incoming/both => save
   - git add . // confirm conflict is resolved
   - git rebase –continue
   - "Please enter commit message for your changes" <yellow message> = commit message, to change this, press “a” or “i” to enter message above => ESC => at bottom enter :wq or :x
   - Result: git log = github’s difference in commits
9. push to own repo
   - git push –force origin main // dont use in organization account
   - git push upstream
   - Result: 1 own repo’s ahead
10. create pull request fm own account // in git
    - Attention: pull to org main will auto deploy to website
    - Set reviewers / assignees if your org need it
    - select draft pull request if not sure
    - once created pull request (green button), can only close request (remain forever)
11. merge all request // in git
    - Result: same org & own repo, not uptodate
12. git pull --rebase upstream main
13. git push –force origin main
    - uptodate
