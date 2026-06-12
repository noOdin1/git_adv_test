<h1>Git command - More git commands practice JS @87%</h1>

<h3>REMINDER: Cloning remote repo</h3>
If you encounter errors like the following: 
>> $\> git clone git@github.com:noOdin1/TOP_curriculum.git
>> Cloning into 'TOP_curriculum'...
>> git@github.com: Permission denied (publickey).
>> fatal: Could not read from remote repository.

You can verify the ssh key being used:

> > ssh -T git@github.com
> > if this throws an error that means your ssh-key is not available
> > for this ssh session. You need to start the ssh key daemon first.
> > eval "$(ssh-agent -s)"
> > This will load the agent to memory. Now to load the key for
> > the github repo that you wish to clone into:
> > ssh-add ~/.ssh/some_ssh_key_file
> > This will add the ssh key for gmail account for
> > github (account being used for TOP).

Then rerun the following command to verify:

> > ssh -T git@github.com
> > output:
> > Hi noOdin1! You've successfully authenticated, but GitHub does not provide shell access.
> > This shows that the proper ssh key has been loaded and you're ready to
> > clone that repo.
