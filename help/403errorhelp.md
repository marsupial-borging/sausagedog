thub seems only supports ssh way to read&write the repo, although https way also displayed 'Read&Write'.

So you need to change your repo config on your PC to ssh way:

edit .git/config file under your repo directory
find url=entry under section [remote "origin"]
change it from url=https://MichaelDrogalis@github.com/derekerdmann/lunch_call.git to url=ssh://git@github.com/derekerdmann/lunch_call.git. that is, change all the texts before @ symbol to ssh://git
Save config file and quit. now you could use git push origin master to sync your repo on GitHub
