# Recovering a Lost GitHub Contribution Streak

Sometimes you forget to commit your work to GitHub and your contribution streak breaks.
Git allows you to create a commit and **set the commit date manually**, which can restore your contribution streak on GitHub.

This guide explains the process step-by-step in simple terms.

---

# Requirements

Before starting, make sure you have:

* Git installed on your computer
* A local project folder connected to GitHub
* A GitHub repository

Git is the version control system used to track changes in your project.

---

# Step 1: Open Your Project Folder

Open the terminal and go to the folder of your project.

Example:

```
cd my-project
```

---

# Step 2: Add the Changes

Tell Git which files you want to save.

```
git add .
```

This command adds all modified files to the staging area so they are ready to be committed.

---

# Step 3: Commit With a Custom Date

Now create the commit but **manually specify the date**.

```
GIT_AUTHOR_DATE="2026-02-20 10:30:00" \
GIT_COMMITTER_DATE="2026-02-20 10:30:00" \
git commit -m "Updated project files"
```

Explanation:

* **GIT_AUTHOR_DATE** → the date when the work was originally done
* **GIT_COMMITTER_DATE** → the date when the commit was recorded
* **git commit -m** → saves the changes with a message

Both dates are set the same so Git records the commit on that exact day.

---

# Step 4: Push the Commit to GitHub

Send the commit to GitHub so it appears on your contribution graph.

```
git push origin main
```

Replace `main` with your branch name if different.

---

# Step 5: Check Your Contribution Graph

Go to your GitHub profile.

If the repository is public (or private contributions are enabled), the commit will appear on the **selected date** in your contribution graph.

---

# Example Workflow

```
git add .
GIT_AUTHOR_DATE="2026-02-20 10:30:00" GIT_COMMITTER_DATE="2026-02-20 10:30:00" git commit -m "Bug fixes"
git push origin main
```

---

# Important Notes

* The date must be in the format:

```
YYYY-MM-DD HH:MM:SS
```

Example:

```
2026-02-20 10:30:00
```

* The commit will appear on the selected day in Git history.
* This method works best when the date is **not in the future**.

---

# Conclusion

By setting the commit date manually, you can add commits to a previous day and keep your GitHub contribution streak active.

This technique is useful when you worked on a project but forgot to commit it on that day.
