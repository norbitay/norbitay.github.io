# zhili-liu.com

The source for [zhili-liu.com](https://zhili-liu.com). The website is built from Jekyll website builder.

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

## Checking locally

You should test changes on your computer before uploading to your website. That way
you know what it will look like before everyone else knows.

Follow the steps below to test locally:

1. Open a terminal window in the same folder as this README file. You can do this in a
   a couple ways:

   If you are using Visual Studio Code, select the *Terminal* tab
   Otherwise, select the Windows Start button, then type Terminal, finally change to
   the directory containing the file.

2. In the terminal window, input the command to start your website locally:

   `bundle exec jekyll serve`

3. Navigate to your website from your computer. You can either click the link in the
   terminal output or directly go to http://127.0.0.1:4000 in a web browser.

   Once the website is running, you can edit files on you computer and it will update
   the website automatically.

4. Stop your local website by typing *Ctrl + c*.

   You will be prompted twice with `Terminate batch job (Y/N)? y

## Commit and publish your changes

Once you are satisfied with the changes as viewed from your computer, you need to update your
real website. 

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

