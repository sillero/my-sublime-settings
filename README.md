### What?

I synced my **[Sublime Text 2](http://www.sublimetext.com/2)** settings files to github

### Why?

So I can have the same packages and settings at work, at home and on the move with my macbook

### And why didn't you use that other method with Dropbox/Google Drive?

I did, but it can present serious problems on sync. This is way is more safe for me, so it can avoid conflicts.
I update my settings when I start to code in a new machine and commit and push when I'm done with it.

### How?

1. Close Sublime Text 2
2. **The most !important step: BACKUP YOUR FILES**:<br/>
Location on **Mac OS X** `~/Library/Application Support/Sublime Text 2/`<br/>
Location on **Windows** `%appdata%\Sublime Text 2\`
3. Create a new repo on github, preferably with a name other then `Sublime Text 2` 
to avoid confusion and mistakes. Something like my-sublime-settings
4. Clone the repo to your computer. I like to keep my repos on a single `github/` folder.
5. Copy the files from your backup folder on **step 2** to the `/your/path/to/github/my-sublime-settings` folder
6. _(optional)_ Tell to your `.gitignore` file to ignore the `/your/path/to/github/my-sublime-settings/Backup` folder 
by adding `Backup/` to it (this can be a very large folder)
7. Commit and Push
8. Delete the original `Sublime Text 2` folder on the locations in **step 2** (must be done in every computer you are in)
9. Create symbolic links to replace the original `Sublime Text 2` folder (must be done in every computer you are in):

**Mac OS X**<br/>

    cd ~/Library/Application\ Support/
    ln -s /your/path/to/github/my-sublime-settings Sublime\ Text\ 2

**Windows**<br/>

    cd %appdata%\Sublime Text 2\
    mklink /D "Sublime Text 2" "/your/path/to/github/my-sublime-settings"

Now all you gotta do is update your repo before you open Sublime Text 2 and commit and push by the end of the day.

Some might not like to update and commit every time you start or stop to code, so you can automate this.<br/>
I'm sure there are lots of tutorials on automating repo sync on github. So, Google it my friends :)

