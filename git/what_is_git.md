 
How does Git Actually Work?

Prediction / Assumptions

Git is a version control system. Meaning: 
1. A timeline is Built (in fact multiple) 
2. You can traverse this timeline 
3. You can interact with git via CLI
4. 


For #1:
The timeline is discrete not continuous: The timeline are consisted of elements. Which are sum representations of the files / directories at a given point of time. 

the git add, push, commit cycle is the mechanism to an element add to this timeline. 

How do add to the timeline? (Methodologically) 

Files begin in your local machine. Then when you make a ‘commit’ you essentially make a set of ‘git objects’ which represent your files & directory structure (and essentially have all of their information relevant to git). This is staging. 

For 2#: 
git reset and rebase are the tools to traverse this timeline. 

git reset: pulls you back to a specific point
git rebase: builds the git history such that changes in a ‘flat manner’. Events are played ontop of each other such that the history log is easier to view. 


Analogy: Flashpoint

In the Flash (tv show), flashpoint is arc where he goes back in time to save his mother, from his reverse flash. In git terms, the Flash essentially, when back on the timeline and made a new branch. 

git branch flashpoint
git switch flashpoint
git reset (“to man with the yellow lighting” event) 
git commit -m “saving mama” 
git push origin flashpoint



* the timeline analogy might now work for explaining git’s multi-person communication capabilities though.


