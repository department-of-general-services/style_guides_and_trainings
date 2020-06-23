# Pushing to GitHub for Code Jam  
So, you've completed your function. Congratulations! The hard part is over. Now all you need to do is "push" your function to GitHub. This document exists to make that part as easy as possible. Let's break it down into steps. 

1. Save your function as a .py file  
You could copy the function and paste it into Visual Studio Code, then save it as a .py. Or, it's totally acceptable to go the File menu in Google Colab and select "Download .py". Save your submission as `code_jam_{lastname}.py`. So for me it'd be `code_jam_trimarco.py`.

2. Use GitHub Desktop to clone the code jam repo to your local
Make sure you've downloaded and authenticated GitHub Desktop (you'll have to provide it with your GitHub username and password). Then select "Clone repository" from the File menu. You'll see a search bar. Enter "code jam" in the search bar and you should see something like in the image below. Pick a good directory to clone into (the result will also be new directory called `code_jam`) and hit the blue button.

<img src="https://raw.githubusercontent.com/department-of-general-services/style_guides_and_trainings/master/img/code_jam_1.png" width="600">

2. Create a new branch  
In GitHub Desktop, go to the Branch menu and select "Create a new branch." In this case, your branch can just be your last name. 

3. Add your .py file to the repo  
Find the local version of the repo on your computer. It will be in the location selected in the previous step. Drag the .py file containing your function and named `code_jam_{lastname}.py` into the subfolder called "submissions". 

4. Commit your changes  
Go back to GitHub Desktop and make the Current Repository says "Code Jam." Now you should see some information saying that a file has been added. You're ready to commit. Just add a commit message like "Submitting my Code Jam entry" and hit the blue button that says "Commit". 

<img src="https://raw.githubusercontent.com/department-of-general-services/style_guides_and_trainings/master/img/code_jam_2.png" width="500">

5. Push your changes  
You're almost there! Now your code is ready and has been committed to GitHub. The only problem is that it exists only on your local machine. You want to make sure it's visible on the remote repository as well. Luckily, this is easy. There's a dark grey button in the top right corner that say "Publish  branch." Click that, and GitHub will tell you that it's moving data. 

6. Confirm your push in the browser 
This step is optional but I'd do it if it were me. What you want to do is visit the repo's page in the browser, which represents its remote version. In the case of Code Jam, [it's here](https://github.com/department-of-general-services/code_jam). When you get there, you should see a highlighted message saying a branch was recently pushed (see below for an example). If you don't see this, something probably didn't work. Feel free to reach out to me (James) if you want to talk through it. 

<img src="https://raw.githubusercontent.com/department-of-general-services/style_guides_and_trainings/master/img/code_jam_3.png" width="700">