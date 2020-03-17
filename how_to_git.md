# Standard git flow
## 0. Make sure you have a working command-line tool
Assuming you're operating in a Windows environment, you'll need to set up a tool to use the command line. Here are a few options:

- The portable command-line [emulator called Cmder](https://cmder.net/) handles the command-line side of git well. 
- Another option is [Git For Windows](https://gitforwindows.org/), which includes a full-featured Graphical User Interface as well. 
 
## 1. Create a repo (if you don't have one) and clone it locally
If you're starting a new repository, you'll want to use the browser to log into your agency's Github and create a new repository. 

Once that's done -- or if you're working on a pre-existing repository -- then you need to "clone" the repo to make a local copy. For most use cases, this local directory is where the coding, writing, and other development activities take place: 

1. In the brower, navigate to your repo and click the green button called "Clone or download." You'll see a URL with an icon of a little clipboard next to it. Click the clipboard to copy the URL.
2. Leave your browser and enter a command-line tool such as Cmder.
2. Use [Linux-style navigation commands](https://www.digitalocean.com/community/tutorials/basic-linux-navigation-and-file-management) like `pwd`, `cd`, and `ls` to navigate to the parent directory where you want your local repo to live.
3. Type `git clone` into the command line, and then paste the url copied in step one above. 
4. Type `ls` in the command line. You should see a folder with your repo in it. 
5. Go ahead and `cd` to enter that folder. Now try typing `git status`. You should get a meaningful message with information about what branch you're on. If you instead get the error message `fatal: not a git repository`, then use the `pwd` Linux command to make sure that you're navigated into the repo.  

## 1. Decide what you want to do and create an issue.
It is a best practice in Git to first decide what you intend to do and only then begin making changes to code and documentation. (Some approaches would include getting your team's approval too). GitHub has this logic built-in in the form of _issues_. A good first step before coding is to envision a medium-sized chunk of work — larger than a commit, but smaller than a repository — and then follow these steps: 

1. Open your repository in the browser and click on the _Issues_ tab. 
2. Click the green button that says "New issue."
3. Give your issue a meaningful name and perhaps a detailed description. 
4. Click the green button that says "Submit new issue", then take note of your issue's number (it will be rendered in grey type). This number will be important in step two.

## 2. Create a branch to match your issue
The following is not the only way to handle git branching patterns, but it might be the simplest and clearest. It takes advantage of some under-the-hood Git features too: 


1. Create a new branch to hold all the commits related to your issue by typing `git checkout -b issue_x`, with the number of your issue in place of the `x`. 
2. Now that you're on the right branch, you're ready to start typing up your code, text, or other work. 

## 3. Stage and commit your changes 
You'll want to "commit" your changes whenever it feels like a meaningful small step has been completed. Commits are important because anyone who's interested in your work can use them to understand the history of work on your project (and this includes future you!)

When it's time to commit, follow these steps:

1. First **get a sense of what's going on** by going `git status`. This command will show all the files that have changed, and which you can consider staging. 
2. Next, **stage the files you want git to track** by going `git add app.py`. It's possible to add everything with the command `git add *`, but it's better not to, since that command can add all sorts of junk to your commit history. 
3. When you're satisfied that you've staged all the files you want your next commit to track (`git status` will show the updated staging), you're ready to actually commit by typing `git commit -m "Your message here"`. It's very important that the commit message be informative, since commit messagese will be a main source of info for future readers trying to understand your repo. 
4. Repeat steps 1 to 3 as needed, until your issue is completed. If you can remember, it's good to make the last commit message for the issue be `git commit -m "closes #1`. This will save you a step by automatically closing issue 1 as soon as your changes are pushed. 
5. Finally, you can populate your local changes to the main remote repo by going `git push origin issue_1`.

## Create a pull request for your issue  
When you switch back to the Github page for your repo in the browser, you'll now see an alert saying that changes have come in from branch `issue_1`. Now you want those changes merged into the master branch, so that the changes in your issue are included in it. 

The standard way to request this kind of merging is called a "Pull Request", and the most common way to put an issue's worth of changes into a request is with the browser:

1. Navigate to your repo in the browser. If you've just pushed code, there'll be a yellow strip with an alert reading "You recently pushed branches". Push the green button that says "Compare & pull request." 
2. The next page is the one where we open a pull request. We can give the PR a brief description (this should be very similar to the issue description, but may have more notes on implementation). If there's a particular person you want to review your code, you can assign reviewers on this page too. When all of that's done, click the green button saying "Create pull request."   
3. The next page is the review page for the pull request. In an ideal world, the reviewer of the PR will not be its author. So at this point you can let your teammates know that a PR is ready for review. 
4. If you're moving through issue on your own and just want to merge in changes, GitHub will let you know if any conflicts have come up. If they have, you'll need to resolve them. 
5. If there are no conflicts with the base branch, you can click the green button that says "Merge pull request," and the changes will be merged.
6. This is a great opportunity to delete the old branch, `issue_1`. Once the branch has been merged, there's no reason to keep it around cluttering things up. 
