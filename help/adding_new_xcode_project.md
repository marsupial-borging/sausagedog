First, use this tutorial --

https://github.com/codepath/ios_guides/wiki/Using-Git-with-Terminal

Then if you encounter a 403 error use this ---

http://stackoverflow.com/questions/7438313/pushing-to-git-returning-error-code-403-fatal-http-request-failed

aka

Github seems only supports ssh way to read&write the repo, although https way also displayed 'Read&Write'.

So you need to change your repo config on your PC to ssh way:

edit .git/config file under your repo directory
find url=entry under section [remote "origin"]
change it from url=https://MichaelDrogalis@github.com/derekerdmann/lunch_call.git to url=ssh://git@github.com/derekerdmann/lunch_call.git. that is, change all the texts before @ symbol to ssh://git
Save config file and quit. now you could use git push origin master to sync your repo on GitHub
