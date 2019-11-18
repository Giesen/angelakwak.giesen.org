# angelakwak.giesen.org



## Notes to self on how to use git and Hugo. It is not complete but just a cheat sheet.


### Move to project directory

First in the bash shell move to the project directory. Most of the command work from within this directory.

```bash
cd ~/Projects/angelakwak.giesen.org <ENTER>
```

## Get the latest changes from github

e.g. because my husband fixed a few things.
This will get the latest changes locally.

```
git pull <ENTER>
```

## Create a new post locally

```bash
hugo new post/my_greatest_new_post.md <ENTER>
```


## Edit the post


```bash
vim content/post/my_greatest_new_post.md <ENTER>
```
Do not forget to set `draft:false` or remove that line altogether if you want to publish the new post.

## Exit vim with saving

Either one of:

* `shift ZZ`
* `: wq!`


## Commit changes locally

```bash
git add content/post/my_greatest_new_post.md <ENTER>
git commit -m `A new post was added, how wonderful` <ENTER>
```

This will commit the changes to the current branch locally. Nothing will change remotely.

## Push the locally commited changes to github and get it published on the blog

```bash
git push <ENTER>
```

## Work on mobile phone

For this to work you need to have your *ssh* key configured in github and in your .ssh directory. Here the rights should be set correctly.
> e.g. If you want to blog from you mobile phone you have to copy the .ssh directory to your home directory within termux and set the rights correctly. And then you have to install hugo, git and openssh/openssl in termux.
> *Termux* is a linux shell on Android.

## vim tutorial

Self explaining vim tutorial
```bash
vimtutor <ENTER>
```


## References

* [Hugo blogging tool](https://gohugo.io/)
* [Git official Documentation](https://git-scm.com/docs) *Everything but a bit advanced. There is a book and there are videos*
  * [Git basics, what isversion control, the video](https://git-scm.com/video/what-is-version-control) 
* [Oh Shit, Git!?!](https://ohshitgit.com/) *For if you screwed up. But a bit advanced*
* [git cheat sheet](https://github.github.com/training-kit/downloads/github-git-cheat-sheet.pdf)
* [Vim basics](https://www.howtoforge.com/vim-basics) 
* [Vim cheat sheet](https://vim.rtorr.com/)


## tutorial videos

* [Vim Tutorial for Beginners: Learn the Vim Editor in 5 minutes](https://www.youtube.com/watch?v=PN-r83wYMug)
* [How to use vim](https://www.youtube.com/watch?v=g-XsXEsd6xA)
* [The vim tutorial, Basic commands](The Vim Tutorial - Part One - Basic Commands) *Part one of a series*



