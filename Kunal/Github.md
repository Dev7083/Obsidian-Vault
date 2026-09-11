1. What is Git?
	- A **version control system**.
	- Tracks changes in your code
	- Lets you go back to previous versions
	- Saves history of your project

2. What is GitHub?
	- A cloud platform by GitHub
	- Stores your Git repositories online
	- Helps in collaboration

3. Flow:
	1. Create/modify files
	2. `git add` → move to staging
	3. `git commit` → save snapshot
	4. `git push` → upload to GitHub

4. Ways :
	 - GitHub Desktop
	 - Command Line
	 - Git Features of IDE(VS Code)
5. Git Commands:
```powershell
	git init              # start repo
	git clone <url>       # copy repo
	git status            # check changes
	git add .             # stage all files
	git commit -m "msg"   # save changes
	git push              # upload to GitHub
	git pull              # get latest changes
```

6. Typical Flow:
```powershell
	git init
	git add .
	git commit -m "Initial commit"
	git remote add origin <repo-url>
	git push -u origin main
```

## 5. Branching (Very Important)

- Default branch → `main`
- Create new branch:

`git checkout -b feature`

👉 Use branches to:

- Work on features safely
- Avoid breaking main code

## 6. Merge Concept

- Combine branches into main

`git merge feature`

## 7. Merge Conflicts

- Happens when same file changed in multiple places
- You manually fix and commit again

## 8. Local vs Remote

- **Local repo** → your computer
- **Remote repo** → GitHub

## 10. Key Concepts to Remember

- Git = tool
- GitHub = platform
- Commit = snapshot
- Branch = parallel work
- Push/Pull = sync


Beginner Workflow (Real Use)

```bash
git clone repo-url
# make changes
git add .
git commit -m "added feature"
git push
```