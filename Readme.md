📌 : Learn hands-on Git and GitHub workflows used in real-world DevOps projects.


: You are working on a new login-page feature and want to merge it back to the main branch.


Clone repository locally.

Create a new branch feature/login-page.

Add a new file login.txt with content: .

Commit the change.

Merge the feature branch into main.

Push updated main branch to remote.




git clone https://github.com/<username>/<repo>.git
cd <repo>
git checkout -b feature/login-page
echo "Login page implemented" > login.txt
git add login.txt
git commit -m "Added login page"
git checkout main
git merge feature/login-page
git push origin main


✅ : login.txt should appear in the on GitHub.




: Your teammate created feature/payment branch on GitHub. You need to continue work on it locally.





Fetch all remote branches.



Checkout the remote branch feature/payment.



Add a file payment.txt with content: .



Commit and push changes to the same branch.




git fetch --all
git checkout feature/payment
echo "Payment Gateway Integration" > payment.txt
git add payment.txt
git commit -m "Integrated payment module"
git push origin feature/payment


✅ : payment.txt should appear in branch on GitHub.




: You need to implement a dashboard feature and push it as a new branch.





Clone the repository.



Create a branch feature/dashboard.



Add file dashboard.txt with content: .



Commit and push to GitHub as a new branch.




git clone https://github.com/<username>/<repo>.git
cd <repo>
git checkout -b feature/dashboard
echo "Dashboard implemented" > dashboard.txt
git add dashboard.txt
git commit -m "Added dashboard feature"
git push origin feature/dashboard


✅ : A new branch feature/dashboard appears on GitHub.




: Your team is releasing versions of the project. Create tags for versions.





Create a lightweight tag v1.0.



Create an annotated tag v1.1 with message .



Push both tags to GitHub.



Delete tag v1.0 locally and remotely.




git tag v1.0
git push origin v1.0

git tag -a v1.1 -m "Bug fixes and improvements"
git push origin v1.1

git tag -d v1.0
git push origin --delete v1.0


✅ : Only tag v1.1 remains on GitHub.




: Two developers edit the same file (app.txt) differently, causing a merge conflict.





User A adds line: → commits and pushes.



User B adds line: → tries to push.



User B pulls from GitHub → conflict appears.



Manually resolve conflict in app.txt.



Commit resolved file and push.




<<<<<<< HEAD
Hello from User B
=======
Hello from User A
>>>>>>> origin/main




Keep both:
Hello from User A
Hello from User B



git pull origin main
# Resolve conflict in file
git add app.txt
git commit -m "Resolved merge conflict"
git push origin main

 


✅ : Conflict resolved and merged changes available in main on GitHub.


📌 :


Submit screenshots of terminal commands and GitHub repository for each assignment.


Each task should show .
