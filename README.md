# Learn `jj-vcs` (Jujutsu Version Control)

Welcome to **Learn `jj-vcs`**, a beginner-friendly guide to [Jujutsu Version Control (jj)](https://github.com/jj-vcs/jj). `jj` is a modern version control system designed to simplify common workflows and improve on Git’s history management, all while staying fully compatible with existing Git repositories.

This project will guide you through everyday version control tasks, from committing and pushing changes to managing your project's history. You'll learn to use `jj` locally for a smoother workflow while continuing to use platforms like GitHub for collaboration.

---

### 💡 Why Learn `jj`?

* **Cleaner History:** `jj` rethinks how version control works, making it easier to create and maintain a clean, linear history.
* **Git Compatibility:** It works seamlessly with Git, so you can keep using GitHub, GitLab, and other platforms without any migration.
* **Local-First:** All of `jj`'s powerful features are local. You can rewrite history, amend commits, and reorder changes without affecting your remote repository until you're ready to push.

---

### 🧑‍💻 Who is this for?

* Developers who use Git for daily tasks like `commit`, `push`, and `pull`.
* Anyone new to `jj`—no prior experience with Jujutsu is required.
* Those curious about a simpler, faster, and more intuitive version control system.

---

### 📦 What you'll learn here

* How to set up and manage a repository with `jj`.
* How to commit, inspect, and share your changes.
* How to use `jj` alongside GitHub for collaborative work.
* A solid foundation for moving on to more advanced `jj` workflows.

---

## 🚀 Getting Started

Before you begin, make sure you have the following tools installed and set up.

### ✅ Prerequisites

* A GitHub account or another Git hosting provider.
* **Git** installed on your system.
* **`jj` (Jujutsu)** installed on your system.

---

### 🛠️ Installing `jj`

You can install `jj` using your system’s package manager or from source. For official installation instructions, visit the link below.

👉 [jj-vcs.github.io/jj/latest/installation](https://jj-vcs.github.io/jj/latest/installation)

After installing, confirm everything is working by checking the version and listing the available commands.

```bash
jj --version
jj help
```

---
### 🤝 Git Compatibility

`jj` works seamlessly with Git repositories. You can use `jj` commands in any Git-managed folder, and they will work as expected.

* **`jj git clone`** to clone GitHub-hosted repositories.
* **`jj git push`** to push your changes as Git commits.
* Your existing Git configuration (`.gitconfig`) will apply automatically.

No migration or conversion is needed—just start using `jj`.

---

### 📥 Clone a Repository

To start working with a GitHub-hosted project, you can clone it using the `jj` command just like you would with Git.

```bash
jj git clone [https://github.com/](https://github.com/)<your-username>/<your-repo-name>.git
```

This creates a local workspace with the repository contents. The `jj` metadata is stored in a hidden `.jj/` folder, and your repository is now fully compatible with `jj` and Git.

---

### 🔍 Explore the Working Copy

After cloning, you will have a local copy of your repository and a clean working copy ready for changes. The **working copy** is the current state of your files on disk.

In `jj`, the `@` symbol represents your working copy. Use `jj status` to see its current state.

```bash
jj status
```

---

### 📝 Make Your First Change

Open a file, like `README.md`, in your editor and add some simple text. For example, a single line at the bottom:

```md
This is my first experiment using `jj` instead of `git`.
```

---

### ✅ Commit the Change with `jj`

Unlike Git, `jj` tracks your working copy continuously. To commit your change, you'll first create a new, empty change on top of your current one, and then describe it.

```bash
# Start a new change
jj new

# Add a message to describe the change
jj describe -m "📚 docs(readme): add a first test line using jj"
```

A common shortcut is to do this in a single step using the `-m` flag.

```bash
jj new -m "📚 docs(readme): add a first test line using jj"
```

You can inspect the new change using `jj log`.

```bash
jj log
```

---

### 🚀 Push to GitHub

When you’re ready to share your changes with the remote repository:

```bash
jj git push
```

`jj` will automatically convert your change to a Git commit and push it to the remote, just as you would expect.

---

