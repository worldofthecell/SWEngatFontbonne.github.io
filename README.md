# Fontbonne Software Engineering Page

## Contents

|Section                            |
|-----------------------------------|
|[Objectives](#objectives)          |
|[Assignment](#assignment)          |
|[Requirements](#requirements)      |
|[Structure](#Structure)       |
|[Procedure](#Procedure)            |


## Objectives

* Learning branching and merging workflow of Git
* Working in a large team to develop software


## Assignment

The objective is to develop a Software Engineering class page with personalized profiles to market our software engineering skills to the employers. The catch is that this will be one big group project with everyone in the class editing the same project folder. Just to clarify, we are not building a webapp with Java or Rails and JavaScript. We are just going to be working with HTML and file structures. 

## Requirements
Collect the following content for your profile.
* A Profile picture (something normal, a headshot, of a reasonable size that can be easily cropped)
* A background picture
* A short bio
* Taglines, favorites, social media profile links. (Not mandatory. You can customize this based on your personality)


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
  * student_name.jpg
  * student_name_background.jpg
  * Add one HTML file to the `students/` folder. Use the `student_name.html` for reference. In fact, feel free to copy as much of the HTML from `student_name.html` into the new file you've created.

## Branching and Merging
A branch is like another "copy" of your repository that you can make modifications to. Suppose you start working on "Project v.1", then you copy it to "Project v.2" to work on a big change (just in case it doesn't work and you want to revert). If it works out, you can copy the changes you made in Project v.2 back into Project v.1 ("merging", in Git). If it doesn't work, you can just delete Project v.2 and try again.
A workflow like this is nice because you can easily undo if you realize the change you made isn't working. Git makes it super easy to go backwards and undo if you work on every new feature on its own branch and only merge when a feature is working (or "stable", as we call it in industry).


### Procedure
In this assignment, we're going to clone the repository and make our changes. When we're done, we'll commit it push into the `master` to send to GitHub.

1.	Clone the repository

2.	Make a new HTML file in the `students/` folder. The file name should be your name. Use the file `student_name.html` to see an example of what a profile's HTML could look like.
  * For instance, we would create a file `john_adams.html` in the main students folder.
  
3.	Add the two photos detailed above to the `img/students` folder. 
  * For example, we would add the pic titled `john_adams.jpg` to the `students` folder inside `img` folder.
  * File endings are case senstive. When adding an <image> tag, make sure that the image source is identical to the name of the image file.
  
4.	Once you've completed the profile, open up `index.html`. Use the pre-existing template as a model and add a section for your profile.

5.	Test your change by firing up `index.html` in your local browser. When everything works and you're ready to commit, go back to sourcetree.

6.	"Stage" your files for commit. 
  a. Git will inform you of files you have modified/created. For example the file you've altered, `index.html`, should appear in the "modifed" section.
  b. Now systematically add each file that you modified and created.

7. Commit your changes 

8. Make sure you get the latest updates by other students working concurrently on this homework by running `git pull`

9.	Open `index.html` again and make sure your changes were merged correctly.

  * While this step should go smoothly, there is a possibility of encountering a merge conflict (because you may have changed some common content and git wouldn't know what to do). In this case Git asks for help. Look at what files it's confused about: `git status`
  * You'll see `index.html` has a conflict, open it up in your favourite editor. Find lines like `<<<<<<<<<`, `===========`, and `>>>>>>>>>`. They show you the 2 versions Git has to choose from.
  * Decide how to fix the file. Maybe it's one or the other. Maybe it's a combination: Change it to include both yours and your classmates changes.
  * Test the change to verify it works and then stage and commit.

10.	Open up `index.html` again. Now you should see your name.

11.	Push your changes to GitHub: `git push origin master`. 
  * This step assumes that you are a collaborator on this project. If you encounter a permission error then email your GitHub ID to the instructor for access.

12. Go to github.io and see your changes

