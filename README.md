# ABDN 2026 Demo: Git & GitHub for fNIRS Research

This repository is your safe space to explore, experiment, and learn without breaking anything.

## 📂 What is in this Repository?
This repository serves as a sandbox for our collaborative coding exercise. Inside, you will find:
*   **Sample fNIRS Open Dataset:** An open-source fNIRS dataset for you to practice loading and analyzing.
*   **Demo Scripts / Notebooks:** Starter code snippets to help you see how version control tracks changes in actual analysis files.
*   **README.md:** This file, which contains your instructions for the hands-on exercise.

---

## 🛠️ Getting Started: How to Do the Exercise

Your goal is to practice the core Git workflow: **Clone → Branch → Edit → Commit → Push → Pull Request**. 

Depending on your comfort level and setup, you can complete this exercise using either a local environment (VS Code) or a cloud environment (Google Colab).

### Step 1: Do you need to download Git?
*   **If using Google Colab:** No! You do not need to install Git or download anything to your computer. Colab is browser-based and handles it for you.
*   **If using VS Code:** Yes. You need Git installed on your computer to track changes locally. 
    *   *Windows:* Download from [gitforwindows.org](https://gitforwindows.org/)
    *   *Mac:* Open your Terminal and type `git --version`. If it's not installed, your Mac will prompt you to install the Command Line Tools.

---

### Step 2: Choose Your Coding Environment

Choose **Option A** (VS Code) for a full development experience, or **Option B** (Google Colab) for a quick, zero-install exploration.

#### Option A: Using VS Code (Local Environment)
*VS Code requires a bit more setup but provides a full project development environment*.

1. **Clone the Repository:** 
   * Open VS Code.
   * Click **Clone Git Repository** on the Welcome screen (or use the terminal: `git clone https://github.com/Huimin1640/ABDN_2026_Demo.git`).
   * Select a folder on your computer to save the project.
2. **Create Your Own Branch:**
   * Do not work on `main`! 
   * Open the VS Code terminal and type: `git switch -c your-name-branch` (replace with your actual name).
3. **Make an Edit:**
   * Open any script or text file in the repository, add a comment (e.g., `# Reviewed by [Your Name]`), and save the file.
4. **Commit and Push Your Changes:**
   * Open the **Source Control** tab (the branch icon on the left).
   * Click the **`+`** icon next to your changed file to stage it (this is the equivalent of `git add .`).
   * Type a short message in the box (e.g., `"Add my name to the file"`) and click **Commit**.
   * Click **Publish Branch** to push your branch to GitHub.
5. **Create a Pull Request:**
   * Go back to this repository on GitHub.com.
   * Click the green **Compare & pull request** button to propose adding your changes to the main project.

#### Option B: Using Google Colab (Cloud Environment)
*Colab is excellent for first-time coding because it is browser-based with no setup required*.

1. **Open Colab:** Go to [colab.research.google.com](https://colab.research.google.com/) and click **New Notebook**.
2. **Clone the Repository:**
   * In the first code cell, run this command to safely download a copy of the project:
     ```python
     !git clone [https://github.com/Huimin1640/ABDN_2026_Demo.git](https://github.com/Huimin1640/ABDN_2026_Demo.git)
     ```
3. **Navigate to the Folder:**
   * In a new cell, move inside the downloaded folder:
     ```python
     %cd ABDN_2026_Demo
     !ls
     ```
4. **Explore Safely:**
   * Click the **Files icon (folder)** on the left sidebar to see the downloaded files. 
   * You can open the demo notebooks directly in Colab and run them. *Note: Because pushing changes back to GitHub from Colab requires advanced authentication steps, we are using Colab strictly to **find, clone, and run** code today!*

---

## 📌 Your Git Cheat Sheet
*Keep these commands handy!*

| Command | What it does |
|---|---|
| `git clone <URL>` | Download the project to your environment |
| `git branch` | See all available branches |
| `git switch -c <name>` | Create a new branch and move onto it |
| `git status` | Show what files have changed |
| `git add .` | Choose all current changes to include in the next checkpoint |
| `git commit -m "message"`| Record a checkpoint locally |
| `git push origin <branch>`| Send your branch from your computer to GitHub |
| `git pull origin main` | Get the latest changes from GitHub to your computer |


## ⚠️ Common Errors & Troubleshooting

Run into a problem? Don't worry, every experienced developer has seen these errors! Here is how to fix them:

### VS Code Issues
*   **"I cloned the repository, but I can't see any files on the left!"**
    *   *The Fix:* You need to tell VS Code to open the specific project folder. Go to **File > Open Folder...** (or **Open...** on Mac) and select the `ABDN_2026_Demo` folder you just downloaded. Also, ensure you have clicked the **Explorer icon** (two overlapping sheets of paper) on the far-left menu bar.

### Common Git Command Errors
If you are using the terminal, you might see one of these messages:

*   **`fatal: not a git repository`**
    *   *Why it happens:* You are not inside the cloned folder.
    *   *The Fix:* Run `cd <folder-name>` (e.g., `cd ABDN_2026_Demo`) first.
*   **`error: failed to push some refs`**
    *   *Why it happens:* Someone else pushed changes first.
    *   *The Fix:* Run `git pull origin main` to get the latest changes, then try pushing again.
*   **`Permission denied`**
    *   *Why it happens:* This is an authentication issue.
    *   *The Fix:* Ask the instructor for help—do not spend session time troubleshooting alone.
*   **`nothing to commit, working tree clean`**
    *   *Why it happens:* There are no new changes yet, or they were already committed.
    *   *The Fix:* Check your repository state by running `git status`.
*   **Merge conflict markers in a file**
    *   *Why it happens:* Git needs you to choose between two versions of a file that changed in the same place.
    *   *The Fix:* Ask the instructor for help—this is a normal part of collaboration.