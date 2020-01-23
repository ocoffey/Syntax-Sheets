# Walkthrough for setting up and using Github/Git

Hello all! I'm writing this as a brief walkthrough for getting up and running with using Github through the command line. I will not be writing this for use with Github Desktop (as I've never used it). The first section of this walkthrough is about getting your free student pack that github offers. The second section will be about actually using git commands effectively, and improving your workflow from it!

## Github Pro Student Pack

All students with a .edu email have free access to the Github Student Developer Pack. The pack can be found [here](https://education.github.com/pack, "Github Student Developer Pack").

If you have your URI email already linked to your github account, you can click "Get the Pack", fill out your information, and you should receive an email shortly that confirms you got the pack!

If you made a github account without a .edu email, you can go into your settings and add your .edu email to your list of emails in the account, and then follow the steps above!

By having Github Pro, you have access to creating free, private github repositories. You should make use of the privacy for any repositories you create for your courses!

### Make a repository for this course

Once you have github pro, go to github's homepage, and in the upper left next to repositories, click "new". For this page, enter your repository name (typically something like csc_212 or the like), make the repository private, and check to let it initialize with a README. We'll be making use of this repository further down!

## Ways of using/installing Git

### CS50 IDE

If you're previously used to CS50 IDE and have been using it for this course, the shell environment already has git installed, so you can skip down to Config.

### Mac and Linux

Mac and Linux don't always have git preinstalled, but the installation is easy.

For Mac, open Terminal, and type `git` + `enter`. It should open a window to install developer tools (accept this, and you should be all set).

For Linux, open Terminal, enter `git` as above, and it should install the package after you accept.

### Windows Subsystem for Linux

For those purely using Windows, I recommend using the Windows Subsystem for Linux. Unfortunately this method is a bit more drawn out than Mac/Linux, but is still well worth it.
> Note: This method will only work on Windows 10, and will not work on older versions of Windows.

#### Installing WSL and Ubuntu

---

First, we need to enable the ability of installing the WSL. To do this, right click the Windows icon (your start menu), and choose "Windows Powershell Admin". Then, copy this command:

`Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux`

Paste it into Powershell, and run it. When complete, you'll need to restart your system.

Upon restart, go to the Microsoft Store, search "Linux", and install Ubuntu (the version without the numbers) [feel free to install a different version if you'd like].

#### Installing and Connecting VS Code

---

For this tutorial, we will be installing VS Code, and making it so that our linux shell is integrated into the program.

1. First, download and install VS Code (link [here](https://code.visualstudio.com/, "VS Code")).
2. After installing VS Code, go to the "Extensions" tab (the 4 blocks along the left side of the windows), and install the "Remote Development" extension.
3. After doing so, you should be able to click the bottom left of your window, and open a new window within the Windows Subsystem for Linux! 
4. You can close the old window, keeping the new one open. Then, enter `ctrl` + ` to open the terminal.
5. Now, you should be able to see your discs by inputting `ls /mnt`. Suggesting that you want to use your C drive for storing files, we can mount the disc with `cd /mnt/c`, and then traverse the disc to a folder that you want to make as your Github folder!

> If you want to make a Github folder within your Documents folder, you can change directory as such: `cd Users/your-username-folder/Documents`. From there, you can create a github folder with `mkdir Github`.

## Actually Using Git

Now that the setup process is done, we need to tell git who we are! 

### Config

We have to tell git our github email and our name. To tell your email, enter

`git config --global user.email "your_email@example.com"`

and to tell your name, enter

`git config --global user.name "Your Name"`

### Pulling a Repository

Now that we've told git who we are, we can pull and push files. We'll start with the repository we made earlier!

1. If you're not still on the repository page, go to the upper right to your profile, and click "Your Repositories". Then click the one you just made.
2. On the right side of the page you should see a green button that says "Clone or Download"; click that, and copy the link!
3. Now, go to whatever terminal you have. Since we previously installed git, all we have to do is `git clone link-that-we-copied-from-earlier`, and enter your github username and password!

> Note: When entering the password, it will not tell you which characters have been entered (for privacy), so make sure to be precise (backspace will also still work if needed).

You should see some things happening in the terminal, and then it should be downloaded locally! Now change directory into the folder using `cd`.

### Add

Now that we downloaded our repository and are inside, let's make a simple python file to try and push to github! To start, let's make a file from the command line, we can enter `echo "This doesn't do anything" > sample.py`.

Now, we're going to push this file to our repository! The first step is entering `git add filename`, where `filename` in this case is `sample.py`. This will stage a change in our repository.
> Note: You can add multiple files to the same staged change by just adding their names afterwards. As an example, if we also edited the README, we could do `git add sample.py README.md`.

### Commit

Now that our change to the repository is staged, we can commit this change by entering `git commit -m "pertinent-message-here"`, where `pertinent-message-here` is a message that describes the changes we made. As an example for our change, we could enter `git commit -m "created sample.py"`.

### Push

Now, we want to push those changes to our repository. To do this, just enter `git push`, and enter your Github username and password when prompted. If you check github, your change should be there!

## Branching (a good practice)

In developing code, it's good to have a working program to test with (even if the program isn't completed yet). As an example, say you wanted to write a program that read information from a file (say, weather readings from the past month), manipulated that data somehow (maybe predicting an average for each week), and then output that manipulation to a different file. This program would have three main sections to it, being:

1. Read data from a file into variables/lists/something else
2. Do something with the data
3. Store the data

You would probably work on the in that order, too; only working on the 'doing something with data' part after you figured out how to 'read data from a file'. Now, to explain how this relates to branching.

All repositories have one branch to start, named `master`. By making other branches, it allows us to have working (if not fully completed) code in our repository stored in `master`, while we develop in a different branch! So as you finished one of those large sections, and have tested your code for it, _then_ you would push that branch to master. Now, to see it in action.

First, we need to make a new branch to work within! The easiest way to do this is with `git checkout -b branch_name`, where `branch_name` is whatever name we choose (for this example, we could choose a name like `dev`, short for development). 
> Normally you have to create a branch before you check it out, but the -b flag allows to do this in one step, by creating, then checking out the branch.

Now, if you enter `git branch`, you should be able to see both `master` and the branch name you chose! Let's do some edits within our branch.

If you solely want to use the command line, we can enter something like `echo "another test" > test.py`. You can also edit or create a file within your IDE or file browser instead.

Once we've made this or some other change to this branch, we can do `git add file-name` and `git commit -m "created a new file"`. Our push is going to look a little different though: we're going to enter `git push -u origin branch_name`. This enables us to push to our github branch instead of to master.

After entering your username and password the push goes through, we can go to github to our repository! A button should appear to compare and pull request; click that, and open a pull request. After that, there should be another button to merge with no issues!

Finally, after a successful merge, in our terminal, checkout master again with `git checkout master`, and do a `git pull` to get our local master up to date with our changes. But make sure to switch back to your branch again before doing edits!

*Hopefully soon I will edit this walkthrough with pictures and more links and such. If you've made it this far and understand it, you're well on your way to having a better development cycle!*
