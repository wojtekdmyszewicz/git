# git

https://github.com/thoughtbot/gitsh

## Filtering commmits

narrow it down to 5 search results

git log -n 2000 | grep -C 5 "club"


## Duplicating a repository (Bitbucket, GitHub)

It uses:

git clone --mirror: to clone every references (commits, tags, branches)

git push --mirror: to push everything

That would give:

git clone --mirror https://bitbucket.org/exampleuser/repository-to-mirror.git

Make a bare mirrored clone of the repository

cd repository-to-mirror.git

git remote set-url --push origin https://github.com/exampleuser/mirrored

Set the push location to your mirror

git push --mirror



Create the branch on your local machine and switch in this branch : 

<pre>$ git checkout -b [name_of_your_new_branch]</pre>

Push the branch on github : 

<pre>$ git push origin [name_of_your_new_branch]</pre>

When you want to commit something in your branch, be sure to be in your branch.

You can see all branches created by using : 

<pre>$ git branch</pre>

Which will show :

<pre>* approval_messages
  master
  master_clean</pre>

Add a new remote for your branch : 

<pre>$ git remote add [name_of_your_remote] <url></pre>

Push changes from your commit into your branch :

<pre>$ git push origin [name_of_your_remote]</pre>

Update your branch when the original branch from official repository has been updated : 

```sh
$ git fetch [name_of_your_remote]
```
Then you need to apply to merge changes, if your branch is derivated from develop you need to do : 

<pre>$ git merge [name_of_your_remote]/develop</pre>

Delete a branch on your local filesystem : 

<pre>$ git branch -d [name_of_your_new_branch]</pre>

To force the deletion of local branch on your filesystem : 

<pre>$ git branch -D [name_of_your_new_branch]</pre>

Delete the branch on github : 

<pre>$ git push origin :[name_of_your_new_branch]</pre>

The only difference is the : to say delete, you can do it too by using github interface to remove branch : https://help.github.com/articles/deleting-unused-branches.
