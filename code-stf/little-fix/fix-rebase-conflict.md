So I had a conflict in my PR

I go `git pull upstream master`

Then I go `gitui`

and I get to see some unstaged file hanging

so they say `rust` use submodule and git don't track some file thingy

I had to go `rm -rf src/tools/cargo/`

and `reset` it in unstaged till shiny and clean

so I can switch to my local brach and `rebase` on master

it says `appending` and **HERE IS WHERE I NORMALLY GET PANIC BUT FIXED IT TODAY!**

I go to `staged` and move the conflict file up to `unstaged`

so I can `diff` and spot the conlict between `=====` `<<<<<<`

I open that file defaultly with `helix` since I did `export GIT_EDITOR=hx`

I goto conflic by `s===n`

*I fix the conflic in a swift, end of story*

But actually I had a bigger trouble

**my PR branch is not my actively working branch**

I spent my time fixing my PR branch but not my working one

So I want my *change of code* go directly to my working branch

I don't know how to do that with git!

So I opened that conflict file in another terminal from `PR branch`

Then I go back to previous terminal and switch to my `local branch`

and I go foward to editor terminal and do good old `:w`

and that's it.

it cost me like 5 sec to write real code

I mean, it's something I wish I knew when I do all this shit.

🍻
