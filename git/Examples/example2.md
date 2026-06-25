### Fetch is a git command

It's the standard method to pull in a remote repository into your local machine. Here's a common scenario, You've stepped away from a project, and you aren't sure if you've made any changes, since you operate on multiple machines. 

You run: 
`git fetch origin main`

Ushering in the remote origin's main branch!

Now, on your machine, you have your current main branch, and whatever main branch exists on the web (origin/main) , at the same time! 

Here are two more options: 

1) Switch to the Remote Branch Directly 

`git switch --detach origin/<remote-branch-name>`

2) Create a local Branch from that Remote

`git switch -c <new-local-branch> origin/<remote-branch-name>`
