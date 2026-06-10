### Git References & Namespaces 

Understanding what branch you're on can be annoying. Understanding the syntax of Git References && Namespaces should alleviate that pain. 

The first thing to note is that the **Git Reference**  is a 'pointer' to a commit hash.  The are organized into namespaces using the forward slash. '/'

*All References are stored as files under .git/refs/* 

Every reference has a fully qualified name (its complete path from refs/)

i.e. 

refs/heads/main -> main
refs/remotes/origin/main -> remote-tracking ref for main on remote origin 

There are two important Namespaces 

### refs/heads/ -- Local Branches 
These are Local branches that you commit to directly 
### refs/remotes/<remotes>/
These are the local **cache** of remote branch state 

## Semantic Distinction: main vs origin/main
These are two independent refs that may point to different commits at any given time.
main (local branch)

Located at refs/heads/main
Modified by local operations: commit, merge, reset, rebase
Represents the user's working line of development
Updated automatically as the user commits

origin/main (remote-tracking branch)

Located at refs/remotes/origin/main
Modified only by network operations: fetch, pull, push, clone, remote update
Represents a cached snapshot of the remote's main at the time of the last synchronization
Read-only from the user's perspective; never directly committed to
May be stale relative to the actual remote until the next fetch
