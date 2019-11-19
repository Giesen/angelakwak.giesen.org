# angelakwak.giesen.org



## Notes from Hans to Angela on how to use Git and Hugo. 

It is not complete but just a cheat sheet.


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

```bashT
git push <ENTER>
```

## Test locally

 * Do not `git add`
 * Dot not `git commit -m ..`
 * And certainly do not `git push`

Testing a new blog post locally can be done by running the *Hugo test server* locally from you blog directory.

```bash
hugo -D server <ENTER>
```

By using the the `-D` flag, draft posts will become visible too.
You can see the  blog by browsing to `http://localhost:1313`.
This is a great way to try out new layout and proof read a post.

The *Hugo test server* servers your blog from memory and watches changes on the file system. If you keep it running. 
All changes are reflected immediately in your browser window. The best way to do this (for now) is keep the hugo test server running in a separete *Git Bash* window.
Later you will learn multiple ways to do this from within one terminal window.


## Deleting an already published blog posts

One way to permanently delete a published post just delete the file locally and commit/push the changes.

```bash
rm content/post/blog_post_that_I_would_like_to_delete.md <ENTER>
git add content/post/blog_post_that_I_would_like_to_delete.md <ENTER>
git commit -m "deleted that ugly post" <ENTER>
git push <ENTER>
```

You can also delete it via the *GitHub* web interface, but then do not forget to `git pull` the change locally.

Finally you can do the change using `git rm`. I Never use that.


### Adding an image


You can add an image to a Hugo blog in 3 ways.

1. Refer a `featuredImage` in the header metadata. This will put the image at the top of your post or in whatever position the blog thheme you use, shows it.
2. Normal markdown via `![link caption or alt text](https://images.example.com/my_awesome_photo.jpg)`  This is similar to a link but it is preceded by a bang (`!`).
3. Use [Hugo shortcodes](https://gohugo.io/content-management/shortcodes/). This allows you to embed pieces of html or Hugo template scripting to do things not possible with vanilla Markdown.

Using a featuredImage The variable `featuredImage` sadly does vary on the skin you use. If you change your blog theme you must change this variable for all blog posts that use it.

For some popular photo platforms such as *Instagram* buildin shortcodes exist. So far I have not seen such a thing for *Flickr*.

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
  * [Git basics, what is version control, the video](https://git-scm.com/video/what-is-version-control) 
* [Oh Shit, Git!?!](https://ohshitgit.com/) *For if you screwed up. But a bit advanced*
* [git cheat sheet](https://github.github.com/training-kit/downloads/github-git-cheat-sheet.pdf)
* [Vim basics](https://www.howtoforge.com/vim-basics) 
* [Vim cheat sheet](https://vim.rtorr.com/)
* [Markdown cheat sheet](https://guides.github.com/pdfs/markdown-cheatsheet-online.pdf)
* [Mastering markdown](https://guides.github.com/features/mastering-markdown/)
* [Add an image using normal Markdown](https://www.markdownguide.org/basic-syntax/#images-1)
* [Hugo shortcodes](https://gohugo.io/content-management/shortcodes/)

## tutorial videos

* [Vim Tutorial for Beginners: Learn the Vim Editor in 5 minutes](https://www.youtube.com/watch?v=PN-r83wYMug)
* [How to use vim](https://www.youtube.com/watch?v=g-XsXEsd6xA)
* [The vim tutorial, Basic commands](https://www.youtube.com/watch?v=ER5JYFKkYDg)



