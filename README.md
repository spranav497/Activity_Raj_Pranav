Step 2: Team Lead B creates remote repository
Create a repository named fintech-app on GitHub/GitLab.

Step 3: B adds A as collaborator

Step 5: B clones the repository
git clone https://github.com/b/fintech-app.git
cd fintech-app

Step 6: B makes a change
echo "// Added by B" >> app.js
git add app.js
git commit -m "B added comment"
git push

Step 9: B merges feature branch
git checkout main
git pull
git merge origin/feature-login
git push

B edits without pulling:

sed -i '2s/.*/Line 2 updated by B/' README.md
git add README.md
git commit -m "B updated README"
git pull