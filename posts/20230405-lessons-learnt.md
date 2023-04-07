%{
  title: "How to force pull in Git ?",
  tags: ["git","force_pull"],
  published: true,
  discussion_url: "https://www.scaler.com/topics/git/git-pull-force/",
  description: Git force pull
   
}
---


### How does force pull work in Git ? 
![conceptual explanation](../images/gitpullimage.png)


### How to implement force pull in Git ?
1. Git fetch = retrieves all changes from the remote repository and stores them locally in your Git repository.
2. Git checkout -b <branch name> = creates new branch 
3. Git reset --hard origin/<branch name> = This will resets our current branch to match the state of the specified remote branch.  

