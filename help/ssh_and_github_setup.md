etting Up SSH

Assumptions:

You have Git installed and typing "git --version" in Terminal tells you which version you have (any version is fine, most recent is good) ---- if you do not, then https://git-scm.com/download/mac
You are fine with storing SSH keys somewhere on your computer; or on a thumbdrive, or wherever
---STEPS---

Open Terminal

Go into whatever directory you would like for storing all the files (http://www.dummies.com/how-to/content/how-to-use-basic-unix-commands-to-work-in-terminal.html)

$ chflags nouchg ~

(to change permissions)

https://help.github.com/articles/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent/

$ ssh-keygen -t rsa -b 4096 -C "your_email@example.com"

(hit enter) (enter passphrase 2x)

(to test...)

$ eval "$(ssh-agent -s)"

$ ssh-add ~/.ssh/id_rsa

https://help.github.com/articles/adding-a-new-ssh-key-to-your-github-account/

$ pbcopy < ~/.ssh/id_rsa.pub

go to https://github.com/marsupial-borging/bandicoot

find the green button "Clone or download"

use the ssh option...

$ git clone

aka...

$ git clone git@github.com:marsupial-borging/bandicoot.git

(now to see what has cloned! if successful (caveat))

$ ls

(you should see the "bandicoot" folder)

$ cd bandicoot

$ ls

(you should see this README...so meta...)

$ vi README.md (this is if you want to see the text...)

(to edit, just start typing from wherever you are...you go instanlty go to the end by typing "g")

$ :q (to exit vi mode after zero edits added, if you do edit, then ESC to exit INSERT mode)

$ :wq (to save and exit)

(also...) $ q! (to exit and discard any edits)

(we probably should do some configging here...to identify yourself)

$ git config --global user.email "you@example.com"

$ git config --global user.name "Your Name"

(let's also add a remote address too...)

$ git add remote origin git@github.com:marsupial-borging/bandicoot.git

$ git remote -v (to check)

$ git status (to check your status, see what changes have occurred that you might want to commit)

(if you made changes you'll want to commit the changes with a message...)

$ git commit -am "Hi! I just changed something and here's what changes I made"

$ git status (to check that things happened)

$ git push (it might tell you a better command and just use that if so)

(if you are a success, you will see a success message with lots of 100%s)

