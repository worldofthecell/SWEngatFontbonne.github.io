# Fontbonne Software Engineering Page

## Contents

|Section                            |
|-----------------------------------|
|[Objectives](#objectives)          |
|[Assignment](#assignment)          |
|[Requirements](#requirements)      |
|[File Structure](#File Structure)       |
|[Branching and Merging](#Branching and Merging)|
|[Procedure](#Procedure)            |


## Objectives

*Learning branching and merging workflow of Git
*Working in a large team to develop software


## Assignment

The objective is to develop a Software Engineering class page with personalized profiles to market our software engineering skills to the employers. The catch is that this will be one big group project with everyone in the class editing the same project folder. Just to clarify, we are not building a webapp with Java or Rails and JavaScript. We are just going to be working with HTML and file structures. 

## Requirements
Collect the following content for your profile.
*A Profile picture (something normal, a headshot, of a reasonable size that can be easily cropped)
*A background picture
*A short bio
*Taglines, favorites, social media profile links. (Not mandatory. You can customize this based on your personality)


## Structure

The structure of this project looks something like this:

```text
├── README.md
├── css
│   ├── css style sheets
│   └── fonts
│       └── font files
├── img
│   ├── lots of images here
│   └── students
│       ├── student_name_background.jpg
│       └── student_name.jpg
├── index.html
├── js
│   └── javascipt files
└── students
    └── student_name.html
```

### Files you will need to alter:
* The only file you'll alter is `index.html`. 

### Files you will need to add:
* Add two pictures to the `img/students` folder (they can be jpg or png files): 
	*student_name.jpg
	*student_name_background.jpg
*Add one HTML file to the students/ folder. Use the `student_name.html` for reference. In fact, feel free to copy as much of the HTML from `student_name.html` into the new file you've created (just don't rename / override that file, as that will cause you some git headaches).

## Branching and Merging
A branch is like another "copy" of your repository that you can make modifications to. Suppose you start working on "Project v.1", then you copy it to "Project v.2" to work on a big change (just in case it doesn't work and you want to revert). If it works out, you can copy the changes you made in Project v.2 back into Project v.1 ("merging", in Git). If it doesn't work, you can just delete Project v.2 and try again.
A workflow like this is nice because you can easily undo if you realize the change you made isn't working. Git makes it super easy to go backwards and undo if you work on every new feature on its own branch and only merge when a feature is working (or "stable", as we call it in industry).


### Procedure
In this assignment, we're going to make a new branch called `add-my-profile-page` and make our change to that copy. When we're done, we'll commit it (to `add-my-profile-page`) and then merge `add-my-profile-page` back into the master to send to GitHub.

*1.	Configure your credentials. Configure your user name with the command `git config --global user.name “your user name”`. You configure your email with the similar command `git config --global user.email “your email address”`. Check your changes by typing `git config user.name` and `git config user.email`.

*2.	Clone your copy of the repository at https:// SWEngatFontbonne.github.io/
3.	See what branch we're on: git branch (the * beside master means we're on that branch)
4.	Make a new branch: git checkout -b add-my-profile-page (the -b means "make a new branch")
5.	See what branch we're on: git branch You'll see 2 branches, with the * beside add-my-profile-page
6.	In this new branch, make a new HTML file in the students/ folder. The file name should be your name. Use the file student_name.html to see an example of what a profile's HTML could look like.
o	For instance, we would create a file john_adams.html in the main students folder.
7.	Still in this branch you created, add the photo detailed above to the img/students folder. 
o	For example, we would add the pic titled john_adams.jpg to the students folder inside img folder.
o	File endings are case senstive. When adding an <image> tag, make sure that the image source is identical to the name of the image file.
8.	Once you've completed the profile, open up index.html. Use the pre-existing template as a model and add a section for your profile.
9.	Test your change by firing up index.html in your local browser. If this was a project, you'd run your work and keep making changes until it worked. When everything works and you're ready to commit, go back to Git Bash
10.	"Stage" your files for commit. 
a)	Start by typing git status. The file you've altered, index.html, should appear in the "Tracked Files" section and the files you've created should appear in the "Untracked Files" section.
b)	Now systematically run git add filename for every file that you updated and created.
11.	Commit your change (to add-my-profile-page branch): git commit -m "Added my 1st page to index.html"
12.	Switch back to master branch: git checkout master (note: no -b)
13.	Open index.html again. Notice that your name isn't in it (because the change is in add-my-profile-page)
14.	Merge add-my-profile-page into master: git merge add-my-profile-page
15.	Open up index.html again. Now you should see your name.
16.	Push your changes to GitHub: git push origin master
17.	Go to github.io and see your changes
18.	Keep your repository tidy! Delete your branch now that it's done: git branch -d add-my-profile-page.
