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
