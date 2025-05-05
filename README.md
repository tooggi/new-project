# new-project

## Git Workflow: Using a Development Branch

This guide explains how to use a `development` branch to work on changes and later merge them into `main`.

---

### 1. Clone the Repository

```bash
git clone git@github.com:your-username/your-repo.git
cd your-repo
```

### 2. Create and Switch to the `development` Branch
```bash
git checkout -b development
```

> This creates a new branch based on `main` (or whatever branch you're currently on) and switches to it.

### 3. Make changes and commit
Make any code changes in your editor (e.g., VS Code).

Then:

```bash
git add .
git commit -m "Describe your changes here"
```

### 4. Push the `development` branch to remote (first time only)

```bash
git push -u origin development
```

> `-u` links the local development branch to the remote one.

### 5. Switch back to `main`

```bash
git checkout main
```

### 6. Update your local `main` (optional but recommended)

```bash
git pull origin main
```

### 7. Merge `development` into `main`

```bash
git merge development
```

If there are no conflicts, it will fast-forward or create a merge commit.

### 8. Push the updated `main` to remote

```bash
git push origin main
```
