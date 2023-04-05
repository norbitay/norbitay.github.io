# zhili-liu.com

The source for [zhili-liu.com](https://zhili-liu.com). The website is built from Jekyll
website builder.

This file is written in Markdown. If you are using Visual Studio Code, choose to preview
this file to see a nicely formatted version.

## Working with this website

The best way make changes to this website is to use Visual Studio Code. That will give
you an application where you can see what files exist and where you can change files.

This website works using a "website builder". What that means is you create a number of
files, then run a command and it will create the website from those files

Most of the files you write will be written in Markdown. Markdown doesn't let you do a
lot, but it has the advantage of ensuring all your pages follow the same style. Fancy
formatting is still possible, but you should try to only use Markdown unless necessary.
Trust me on this!

Your overall process looks something like:

1. Start running the website on your computer
2. Make the changes you want and check that the changes look right
3. Commit and publish your changes

The sections below give you steps to do each of these.

## Run the website on your computer

You should test changes on your computer before uploading to your website. That way
you know what it will look like before everyone else knows.

Follow the steps below to test locally:

1. Open a terminal window in the same folder as this README file. You can do this in a
   a couple ways:

   If you are using Visual Studio Code, select the *Terminal* tab.
   Otherwise, select the Windows Start button, then type Terminal, finally change to
   the directory containing the file.

2. In the terminal window, input the command to start your website locally:

   `bundle exec jekyll serve`

   You will see some output, eventually ending with something like the following:

   ```
   Auto-regeneration: enabled for 'C:/Users/norbi/Website/norbitay.github.io'
    JekyllAdmin mode: production
     Server address: http://127.0.0.1:4000
    Server running... press ctrl-c to stop.
   ```

   The key part is the *Server running*. Now your website is running on your computer.

3. Navigate to your website from your computer. You can either click the link in the
   terminal output or directly go to http://127.0.0.1:4000 in a web browser.

   Once the website is running, you can edit files on you computer and it will update
   the website automatically. See the next section for details.

4. Stop your local website by typing *Ctrl + c*.

   You will be prompted twice with `Terminate batch job (Y/N)?`. Input `y` then press `Enter`
   twice.

## Adding pages

### Blog posts

1. Create a new file in `_posts` for the new blog post. The file
   name begins with the date followed by a name that shows in the
   URL.
   
   The easiest way to do this to copy an existing post and then
   rename the file.
2. Open the file you created and edit the information in the header.
   
   That's the part at the top between the first `---` and the second
   `---`.
3. Create a picture for the blog post. The size should be
   1280 x 720 px (but doesn't be). The picture MUST go into the folder `assets\blog`.
   
   Give it a descriptive name so that you remember what the name is.
   
   Take note of the file extension. It is a `.png` or `.jpg` file.

   In the header section, make sure that `post-image` has the right file name.

## Commit and publish your changes

Once you are satisfied with the changes as viewed from your computer, you need to update your
real website. 

### Using Visual Studio Code

1. In the left toolbar, choose **Source Control**. The Source Control view shows.

2. You will see a list of files that were changed. Some may be new, deleted or just changed.
   You need to tell Git (that's the thing that keeps track of files) which changes you REALLY
   want. For example, just because you deleted something, doesn't mean that it is really gone.

   For each file, click the plus sign. The file moves to a section titled **Staged Changes**.

3. Input a message describing what you changed, then select **Commit**

4. Publish your changes by selecting **Sync Changes** (the button text changes once you committed from
   the prior step).

### Using a Terminal Window

1. In the terminal window, input the command below to see what changes you made:

   `git status`

   You will see a list of files that changes. Check that the files you think you changed are
   actually what was changed.

2. In the terminal window, input the command below to indicate you want add of the changed
   files to be changed on your website.

   `git add *`

3. In the terminal window, input the command below to commit the changes. You should put in a message
   to indicate that what changed.

   `git commit -m "I changed something"`

4. In the terminal window, input the command below to publish your changes so that your website updates:

   `git push`

