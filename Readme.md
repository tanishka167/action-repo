# Action Repo – GitHub Webhook Trigger

This repository is created solely for testing and triggering GitHub webhook events such as:

-  Push
-  Pull Request
-  Merge

The webhook for this repository is connected to a Flask server hosted in a separate repository: [`webhook-repo`](https://github.com/Pragat2021/webhook-repo).

---

## Purpose

This repo is used to:

- Trigger GitHub events that are captured by a Flask server
- Test integration of GitHub with webhooks
- Simulate real repository activity (push, PRs, merges)

---

## How to Use

### 1. Make a Push

```bash
git clone https://github.com/Pragat2021/action-repo.git
cd action-repo
echo "test" >> test.txt
git add .
git commit -m "Testing push event"
git push


 2. Open a Pull Request
Create a new branch:

bash
Copy
Edit
git checkout -b test-branch


Make a change and push it:

bash
Copy
Edit
echo "another test" >> test2.txt
git add .
git commit -m "PR test"
git push --set-upstream origin test-branch

Open GitHub and create a pull request to main or master.





 3. Merge a Pull Request
Once the PR is reviewed, merge it on GitHub. This will trigger a pull_request with action: closed and merged: true.
