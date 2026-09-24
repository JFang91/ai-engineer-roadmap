# From Rusty to Hired: a 12-Month Roadmap to an AI / Software Engineering Role

**Sept 9, 2026 → Sept 12, 2027**

---

## How to use this document

- This is a living checklist. Change `- [ ]` to `- [x]` as you finish things.
- In Week 1 you will put this file into your own GitHub repository as the README. From then on, checking a box and committing it is a git rep. Your commit history becomes the record of the year.
- Every phase ends with a **Done when** checkpoint. Move on when the checkpoint is met, not just because the calendar says so. If you're two weeks past the phase's end date and still not done, see *If you fall behind* near the bottom and move on anyway.
- Any term or name you don't recognize is defined in the **Glossary** at the bottom. Read the glossary once now, then use it as a lookup.
- Hours in parentheses are estimates for a rusty-but-not-beginner learner. You'll be faster on some, slower on others.
- Links were checked in September 2026. If one dies, search the title.
- The order of items matters less than doing them. Consistency beats perfection every single week.

---

## The goal, precisely

- **Target role:** AI Engineer (primary) or Software Engineer with an AI focus (secondary), at a startup or mid-size company. Big tech is the stretch. Machine Learning Engineer roles at large companies become realistic 1–2 years *after* this first role.
- **Target date:** an offer by September 2027.
- **What you'll be able to show by then:**
  - 3 deployed projects, each with real evaluation and a README that reads like an engineer wrote it
  - A GitHub profile with 12 months of consistent commits
  - 150 solved algorithm problems and the ability to solve a new medium in 30 minutes
  - A trained-from-scratch GPT you built by hand, and can explain
  - 3+ short technical blog posts
  - At least one merged open-source contribution
  - 6+ people in the industry who know you and can refer you

---

## Ground rules

1. **Consistency over intensity.** ~15 hours every week for 50 weeks beats 40-hour bursts and a crash. Protect the habit before anything else. Missing one day is fine; never miss two in a row.
2. **Build more than you consume.** Cap videos and reading at ~40% of your time. The rest is typing code, solving problems, and shipping.
3. **AI as tutor, not author — for the first six months.** Use Claude to explain, quiz you, and review your code. Do not let it write the code. If you can't explain a line, you don't get to commit it. **Turn off AI autocomplete in your editor** (Copilot and similar) during Phases 0–2. From Phase 3 on, flip this: AI engineers are expected to be excellent with tools like Claude Code and Cursor, and by then you'll be able to judge the output.
4. **Everything goes on GitHub.** Commits are your proof of work. Nobody can argue with a green contribution graph.
5. **Work stays at work.** You work in a regulated environment (GMP, HIPAA, 21 CFR Part 11). Nothing from your employer — data, queries, documents, code, screenshots — goes into personal projects, personal accounts, or personal AI tools. Use a personal computer and personal accounts for everything in this plan. Public datasets only.
6. **Extra hours go to projects, not more videos.** If you have a 20+ hour week, spend the surplus on the current project or on extra algorithm problems. Never on a fourth course.

---

## Your week (~15 hours)

| When | Length | What |
|---|---|---|
| Weekday mornings, before work (Mon–Fri) | 60–90 min | Course material, reading, or project work. Mornings because nothing has gone wrong yet. |
| Weekend block A (Sat or Sun) | 4–5 h | Project work only. One long uninterrupted block. |
| Weekend block B (the other day) | 2–3 h | Algorithm problems + weekly review + commit "Week N done". |
| At work | 0 personal hours | Write every SQL query yourself first, then let AI review. See *What to do at work*. |

**If you have 20+ hours this week:** add one more algorithm problem (4 instead of 3), do the optional hard problems, and put the rest into the project. In Phase 2 the surplus goes to Karpathy's optional video 9. In Phase 3 it goes to a second open-source contribution.

**Sunday ritual (15 min, every week, all year):** check the boxes, write 3 lines in `log.md` (what worked, what didn't, what's next), commit and push. This is non-negotiable and it's the smallest habit in the plan.

---

## People you'll see named in this plan

- **Andrej Karpathy** — Stanford PhD, founding member of OpenAI, led AI at Tesla, now runs an education company (Eureka Labs). His free YouTube series *Neural Networks: Zero to Hero* is widely considered the single best way to learn how neural networks and language models actually work. You build them from scratch in plain Python, line by line.
- **3Blue1Brown** (Grant Sanderson) — YouTube channel with the best visual explanations of linear algebra, calculus, and neural networks.
- **Aurélien Géron** — author of *Hands-On Machine Learning*, the standard practical ML textbook.
- **Chip Huyen** — author of *AI Engineering* (2025), the textbook for the role you're targeting, and *Designing Machine Learning Systems*.
- **Hamel Husain** — ML engineer (ex-GitHub, Airbnb) whose writing on *evals* is the reference for how to test AI products.
- **Sebastian Raschka** — author of *Build a Large Language Model (From Scratch)*.
- **NeetCode** (Navdeep Singh) — ex-Google engineer whose free site organizes the 150 algorithm problems that interviews actually draw from.
- **Andrew Ng** — Stanford professor, co-founder of Coursera; his ML courses are the classic gentle introduction.

---

# Phase 0 — Weeks 0–2: Setup and Diagnostic
**Wed Sept 9 – Sun Sept 27, 2026**

Goal: know exactly where you're starting from, have every tool working, and have the habit started. **Do not start "studying" yet.** Measure first.

## Week 0 — Wed Sept 9 to Sun Sept 13: Accounts, tools, orientation (~6 h total)

### Decide your machine
- [ ] Use a **personal** laptop (Mac, Windows, or Linux — all fine). Not the work laptop. No GPU needed; everything in this plan runs on a normal laptop or in free cloud notebooks.
- [ ] If you don't have a personal laptop: GitHub Codespaces gives you a full development environment in the browser with a free monthly allowance → https://github.com/features/codespaces. Google Colab gives free notebooks with a GPU for the deep-learning phase → https://colab.research.google.com/

### Create accounts (all free) (~30 min)
- [ ] GitHub → https://github.com/signup — pick a professional username; this will be on your resume
- [ ] LeetCode → https://leetcode.com/ (free tier is all you need)
- [ ] NeetCode → https://neetcode.io/ (free tier is all you need)
- [ ] Exercism → https://exercism.org/
- [ ] Kaggle → https://www.kaggle.com/
- [ ] Hugging Face → https://huggingface.co/join

### Install tools (~1 h)
- [ ] **VS Code** (code editor) → https://code.visualstudio.com/
  - Install the **Python** and **Jupyter** extensions from the Extensions panel (Ctrl/Cmd+Shift+X)
  - **Disable any AI autocomplete** (Copilot etc.) if present. Rule 3.
- [ ] **Git** (version control) → https://git-scm.com/downloads (Mac: run `xcode-select --install` in Terminal instead)
- [ ] **GitHub CLI** (makes signing in painless) → https://cli.github.com/ — then run `gh auth login` in your terminal and follow the prompts
- [ ] **uv** (installs Python and manages packages; replaces pip/venv/conda) → https://docs.astral.sh/uv/getting-started/installation/
  - Then run `uv python install 3.12` in your terminal
- [ ] Verify: open a terminal and run `git --version`, `gh --version`, `uv --version`. All three should print a version number.

### Orientation (~4 h, over the weekend, no coding)
- [ ] Watch Karpathy's **Deep Dive into LLMs like ChatGPT** (3.5 h, made for a general audience) → https://www.youtube.com/watch?v=7xTGNNLPyMI
  - This is your "what am I getting myself into" video. It explains how the models you use every day are actually built. You won't understand everything. You're not supposed to yet. Write down 5 things you want to understand better; you'll come back to that list in Phase 2.
  - Short on time? His 1-hour version: **Intro to Large Language Models** → https://www.youtube.com/watch?v=zjkBMFhNj_g
- [ ] Read this whole document once, including the glossary.
- [ ] Set up your calendar: block the weekday mornings and two weekend blocks as recurring events through September 2027. Treat them like meetings with your boss.

## Week 1 — Mon Sept 14 to Sun Sept 20: Diagnostic (~13 h)

The point of this week is a written list of what you still know, what's fuzzy, and what's gone. That list decides how much of Phase 1 you can skip. Be honest with yourself — there are no points for pretending.

### Monday (75 min): learn git and GitHub by doing
- [ ] Complete GitHub Skills — **Introduction to GitHub** (interactive, in the browser, ~1 h) → https://github.com/skills/introduction-to-github
  - You'll learn what a repository, branch, commit, and pull request are by making them.

### Tuesday (75 min): your first real repo
- [ ] On GitHub, click **New repository** → name it `ai-engineer-roadmap` → Public → check "Add a README file" → Create.
- [ ] In your terminal:
  ```bash
  git config --global user.name "Your Name"
  git config --global user.email "you@example.com"
  git config --global init.defaultBranch main

  # go to a folder where you keep code, e.g.
  mkdir -p ~/code && cd ~/code
  gh repo clone <your-github-username>/ai-engineer-roadmap
  cd ai-engineer-roadmap
  ```
- [ ] Replace the `README.md` in that folder with **this file** (rename it to `README.md`).
- [ ] Create an empty `log.md` for your weekly notes.
- [ ] Commit and push:
  ```bash
  git status                     # see what changed
  git add README.md log.md
  git commit -m "Add 12-month roadmap"
  git push
  ```
- [ ] Refresh the repo page on GitHub. Your roadmap should be there, with checkboxes rendered. **This is your first commit of the year.**
- [ ] Read Pro Git, Chapter 1 (Getting Started, ~30 min) → https://git-scm.com/book/en/v2/Getting-Started-About-Version-Control

### Wednesday (75 min): algorithm diagnostic, part 1
Solve in Python on LeetCode. **20 minutes max per problem.** If you're stuck at 20 minutes, stop, write down where you got stuck, and read the solution. No AI help. Record for each: solved alone / solved with hints / couldn't.
- [ ] Two Sum → https://leetcode.com/problems/two-sum/
- [ ] Contains Duplicate → https://leetcode.com/problems/contains-duplicate/
- [ ] Valid Anagram → https://leetcode.com/problems/valid-anagram/

### Thursday (75 min): algorithm diagnostic, part 2
- [ ] Valid Palindrome → https://leetcode.com/problems/valid-palindrome/
- [ ] Best Time to Buy and Sell Stock → https://leetcode.com/problems/best-time-to-buy-and-sell-stock/
- [ ] Then skim the official Python tutorial, sections 3–5 (~30 min) → https://docs.python.org/3/tutorial/introduction.html — note anything that looks unfamiliar (list comprehensions? dictionaries? f-strings? slicing?).

### Friday (60 min): the explain-out-loud test
Record yourself (phone voice memo) explaining each concept for 2 minutes, as if to a smart friend who isn't technical. Then compare against the "passing answer" hint. Grade yourself: clear / fuzzy / blank.
- [ ] **Overfitting** — *passing answer mentions:* model memorizes training data, does great on training data and badly on new data; fix with more data, simpler model, regularization, or stopping earlier.
- [ ] **Train / validation / test split** — *mentions:* train to fit, validation to choose settings, test touched exactly once at the end to estimate real-world performance.
- [ ] **Gradient descent** — *mentions:* a loss function measures how wrong the model is; take small steps in the direction that reduces the loss; the learning rate is the step size.
- [ ] **Precision vs. recall** — *mentions:* precision = of the things I flagged, how many were right; recall = of the things I should have flagged, how many did I catch; the trade-off between them.
- [ ] **Matrix multiplication** — *mentions:* rows times columns, shapes must line up (m×n times n×p gives m×p), and it's how a layer of a neural network transforms its input.

### Saturday (4–5 h): data and ML diagnostic
- [ ] Create a project with uv and install the data tools:
  ```bash
  cd ~/code/ai-engineer-roadmap
  mkdir week1-diagnostic && cd week1-diagnostic
  uv init
  uv add pandas seaborn matplotlib scikit-learn jupyterlab
  uv run jupyter lab
  ```
  Add a line `.venv/` to the repo's `.gitignore` file (create the file if it doesn't exist) so the installed packages never get committed.
- [ ] In a new notebook, using the built-in penguins dataset (`import seaborn as sns; df = sns.load_dataset("penguins")`):
  - Look at the data (`df.head()`, `df.info()`, `df.describe()`)
  - Handle the missing values (decide: drop or fill, and say why in a markdown cell)
  - Make 3 plots: one distribution, one relationship between two numeric columns, one grouped comparison
  - Fit a linear regression with scikit-learn predicting body mass from flipper length; report the R² on a held-out test set
  - Write 5 sentences of conclusions in a markdown cell
- [ ] **Time yourself.** Write down how long it took and which parts you had to look up. (A fluent person does this in ~45 minutes. Two to three hours is normal for rusty. Longer is fine — it just means Phase 1 goes at full length.)
- [ ] Commit and push the notebook.
- [ ] Then start NeetCode's free **Data Structures & Algorithms for Beginners** course, first section (Arrays) → https://neetcode.io/courses — just watch and gauge how much is familiar (~45 min).

### Sunday (2–3 h): write the diagnostic, set up Exercism
- [ ] Create `diagnostic.md` in your repo with three lists: **Came back easily**, **Fuzzy**, **Gone**. Cover: Python syntax, algorithm problems, pandas, plotting, scikit-learn, the five ML concepts, git.
- [ ] Based on it, mark Phase 1 items you can skip (mostly in Weeks 3–4). Be conservative: when in doubt, don't skip.
- [ ] Set up the Exercism Python track and install its CLI → https://exercism.org/tracks/python — do the "Hello, World!" exercise to confirm everything works.
- [ ] Sunday ritual: `log.md` entry, check boxes, commit `Week 1 done`.

**Week 1 done when:** the repo exists with this README, the diagnostic notebook, and `diagnostic.md`, all pushed; Exercism works locally.

## Week 2 — Mon Sept 21 to Sun Sept 27: Warm-up (~14 h)

Now you know where you stand. This week rebuilds the basic tools you'll use every day for a year.

### Weekday mornings
- [ ] **Mon:** Exercism — 3 exercises (the track starts with basics: numbers, strings, conditionals). Read the community solutions after you submit; that's where the learning is.
- [ ] **Tue:** MIT Missing Semester, Lecture 1: *Course overview + the shell* (video ~50 min + do the exercises) → https://missing.csail.mit.edu/2020/course-shell/
- [ ] **Wed:** Pro Git, Chapter 2: *Git Basics* (~45 min) → https://git-scm.com/book/en/v2/Git-Basics-Getting-a-Git-Repository — practice `git log`, `git diff`, and undoing a change on your own repo. Then 20 min of the game **Oh My Git!** → https://ohmygit.org/
- [ ] **Thu:** NeetCode DSA for Beginners — *Dynamic Arrays* and *Stacks* sections; then solve Valid Parentheses → https://leetcode.com/problems/valid-parentheses/
- [ ] **Fri:** 3Blue1Brown, *Essence of Linear Algebra*, chapters 1–4 (vectors, linear combinations, linear transformations, matrix multiplication; ~45 min) → https://www.3blue1brown.com/topics/linear-algebra

### Weekend block A (4–5 h): Python back to fluent
- [ ] Official Python tutorial, sections 4–5 (control flow, data structures; ~1.5 h, type the examples) → https://docs.python.org/3/tutorial/controlflow.html
- [ ] Exercism — 3 more exercises
- [ ] Set up the *Hands-On Machine Learning* notebooks: clone https://github.com/ageron/handson-ml3 and run the Chapter 1 notebook. Read Chapter 1 (*The Machine Learning Landscape*) if you have the book; if not, the notebook plus Kaggle's free **Intro to Machine Learning** course covers the same ground → https://www.kaggle.com/learn/intro-to-machine-learning

### Weekend block B (2–3 h)
- [ ] Kaggle Learn **Pandas** mini-course, first half → https://www.kaggle.com/learn/pandas
- [ ] Solve Group Anagrams (20-minute cap, then study the NeetCode video solution) → https://leetcode.com/problems/group-anagrams/
- [ ] Sunday ritual. Commit `Week 2 done`.

**Phase 0 done when:**
- [ ] `diagnostic.md` exists and you've used it to mark skips in Phase 1
- [ ] You can clone, edit, commit, and push without looking anything up
- [ ] You've solved 7 easy problems (5 diagnostic + Valid Parentheses + Group Anagrams) and know your 20-minute stall points
- [ ] Your weekly schedule has held for two consecutive weeks. **This is the real milestone.**

---

# Phase 1 — Weeks 3–14: Foundations
**Mon Sept 28 – Sun Dec 20, 2026 (12 weeks, ~15 h/week)**

Goal: fluent Python, working knowledge of data structures & algorithms, solid classical machine learning, basic engineering hygiene, and one real project on GitHub.

## Recurring every week in Phase 1

| Item | Time | Notes |
|---|---|---|
| Exercism Python | 5 × 20 min | One exercise per weekday morning as a warm-up, before the main item. Stop when the track feels easy (probably ~Week 8). |
| NeetCode 150 problems | 3 h | 3–4 problems/week, in roadmap order → https://neetcode.io/roadmap. 25-min cap, then watch NeetCode's video solution, then **re-solve from scratch** without looking. Problems marked *(hard, optional)* only if you have time. |
| Machine learning | 5 h | *Hands-On Machine Learning* (Géron, 3rd ed.), Part I, one chapter/week, coding along in the notebooks → https://github.com/ageron/handson-ml3. Free alternative with the same coverage: *An Introduction to Statistical Learning with Python* (free PDF) → https://www.statlearning.com/. Prefer video? Andrew Ng's ML Specialization (audit free) → https://www.coursera.org/specializations/machine-learning-introduction |
| Math / engineering | 2 h | Rotates by week, below. |
| Project 1 (from Week 10) | 4–6 h | Weekend block A. Spec is in the *Project specs* section. |
| At work | 0 | Write your own SQL. |

**Problem-solving method (use every time):** read the problem twice → say the brute-force approach out loud → name the pattern (hash map? two pointers? stack?) → write the code → trace through one example by hand → only then run it. This is the interview method; practicing it now means it's automatic in Phase 4.

## Week 3 — Sept 28 to Oct 4
- [ ] Exercism ×5
- [ ] NeetCode (Arrays & Hashing): Top K Frequent Elements, Encode and Decode Strings (NeetCode has the free version), Product of Array Except Self
- [ ] NeetCode DSA for Beginners course: *Linked Lists* and *Recursion* sections
- [ ] Géron Ch. 2, *End-to-End Machine Learning Project*, first half (this is the most important chapter in the book; it's the whole workflow)
- [ ] 3Blue1Brown Linear Algebra, chapters 5–9 (determinant, inverse matrices, column space, nonsquare matrices, dot products)
- [ ] Missing Semester Lecture 2: *Shell Tools and Scripting* → https://missing.csail.mit.edu/2020/shell-tools/
- [ ] Sunday ritual

## Week 4 — Oct 5 to 11
- [ ] Exercism ×5
- [ ] NeetCode: Valid Sudoku, Longest Consecutive Sequence; (Two Pointers) Two Sum II
- [ ] Géron Ch. 2, second half — finish the full pipeline: split, explore, prepare, model, cross-validate, fine-tune, evaluate on test
- [ ] 3Blue1Brown Linear Algebra, chapters 10–16 (cross products, change of basis, eigenvectors, abstract vector spaces). You don't need to master eigenvectors; you need the picture.
- [ ] Kaggle Learn **Pandas**, second half → https://www.kaggle.com/learn/pandas
- [ ] Sunday ritual

## Week 5 — Oct 12 to 18
- [ ] Exercism ×5
- [ ] NeetCode: 3Sum, Container With Most Water; (Sliding Window) Longest Substring Without Repeating Characters
- [ ] Géron Ch. 3, *Classification* — precision, recall, F1, ROC curves, confusion matrices. Be able to explain when accuracy lies.
- [ ] 3Blue1Brown *Essence of Calculus*, chapters 1–6 → https://www.3blue1brown.com/topics/calculus
- [ ] Missing Semester Lecture 5: *Command-line Environment* → https://missing.csail.mit.edu/2020/command-line/
- [ ] Sunday ritual

## Week 6 — Oct 19 to 25
- [ ] Exercism ×5
- [ ] NeetCode: Longest Repeating Character Replacement, Permutation in String; Trapping Rain Water *(hard, optional)*
- [ ] Géron Ch. 4, *Training Models* — linear regression by gradient descent, learning rate, regularization (ridge, lasso), logistic regression. **This chapter is the bridge to deep learning.** Slow down here.
- [ ] 3Blue1Brown Calculus, chapters 7–12 (chain rule, implicit differentiation, limits, integrals, Taylor series). The chain rule is the one that matters most for you.
- [ ] Pro Git Ch. 3, *Branching* (~1 h) → https://git-scm.com/book/en/v2/Git-Branching-Branches-in-a-Nutshell — from now on, do project work on a branch and merge it.
- [ ] Sunday ritual

## Week 7 — Oct 26 to Nov 1
- [ ] Exercism ×5
- [ ] NeetCode: Minimum Window Substring *(hard, optional)*; (Stack) Min Stack, Evaluate Reverse Polish Notation, Generate Parentheses
- [ ] Géron Ch. 5 (*SVMs*, skim — know what a kernel is) and Ch. 6 (*Decision Trees*, read fully)
- [ ] Probability & statistics refresh: from *Learning Data Science* (the Data 100 textbook, free) → https://learningds.org/ — read the chapters on simulation/sampling and on summary statistics & loss functions. For anything that feels new, Khan Academy → https://www.khanacademy.org/math/statistics-probability
- [ ] Sunday ritual

## Week 8 — Nov 2 to 8
- [ ] Exercism ×5 (stop the daily Exercism after this week if it's easy; replace with a 4th NeetCode problem)
- [ ] NeetCode: Daily Temperatures, Car Fleet; (Binary Search) Binary Search, Search a 2D Matrix
- [ ] Géron Ch. 7, *Ensemble Learning and Random Forests* — random forests and gradient boosting are what wins on tabular data in industry. Know why.
- [ ] pytest getting started (~1 h) → https://docs.pytest.org/en/stable/getting-started.html — then write tests for two of your Exercism solutions, in a `tests/` folder, run with `uv run pytest`
- [ ] Sunday ritual

## Week 9 — Nov 9 to 15
- [ ] NeetCode: Koko Eating Bananas, Find Minimum in Rotated Sorted Array, Search in Rotated Sorted Array, Time Based Key-Value Store
- [ ] Géron Ch. 8 (*Dimensionality Reduction*, PCA) and Ch. 9 (*Unsupervised Learning*, k-means, clustering)
- [ ] FastAPI tutorial, first half (First Steps through Request Body; ~2 h) → https://fastapi.tiangolo.com/tutorial/ — build a toy API that returns a prediction from a hard-coded formula
- [ ] Sunday ritual

## Week 10 — Nov 16 to 22
- [ ] NeetCode: Median of Two Sorted Arrays *(hard, optional)*; (Linked List) Reverse Linked List, Merge Two Sorted Lists, Linked List Cycle
- [ ] FastAPI tutorial, second half (Query Parameters and String Validations through Handling Errors)
- [ ] **Project 1 kickoff (weekend block A):** choose your dataset (see *Project specs*), write `PLAN.md`: the question, the target variable, the metric and why, a baseline you must beat, and what "done" looks like. Create the repo `project-1-<name>` with a branch-based workflow.
- [ ] Sunday ritual

## Week 11 — Nov 23 to 29 (Thanksgiving week — deliberately light)
- [ ] NeetCode: Reorder List, Remove Nth Node From End of List
- [ ] Project 1: data loading and cleaning as a **script** (`src/data.py`), not just notebook cells. EDA notebook with 5+ plots and written observations.
- [ ] Sunday ritual

## Week 12 — Nov 30 to Dec 6
- [ ] NeetCode: Copy List with Random Pointer, Add Two Numbers, Find the Duplicate Number
- [ ] Project 1: baseline model + proper cross-validation + your chosen metric, in `src/train.py`. Then feature engineering and 2–3 model families (linear, random forest, gradient boosting). Record every result in a table in `RESULTS.md`.
- [ ] Sunday ritual

## Week 13 — Dec 7 to 13
- [ ] NeetCode: LRU Cache; Merge K Sorted Lists *(hard, optional)*; (Trees) Invert Binary Tree, Maximum Depth of Binary Tree
- [ ] Project 1: pick the final model, evaluate **once** on the held-out test set, save it (`joblib`), serve it from a FastAPI endpoint (`POST /predict`), write tests for the data pipeline and the endpoint.
- [ ] Sunday ritual

## Week 14 — Dec 14 to 20
- [ ] NeetCode: Diameter of Binary Tree, Balanced Binary Tree, Same Tree
- [ ] Project 1: README (see the README template in *Project specs*), clean the repo, pin dependencies (`uv lock`), final push. Ask Claude to **review** the repo as a hiring manager would and fix what it flags.
- [ ] Write `phase1-retro.md`: what you learned, what was harder than expected, what you'd do differently.
- [ ] Take the Phase 1 checkpoint below honestly.
- [ ] Sunday ritual. Commit `Phase 1 done`.

**Phase 1 done when:**
- [ ] ~43 NeetCode problems solved (including the diagnostic), and you can re-solve any Arrays/Hashing or Two-Pointer problem cold
- [ ] Project 1 is on GitHub with a working `/predict` endpoint, tests that pass, and a README with a results table
- [ ] You can explain out loud, clearly: bias vs. variance, why we cross-validate, what regularization does, why accuracy is the wrong metric for imbalanced classes, and why random forests beat a single tree
- [ ] You write SQL at work without AI first, and only use AI to review
- [ ] You've used a branch and merged it at least 5 times

---

# Phase 2 — Weeks 15–27: Depth
**Mon Dec 21, 2026 – Sun Mar 21, 2027 (13 weeks, ~15 h/week)**

Goal: understand neural networks from the inside by building them, then learn to build on top of large language models the way an engineer does — with evaluation, not vibes.

## Recurring every week in Phase 2

| Item | Time | Notes |
|---|---|---|
| NeetCode 150 | 3 h | 3/week: Trees → Tries → Heaps → Backtracking → start Graphs. Same method as Phase 1. |
| Karpathy, *Neural Networks: Zero to Hero* (Weeks 16–23) | 6–7 h | Course page → https://karpathy.ai/zero-to-hero.html · Playlist → https://www.youtube.com/playlist?list=PLAqhIrjkxbuWI23v9cThsA9GvCAUhRvKZ · Notebooks → https://github.com/karpathy/nn-zero-to-hero. **Rules:** pause the video, type every line yourself, run it, predict the output before you run it. Never copy-paste. Coding along takes 3–4× the video length. Each video = roughly one week. |
| Chip Huyen, *AI Engineering* (Weeks 17–26) | 2 h | One chapter/week → https://huyenchip.com/books/. It's a paid O'Reilly book (~$50, or read through an O'Reilly trial / your library). This is the textbook for your target role. |
| Project 2 (Weeks 22–27) | 5–6 h | Weekend block A. Spec in *Project specs*. |

**A note on hardware:** Karpathy's first six videos run fine on a laptop CPU. For *Let's build GPT* and beyond, use Google Colab's free GPU → https://colab.research.google.com/ (Runtime → Change runtime type → T4 GPU).

## Week 15 — Dec 21 to 27 (holiday week — light, intuition only)
- [ ] 3Blue1Brown *Neural Networks* series, chapters 1–4 (what a neural network is, gradient descent, backpropagation; ~1.5 h) → https://www.3blue1brown.com/topics/neural-networks
- [ ] 3Blue1Brown, chapters 5–7 of the same series (transformers, attention, MLPs in LLMs; ~1 h) — watch for the picture, not the math
- [ ] PyTorch *Learn the Basics* tutorial, first 4 pages (Tensors, Datasets, Transforms, Build Model; ~1.5 h) → https://pytorch.org/tutorials/beginner/basics/intro.html
- [ ] NeetCode: Subtree of Another Tree, Lowest Common Ancestor of a BST
- [ ] Sunday ritual

## Week 16 — Dec 28 to Jan 3
- [ ] **Karpathy 1: *The spelled-out intro to neural networks and backpropagation: building micrograd*** (2 h 25 m video; budget 7–8 h with coding). You build a tiny automatic-differentiation engine — the thing PyTorch does under the hood. If the chain rule was fuzzy in Week 6, this is where it clicks.
- [ ] Do the exercises he links in the video description.
- [ ] NeetCode: Binary Tree Level Order Traversal, Binary Tree Right Side View
- [ ] Sunday ritual

## Week 17 — Jan 4 to 10
- [ ] **Karpathy 2: *The spelled-out intro to language modeling: building makemore*** (1 h 57 m). Bigram model, torch.Tensor, negative log likelihood.
- [ ] Huyen Ch. 1, *Introduction to Building AI Applications with Foundation Models*
- [ ] NeetCode: Count Good Nodes in Binary Tree, Validate Binary Search Tree, Kth Smallest Element in a BST
- [ ] Sunday ritual

## Week 18 — Jan 11 to 17
- [ ] **Karpathy 3: *Building makemore Part 2: MLP*** (1 h 15 m). Embeddings, hidden layers, train/dev/test splits, learning-rate tuning, over/underfitting — every ML fundamental from Phase 1 shows up again, now inside a neural net.
- [ ] Huyen Ch. 2, *Understanding Foundation Models*
- [ ] NeetCode: Construct Binary Tree from Preorder and Inorder Traversal; (Tries) Implement Trie, Design Add and Search Words Data Structure
- [ ] Sunday ritual

## Week 19 — Jan 18 to 24
- [ ] **Karpathy 4: *Building makemore Part 3: Activations & Gradients, BatchNorm*** (1 h 55 m). Why deep nets are hard to train and the diagnostics engineers actually look at.
- [ ] Huyen Ch. 3, *Evaluation Methodology* — **read this one twice.** Evaluation is the skill that separates AI engineers from demo-builders.
- [ ] NeetCode: Binary Tree Maximum Path Sum *(hard, optional)*; (Heap) Kth Largest Element in a Stream, Last Stone Weight, K Closest Points to Origin
- [ ] Sunday ritual

## Week 20 — Jan 25 to 31
- [ ] **Karpathy 5: *Building makemore Part 4: Becoming a Backprop Ninja*** (1 h 55 m). Manual backpropagation through a whole network. Hard. Worth it. If you're behind schedule, watch it without coding along and move on.
- [ ] Huyen Ch. 4, *Evaluate AI Systems*
- [ ] NeetCode: Kth Largest Element in an Array, Task Scheduler, Design Twitter
- [ ] Sunday ritual

## Week 21 — Feb 1 to 7
- [ ] **Karpathy 6: *Building makemore Part 5: Building a WaveNet*** (56 m). Then **start Karpathy 7: *Let's build GPT: from scratch, in code, spelled out*** (1 h 56 m) — first half. Use Colab GPU.
- [ ] Huyen Ch. 5, *Prompt Engineering*
- [ ] NeetCode: Find Median from Data Stream *(hard, optional)*; (Backtracking) Subsets, Combination Sum
- [ ] Sunday ritual

## Week 22 — Feb 8 to 14
- [ ] **Finish Karpathy 7: *Let's build GPT*.** When your character-level GPT generates Shakespeare-ish text, take a screenshot. You have now built the architecture behind every model you use. Write a short `what-i-built.md` explaining, in your own words, what attention does.
- [ ] Huyen Ch. 6, *RAG and Agents* — the chapter your next two projects are built on.
- [ ] Hugging Face LLM Course, chapters 1–2 (Transformer models; using Transformers) → https://huggingface.co/learn/llm-course/en/chapter1/1
- [ ] **Project 2 kickoff (weekend block A):** choose your corpus (see *Project specs*). **Write 30 question-and-answer pairs by hand** before writing any code. This is your eval set. It's the most important artifact in the project.
- [ ] NeetCode: Permutations, Subsets II, Combination Sum II
- [ ] Sunday ritual

## Week 23 — Feb 15 to 21
- [ ] **Karpathy 8: *Let's build the GPT Tokenizer*** (2 h 13 m). Explains half the weird behaviors of LLMs.
- [ ] Huyen Ch. 7, *Finetuning* (read; you'll do it in Phase 3)
- [ ] Anthropic's prompt engineering interactive tutorial (in the courses repo) → https://github.com/anthropics/courses — and the API docs → https://docs.claude.com/en/api/overview. Get an API key on a **personal** account; set a spending limit ($10 is plenty for the month).
- [ ] Project 2: ingestion pipeline — load documents, chunk them, embed them (sentence-transformers → https://www.sbert.net/ or an API embedding model), store in Chroma → https://docs.trychroma.com/. Retrieve the top-k chunks for a question and print them. No LLM yet.
- [ ] NeetCode: Word Search, Palindrome Partitioning, Letter Combinations of a Phone Number
- [ ] Sunday ritual

## Week 24 — Feb 22 to 28
- [ ] Hamel Husain, *Your AI Product Needs Evals* → https://hamel.dev/blog/posts/evals/ and the *Evals FAQ* → https://hamel.dev/blog/posts/evals-faq/. Take notes on: unit-test-style assertions, LLM-as-judge, and looking at your data.
- [ ] Huyen Ch. 8, *Dataset Engineering* (skim)
- [ ] Project 2: add generation (retrieved chunks + question → LLM → answer with citations). Build the eval harness: for each of your 30 questions, measure (a) **retrieval hit rate** — did the right chunk appear in the top-k? and (b) **answer correctness** via an LLM-as-judge prompt comparing to your reference answer. Save results to a CSV. **Look at every failure by hand.**
- [ ] NeetCode: N-Queens *(hard, optional)*; (Graphs) Number of Islands, Clone Graph
- [ ] Sunday ritual

## Week 25 — Mar 1 to 7
- [ ] Anthropic, *Building Effective Agents* → https://www.anthropic.com/engineering/building-effective-agents — the reference for Project 3's design. Also read *Writing effective tools for agents* → https://www.anthropic.com/engineering/writing-tools-for-agents
- [ ] Huyen Ch. 9, *Inference Optimization* (skim; know what latency, throughput, and caching mean here)
- [ ] Project 2: iterate. Change one thing at a time (chunk size, overlap, top-k, a reranker, the prompt), re-run the eval, log the numbers in `RESULTS.md`. Add cost and latency logging per query. This loop — change, measure, keep or revert — is the core skill of the job.
- [ ] NeetCode: Max Area of Island, Pacific Atlantic Water Flow, Surrounded Regions
- [ ] Sunday ritual

## Week 26 — Mar 8 to 14
- [ ] Huyen Ch. 10, *AI Engineering Architecture and User Feedback*
- [ ] Project 2: build a simple UI with Gradio → https://www.gradio.app/guides/quickstart and deploy it free on Hugging Face Spaces → https://huggingface.co/spaces. Add an "Evals" tab that shows your results table. Write the README (template in *Project specs*).
- [ ] NeetCode: Rotting Oranges, Walls and Gates (free on NeetCode), Course Schedule
- [ ] Sunday ritual

## Week 27 — Mar 15 to 21
- [ ] Project 2 polish: tests for the chunker and the eval harness; `uv lock`; final README with the before/after eval table. Ask Claude to review it as a hiring manager.
- [ ] **Blog post #1** (600–1000 words): "I built a RAG system and measured it." What you built, what broke, what the numbers were before and after each change. Publish on a free GitHub Pages blog (→ https://pages.github.com/) and cross-post to LinkedIn. Writing about it is worth more than one extra feature.
- [ ] Optional if ahead: **Karpathy 9: *Let's reproduce GPT-2 (124M)*** (4 h)
- [ ] NeetCode: Course Schedule II, Graph Valid Tree (free on NeetCode), Number of Connected Components (free on NeetCode)
- [ ] Write `phase2-retro.md`. Take the checkpoint.
- [ ] Sunday ritual. Commit `Phase 2 done`.

**Phase 2 done when:**
- [ ] You have trained a GPT from scratch and can explain attention, embeddings, and why tokenization matters, out loud, without notes
- [ ] Project 2 is live on Hugging Face Spaces with an eval table showing at least 3 measured iterations
- [ ] ~80 NeetCode problems total; you can solve a new tree or backtracking problem in 30 minutes
- [ ] You've read *AI Engineering* and the Hamel evals post, and you can explain what an "eval" is to a non-technical friend
- [ ] Blog post #1 is published

---

# Phase 3 — Weeks 28–40: Portfolio and Visibility
**Mon Mar 22 – Sun Jun 20, 2027 (13 weeks, ~15 h/week)**

Goal: one project that looks like a real product, a public trail of writing and contributions, and people in the industry who know your name. **The AI rule flips this phase:** start using Claude Code and Cursor as power tools. You can now judge their output.

## Recurring every week in Phase 3

| Item | Time | Notes |
|---|---|---|
| NeetCode 150 | 3 h | 3/week: Advanced Graphs → 1-D DP → 2-D DP → Greedy → Intervals. Dynamic programming is where most people quit; don't. |
| Project 3 (capstone) | 8–9 h | Weekend block A + 2 mornings. Spec in *Project specs*. |
| Networking | 1–2 h | 2 coffee chats per month (video or in person), 20–30 min each. Tracker in `network.md`: who, when, what you learned, follow-up. |
| Open source | 1–2 h | Weeks 31–35. One merged pull request minimum. |
| Writing | — | Blog posts #2 and #3 in Weeks 34 and 38. |

**Set up your AI tools (Week 28, ~1 h):**
- Claude Code (terminal coding agent) → https://docs.claude.com/en/docs/claude-code/overview
- Cursor (AI-native editor) → https://cursor.com/
- How to use them well: describe the *what* and the *constraints*, review every diff before accepting, ask it to write tests first, and never merge code you couldn't have written yourself given time. You'll be asked in interviews how you use these tools. Have a real answer.

## Week 28 — Mar 22 to 28
- [ ] **Capstone design doc (`DESIGN.md`, 1 page):** problem, who it's for, architecture diagram (draw it in Excalidraw → https://excalidraw.com/), the eval plan, what "v1" includes and excludes. Choose agent or fine-tune (see *Project specs*).
- [ ] Create repo `project-3-<name>` **with CI on day one**: GitHub Actions running `pytest` on every push → https://docs.github.com/en/actions/quickstart. A `Dockerfile` that runs the app → https://docs.docker.com/get-started/
- [ ] Set up Claude Code and/or Cursor (above)
- [ ] NeetCode: Redundant Connection, Word Ladder *(hard, optional)*; (Advanced Graphs) Network Delay Time
- [ ] Sunday ritual

## Week 29 — Mar 29 to Apr 4
- [ ] Capstone: end-to-end skeleton working, ugly. Input → core logic → output, deployed nowhere yet.
- [ ] **Message the friends at DeepMind.** Template: "Hey — I've spent the last six months rebuilding my engineering skills and I'm aiming for AI engineer roles by the fall. I'd love 20 minutes to hear how you got in and what the interview process was like. Here's what I've built so far: [GitHub link]." Ask specifically: what did the interviews test, what would they do in your position, who else should you talk to.
- [ ] NeetCode: Min Cost to Connect All Points, Cheapest Flights Within K Stops; Swim in Rising Water *(hard, optional)*
- [ ] Sunday ritual

## Week 30 — Apr 5 to 11
- [ ] Capstone: persistence (SQLite or Postgres via SQLAlchemy → https://docs.sqlalchemy.org/en/20/tutorial/) and the first 30-case eval set, written by hand.
- [ ] LinkedIn rewrite: headline "Software engineer building AI systems | Python, PyTorch, LLM evals | ex-analyst" (or honest equivalent), About section that leads with what you've built, Featured section with your three repos and blog post.
- [ ] Coffee chat #1
- [ ] NeetCode (1-D DP): Climbing Stairs, Min Cost Climbing Stairs, House Robber
- [ ] Sunday ritual

## Week 31 — Apr 12 to 18
- [ ] Capstone: eval-driven iteration #1 — run the eval set, read every failure, fix the biggest category, re-run, log in `RESULTS.md`.
- [ ] **Open source, step 1:** pick one library you used in Projects 2–3 (Chroma, Gradio, sentence-transformers, a small eval or agent library). Read its `CONTRIBUTING.md`. Find one issue labelled `good first issue` or one documentation page with an error or gap. Comment on the issue saying you'd like to take it.
- [ ] NeetCode: House Robber II, Longest Palindromic Substring, Palindromic Substrings
- [ ] Sunday ritual

## Week 32 — Apr 19 to 25
- [ ] Capstone: deploy v1 — Docker image → Render (→ https://render.com/) or Fly.io (→ https://fly.io/). Free/hobby tiers are enough. Public URL in the README.
- [ ] Coffee chat #2. Also: find your Berkeley alumni on LinkedIn (school page → Alumni tab → filter by "AI" or "machine learning" and company). Message 3 with a specific, short ask.
- [ ] NeetCode: Decode Ways, Coin Change, Maximum Product Subarray
- [ ] Sunday ritual

## Week 33 — Apr 26 to May 2
- [ ] Capstone: observability — structured logging of every model call (inputs, outputs, tokens, cost, latency) to your database; a `/metrics` or admin page that shows them.
- [ ] **Open source, step 2:** submit your first pull request (docs fix or small bug). Follow their PR template exactly. Respond to review comments within a day.
- [ ] NeetCode: Word Break, Longest Increasing Subsequence, Partition Equal Subset Sum
- [ ] Sunday ritual

## Week 34 — May 3 to 9
- [ ] **Blog post #2:** the capstone so far — the design decision you got wrong and how the evals showed it.
- [ ] Register for a hackathon in the next 6 weeks. Find one: Devpost → https://devpost.com/hackathons, Major League Hacking → https://mlh.io/seasons/2027/events, or local AI meetups on Luma → https://lu.ma/ and Meetup → https://www.meetup.com/. Hackathons are underrated: a project, teammates, and recruiters in one weekend.
- [ ] **Resume v1.** One page. Bullets in the form "Did X, measured by Y, by doing Z." Your analyst job goes on it truthfully in engineering language: the SQL, the data pipelines, the stakeholder requirements, the reporting systems — whatever you actually did. Projects section with the three repos, each with one metric.
- [ ] NeetCode (2-D DP): Unique Paths, Longest Common Subsequence, Best Time to Buy and Sell Stock with Cooldown
- [ ] Sunday ritual

## Week 35 — May 10 to 16
- [ ] Capstone: polish the UI; write the README with architecture diagram, eval results table, and a 60-second demo GIF (record with your OS screen recorder, convert with https://ezgif.com/)
- [ ] **Open source, step 3:** second PR — a real bug fix this time, with a test.
- [ ] Coffee chat #3
- [ ] NeetCode: Coin Change II, Target Sum, Interleaving String
- [ ] Sunday ritual

## Week 36 — May 17 to 23
- [ ] Hackathon weekend (if scheduled), or a capstone feature you cut from v1
- [ ] Coffee chat #4
- [ ] NeetCode: Edit Distance; Longest Increasing Path in a Matrix *(hard, optional)*; Distinct Subsequences *(hard, optional)*
- [ ] Sunday ritual

## Week 37 — May 24 to 30
- [ ] **Portfolio page:** a GitHub profile README (→ https://docs.github.com/en/account-and-profile/setting-up-and-managing-your-github-profile/customizing-your-profile/managing-your-profile-readme) linking your three projects, blog, and LinkedIn. Optionally a one-page site on GitHub Pages.
- [ ] Resume v2 — get feedback from two people (a friend in the industry and Claude, prompted as a skeptical hiring manager for AI engineer roles). Fix it.
- [ ] NeetCode (Greedy): Maximum Subarray, Jump Game, Jump Game II; Burst Balloons *(hard, optional)*
- [ ] Sunday ritual

## Week 38 — May 31 to Jun 6
- [ ] **Calibration applications: send 10.** Startups and mid-size companies only, roles titled AI Engineer, Applied AI Engineer, LLM Engineer, Software Engineer (AI/ML), Forward Deployed Engineer. Sources: Wellfound → https://wellfound.com/, YC's Work at a Startup → https://www.workatastartup.com/, LinkedIn. Track every one in a spreadsheet (company, role, date, source, referral?, status, notes). The goal is to see what happens, not to get hired yet.
- [ ] **Blog post #3:** the open-source contribution or the hackathon.
- [ ] NeetCode: Gas Station, Hand of Straights, Merge Triplets to Form Target Triplet
- [ ] Sunday ritual

## Week 39 — Jun 7 to 13
- [ ] **Behavioral story bank:** write 8 stories in STAR format (Situation, Task, Action, Result), 6–8 sentences each, from your analyst job and your projects: a conflict with a stakeholder, a failure and what you changed, a time you influenced without authority, a time you handled ambiguity, a time you had to learn something fast, a time you pushed back, a time you delivered under pressure, your proudest technical decision. Save as `stories.md` (private repo).
- [ ] Coffee chats #5 and #6
- [ ] NeetCode: Partition Labels, Valid Parenthesis String; (Intervals) Insert Interval
- [ ] Sunday ritual

## Week 40 — Jun 14 to 20
- [ ] Capstone final: everything merged, CI green, deployed, README complete. Freeze it. (You can keep adding later; from here on the time goes to interviews.)
- [ ] Review the 10 calibration applications: any responses? Any patterns in the rejections? Adjust resume/positioning.
- [ ] NeetCode: Merge Intervals, Non-overlapping Intervals, Meeting Rooms (free on NeetCode)
- [ ] Write `phase3-retro.md`. Take the checkpoint.
- [ ] Sunday ritual. Commit `Phase 3 done`.

**Phase 3 done when:**
- [ ] Capstone is deployed with CI, Docker, a database, logging, and an eval table showing iterations
- [ ] 3 blog posts published; GitHub profile README and LinkedIn are done
- [ ] At least 1 merged pull request in a real open-source project
- [ ] ~115 NeetCode problems total (more if you did the optional hards)
- [ ] 6+ coffee chats logged in `network.md`; you've asked at least 2 people if they'd refer you when the time comes
- [ ] 10 applications sent and tracked
- [ ] 8 STAR stories written

---

# Phase 4 — Weeks 41–52: Interview Mode
**Mon Jun 21 – Sun Sep 12, 2027 (12 weeks, ~15 h/week)**

Goal: convert. The building is done; now you practice performing it under pressure, and you run a real job search like a project.

## Recurring every week in Phase 4

| Item | Time | Notes |
|---|---|---|
| Coding practice | 5 h | Weeks 41–42: finish the scheduled list. From Week 43: **one timed problem every day** (LeetCode medium, 30-minute timer, talk out loud the whole time, no IDE autocomplete). Redo problems you failed 2 weeks later. |
| System / ML design | 3 h | See resources below. Practice on a whiteboard or Excalidraw, out loud, 45 minutes per problem. |
| Behavioral | 1 h | Rehearse 2 STAR stories per week out loud; tighten to 2 minutes each. |
| Applications + referrals | 3–4 h | 10–15 applications/week, referral-first. Every application to a company where you know someone starts with a message to that person. |
| Mock interviews | 1–2 h | 5 minimum across the phase: 2 coding, 2 design, 1 behavioral. Friends from your coffee chats, or interviewing.io → https://interviewing.io/ (has free peer practice). Record and re-watch. |

**Design resources:**
- *Machine Learning System Design Interview* (Ali Aminian & Alex Xu) → https://bytebytego.com/ — the standard prep book; work through the problems as if you're in the room
- *Designing Machine Learning Systems* (Chip Huyen), Chapters 1–2 and 6–9 → https://huyenchip.com/books/
- Chip Huyen's free *Machine Learning Interviews Book* → https://huyenchip.com/ml-interviews-book/ — read the "Questions" chapters
- Your own Projects 2 and 3. The best design answers are "here's how I actually did it, and here's what I'd change at 100× scale."

**Where to apply:**
- Startups: Wellfound → https://wellfound.com/, Work at a Startup → https://www.workatastartup.com/, YC jobs → https://www.ycombinator.com/jobs
- Mid-size AI-forward companies: LinkedIn Jobs with alerts for "AI Engineer", "Applied AI", "LLM Engineer", "Forward Deployed Engineer", "Software Engineer, AI"
- Big tech: **only via referral.** Cold applications to big tech at this stage are a lottery ticket; a referral is a real chance.
- Adjacent titles worth applying to: Analytics Engineer, Data Engineer, Solutions Engineer (AI), Forward Deployed Engineer. A step job in the right direction counts.
- Internal: if your current company opens data engineering, analytics engineering, or AI/automation roles, apply. Life sciences companies are building these teams and you already understand the environment.

## Week 41 — Jun 21 to 27
- [ ] NeetCode: Meeting Rooms II (free on NeetCode), Minimum Interval to Include Each Query *(hard, optional)*; (Math & Geometry) Rotate Image, Spiral Matrix, Set Matrix Zeroes, Happy Number, Plus One
- [ ] Aminian & Xu, Introduction + Chapters 1–2. Practice problem: *design a system that recommends products* — 45 min, out loud.
- [ ] Application tracker set up (spreadsheet). Send the referral asks you set up in Phase 3: "The time has come — would you be willing to refer me for [specific role + link]?"
- [ ] Applications: 10
- [ ] Sunday ritual

## Week 42 — Jun 28 to Jul 4
- [ ] NeetCode: Pow(x, n), Multiply Strings, Detect Squares; (Bit Manipulation) Single Number, Number of 1 Bits, Counting Bits, Reverse Bits, Missing Number, Sum of Two Integers, Reverse Integer. **That's every non-hard problem on the list. Screenshot the roadmap.**
- [ ] The hards you haven't done become your timed problems for Weeks 43–47, one or two per week mixed in with the mediums: Sliding Window Maximum, Largest Rectangle in Histogram, Reverse Nodes in K-Group, Serialize and Deserialize Binary Tree, Word Search II, Reconstruct Itinerary, Alien Dictionary, Regular Expression Matching, plus any *(hard, optional)* you skipped earlier. Finishing those is what makes it 150/150.
- [ ] Aminian & Xu, Chapters 3–4
- [ ] Applications: 10
- [ ] Sunday ritual

## Week 43 — Jul 5 to 11
- [ ] Daily timed mediums begin (6 this week). Start a `weak-spots.md`: which patterns you miss under time.
- [ ] Design practice: **a RAG system for a company's internal docs** — ingestion, retrieval, generation, evaluation, permissions, cost at 10k queries/day. Use Project 2 as the base.
- [ ] Mock interview #1 (coding)
- [ ] Applications: 10–15
- [ ] Sunday ritual

## Week 44 — Jul 12 to 18
- [ ] Daily timed mediums (6)
- [ ] Design practice: **an evaluation pipeline for an LLM feature** — offline evals, LLM-as-judge calibration against human labels, online A/B tests, regression gates in CI.
- [ ] Mock interview #2 (behavioral) — 2-minute answers, then the "tell me more" follow-ups
- [ ] Applications: 10–15
- [ ] Sunday ritual

## Week 45 — Jul 19 to 25
- [ ] Daily timed mediums (6)
- [ ] Design practice: **an agent with tools for customer support** — tool design, guardrails, human handoff, failure modes, what you log. Use Anthropic's *Building Effective Agents* as your vocabulary.
- [ ] Mock interview #3 (coding)
- [ ] Applications: 10–15
- [ ] Sunday ritual

## Week 46 — Jul 26 to Aug 1
- [ ] Daily timed mediums (6)
- [ ] Design practice: **fraud detection or recommendation system** (classic ML design) — features, training data, offline metrics, serving, monitoring, retraining
- [ ] Huyen DMLS Chapters 6–9 (model development, deployment, monitoring, infrastructure)
- [ ] Mock interview #4 (design)
- [ ] Applications: 10–15
- [ ] Sunday ritual

## Week 47 — Aug 2 to 8
- [ ] Redo every problem in `weak-spots.md`
- [ ] Design practice: **LLM cost and latency optimization** — caching, model routing (small model first), batching, streaming, prompt compression, when to fine-tune vs. prompt
- [ ] Take-home practice: give yourself 4 hours to build a small LLM app from a one-paragraph spec, with tests and a README. Take-homes are common for AI engineer roles.
- [ ] Mock interview #5
- [ ] Applications: 10–15
- [ ] Sunday ritual

## Weeks 48–52 — Aug 9 to Sep 12
- [ ] Daily timed problem continues (never stop until you sign)
- [ ] Interview loops: after every real interview, write down every question within an hour, in `interviews.md`. Patterns will appear by the third loop.
- [ ] Keep applying at 10/week until you have a signed offer. Pipelines dry up faster than they fill.
- [ ] When an offer comes: compensation data at Levels.fyi → https://www.levels.fyi/. Ask for a few days. Negotiate once, politely, with a number.
- [ ] Write `phase4-retro.md` and the final `log.md` entry, whatever the outcome.

**Phase 4 done when:**
- [ ] 150/150 NeetCode plus 40+ timed mediums
- [ ] 5+ mock interviews, 5+ design problems practiced out loud
- [ ] 80+ applications tracked, at least 15 via referral
- [ ] An offer you'd take — or, if not yet, a pipeline of active loops and a portfolio that makes month 13 a continuation, not a restart

---

# Project specs

Three projects, increasing in scope. Each one should look like something an engineer shipped, not a homework notebook. The rule for choosing a dataset or domain: **pick something you find interesting**, because you'll spend 40–100 hours with it. Sports, music, games, movies, finance, housing, transit, your own hobby — anything with public data.

## What every project repo must have (the hiring-manager checklist)
- [ ] A README that opens with **one sentence** on what it does and one screenshot or GIF
- [ ] A "Results" section with a **table of numbers** (metric before/after, or eval scores per iteration)
- [ ] A "How to run it" section that works in 3 commands from a fresh clone
- [ ] Code in a `src/` folder as modules, not just notebooks (notebooks are fine for exploration, in `notebooks/`)
- [ ] Tests in `tests/` that pass with `uv run pytest`
- [ ] Pinned dependencies (`pyproject.toml` + `uv.lock`)
- [ ] A short "What I'd do next" section — shows judgment
- [ ] No secrets committed (API keys go in `.env`, which is in `.gitignore`)

## Project 1 (Phase 1, Weeks 10–14): End-to-end classical ML, served as an API

**What:** take a messy public tabular dataset, predict something, serve the prediction.

**Dataset options** (pick one, or anything you care more about):
- Inside Airbnb — listings for any city; predict nightly price → https://insideairbnb.com/get-the-data/
- Lending Club loan data (on Kaggle) — predict default; a real imbalanced-class problem
- Spotify tracks datasets (on Kaggle) — predict popularity or genre
- NYC Yellow Taxi trips — predict trip duration or tip → https://www.nyc.gov/site/tlc/about/tlc-trip-record-data.page
- Browse: Kaggle Datasets → https://www.kaggle.com/datasets · UCI ML Repository → https://archive.ics.uci.edu/ · Hugging Face Datasets → https://huggingface.co/datasets

**Must include:** a `PLAN.md` written before coding; data cleaning as a script; EDA notebook with written observations; a baseline (predict the mean/majority class) that you beat; k-fold cross-validation; the right metric for the problem (and a sentence on why); at least 3 model families compared in a table; the test set touched exactly once; the model saved and served from a FastAPI `POST /predict` endpoint; tests for the pipeline and the endpoint.

**Stretch:** a Dockerfile; a `GET /health` endpoint; input validation with Pydantic (FastAPI does this for you).

## Project 2 (Phase 2, Weeks 22–27): RAG system with real evaluation

**What:** a question-answering system over a document collection, with a measured evaluation loop. This is the canonical AI engineer project — and the eval is what separates yours from the thousand "chat with your PDF" clones.

**Corpus options** (public, text-heavy, something you'd actually ask questions about):
- The documentation of a library you use (FastAPI, pandas, PyTorch — they're all open source)
- A Wikipedia subset on a topic you love (a sport, a historical period, a game franchise)
- Paul Graham's essays (a classic RAG corpus) → https://www.paulgraham.com/articles.html
- Public government documents on a topic you care about (tax publications, transit reports)
- Open textbooks (e.g., *Learning Data Science* itself)

**Must include:** 30+ hand-written question/answer pairs **before** any code; a chunking + embedding + vector-store ingestion pipeline (Chroma is the simplest start); retrieval with top-k; generation with citations to the source chunks; an eval harness that measures retrieval hit rate and answer correctness (LLM-as-judge against your reference answers); per-query cost and latency logging; at least 3 logged iterations where you changed one thing and re-measured; a Gradio UI deployed on Hugging Face Spaces with an Evals tab.

**Stretch:** a reranker; hybrid search (keyword + vector); a "no answer found" path with its own eval.

## Project 3 (Phase 3, Weeks 28–40): Capstone — pick one

**Option A: an agent with tools that does something useful end to end.** Examples: a research assistant that searches, reads, and writes a cited briefing; a personal finance categorizer that reads CSV exports and answers questions; a job-application tracker that reads postings, drafts tailored notes, and tracks status (yes, you can use it in Phase 4); a coding assistant that runs your tests and proposes fixes. Design it with the patterns in Anthropic's *Building Effective Agents*: start with the simplest workflow that works, add autonomy only where it earns its keep.

**Option B: fine-tune a small open model for a specific task and prove it beat the base model.** Pick a task (classification, extraction, a house style), build a dataset (hundreds to low thousands of examples), fine-tune a 1–3B-parameter open model with LoRA using Hugging Face TRL → https://huggingface.co/docs/trl and PEFT → https://huggingface.co/docs/peft (the free *smol course* walks through exactly this → https://huggingface.co/learn/smol-course/unit0/1), and evaluate base vs. fine-tuned vs. a prompted frontier model on a held-out set. The comparison table is the deliverable.

**Both options must include:** `DESIGN.md` with an architecture diagram; GitHub Actions CI running tests on every push; a Dockerfile; a database (SQLite is fine); structured logging of every model call (tokens, cost, latency); a hand-built eval set of 30+ cases with at least 3 measured iterations in `RESULTS.md`; deployed with a public URL (Render / Fly.io / Hugging Face Spaces); a demo GIF in the README.

---

# What to do at work (on company time, compliantly)

You have 40 hours a week in a data environment. Used well, it's free practice. Used carelessly, it's a compliance problem. The line:

**Do:**
- Write every SQL query yourself first. Then paste it into your approved AI tool and ask it to review, not rewrite. Within a month you'll be fluent again.
- Learn your company's data stack deeply: how the warehouse is modeled, how the BI tool queries it, where the pipelines live. Ask the data engineers to walk you through one pipeline.
- Volunteer for automation or analytics-engineering work through proper channels. Understanding how a regulated data environment works (validation, audit trails, access control) is an asset on your resume when described appropriately.
- Practice SQL on public problems in personal time: LeetCode SQL 50 → https://leetcode.com/studyplan/top-sql-50/ · DataLemur → https://datalemur.com/ · Mode's SQL tutorial → https://mode.com/sql-tutorial/
- If internal data/AI/engineering roles open up, apply. You're already inside.

**Don't:**
- Move any company data, queries, documents, schemas, or screenshots to personal devices, personal accounts, or personal AI tools. Not even "anonymized." Not even "just the structure."
- Build personal projects on company data or company systems.
- Use work AI tools for personal-project code, or personal AI tools for work.

Your resume will say what you did at work in truthful, engineering-flavored language. It won't say anything about the data itself.

---

# How to use Claude (and other AI) while learning

**Phases 0–2 (tutor mode).** Prompts that work:

- *Explain:* "Explain [concept] to someone who studied it at Berkeley four years ago and forgot it. Assume I've seen it before. Use one concrete example and stop."
- *Quiz:* "Quiz me on [topic] — 5 questions, one at a time. Don't tell me the answer until I've attempted it. Then tell me what my answer revealed about my understanding."
- *Review, don't fix:* "Here's my code for [problem]. Do not rewrite it. Tell me what's wrong or could be better, and ask me one question that would lead me to the fix."
- *Complexity check:* "Here's my solution. What's the time and space complexity, and is there a well-known better approach? Name the pattern; don't write the code."
- *Rubber duck:* "I'm stuck on [problem]. Here's my thinking so far: [...]. Ask me questions to help me find the gap. Don't give hints unless I ask."
- *Explain-back check:* "I'm going to explain [concept] in my own words. Tell me what I got wrong or left out: [your explanation]."

**Phase 3 onward (power-tool mode).** Use Claude Code / Cursor to scaffold, write tests, refactor, and debug — but review every diff, ask *why* when you don't follow, and keep the rule: never merge code you couldn't have written yourself given time. Being fast *and* able to judge the output is exactly what employers are hiring for.

**All phases:** never paste work data or work code into any AI tool that isn't approved by your employer.

---

# If you fall behind

You will, at some point. The plan shrinks; it doesn't stop.

**Priority order (cut from the bottom):**
1. The weekly habit itself (even 5 hours in a bad week — keep the streak)
2. NeetCode problems (interviews don't care why you were busy)
3. Karpathy videos 1, 2, 3, 7 (micrograd, bigram, MLP, GPT) — the non-negotiable core
4. Project 2 with its eval harness
5. Project 1
6. Project 3 — scope it down before you cut it: v1 can be small
7. Blog posts, open source, hackathon
8. Karpathy 4, 5, 6, 8, 9 and the optional hard problems

**If you're 2+ weeks behind at a phase boundary:** move on anyway. Carry only the top-3 priority items forward. Don't try to "catch up" everything; that's how people quit.

**If you have a 25-hour week:** projects first, then extra problems, then optional videos. Never a new course.

**If you're doubting whether this is working (you will, around Weeks 6, 20, and 35):** re-read `diagnostic.md` from Week 1. Then look at your GitHub contribution graph. Then keep going.

---

# Costs

Nearly everything is free. Expect roughly **$150–250 for the year**:
- *Hands-On Machine Learning* (Géron) — ~$50, or free alternative ISLP
- *AI Engineering* (Huyen) — ~$50–60, or an O'Reilly trial / library
- *Machine Learning System Design Interview* (Aminian & Xu) — ~$40
- LLM API credits for Projects 2–3 — $20–50 total if you set spending limits
- Optional: Cursor Pro (~$20/month for a few months in Phase 3–4), a domain name
- **Not needed:** LeetCode Premium (NeetCode has the premium problems for free), paid bootcamps, certificates

---

# Master resource list

**Tools**
- VS Code → https://code.visualstudio.com/
- Git → https://git-scm.com/downloads · GitHub CLI → https://cli.github.com/
- uv (Python + packages) → https://docs.astral.sh/uv/
- Google Colab (free GPU notebooks) → https://colab.research.google.com/
- GitHub Codespaces → https://github.com/features/codespaces
- Excalidraw (diagrams) → https://excalidraw.com/

**Git / GitHub / command line**
- GitHub Skills: Introduction to GitHub → https://github.com/skills/introduction-to-github
- Pro Git (free book) → https://git-scm.com/book/en/v2
- Oh My Git! (game) → https://ohmygit.org/
- MIT Missing Semester → https://missing.csail.mit.edu/

**Python**
- Official tutorial → https://docs.python.org/3/tutorial/
- Exercism Python track → https://exercism.org/tracks/python
- *Python Crash Course* (Eric Matthes), if the diagnostic was rough → https://ehmatthes.github.io/pcc_3e/
- Kaggle Learn (Python, Pandas, Intro ML) → https://www.kaggle.com/learn

**Algorithms**
- NeetCode roadmap (the 150) → https://neetcode.io/roadmap
- NeetCode courses (DSA for Beginners) → https://neetcode.io/courses
- LeetCode → https://leetcode.com/
- *Grokking Algorithms* (Aditya Bhargava) — friendly illustrated book if DS&A feels alien → https://www.manning.com/books/grokking-algorithms-second-edition

**Math**
- 3Blue1Brown Linear Algebra → https://www.3blue1brown.com/topics/linear-algebra
- 3Blue1Brown Calculus → https://www.3blue1brown.com/topics/calculus
- 3Blue1Brown Neural Networks → https://www.3blue1brown.com/topics/neural-networks
- Khan Academy Statistics & Probability → https://www.khanacademy.org/math/statistics-probability
- *Learning Data Science* (Data 100 textbook, free) → https://learningds.org/

**Machine learning**
- *Hands-On Machine Learning* notebooks → https://github.com/ageron/handson-ml3
- *An Introduction to Statistical Learning* (free PDF) → https://www.statlearning.com/
- Andrew Ng, ML Specialization → https://www.coursera.org/specializations/machine-learning-introduction
- scikit-learn user guide → https://scikit-learn.org/stable/user_guide.html

**Deep learning**
- Karpathy, *Neural Networks: Zero to Hero* → https://karpathy.ai/zero-to-hero.html · playlist → https://www.youtube.com/playlist?list=PLAqhIrjkxbuWI23v9cThsA9GvCAUhRvKZ · notebooks → https://github.com/karpathy/nn-zero-to-hero
- Karpathy, *Deep Dive into LLMs like ChatGPT* → https://www.youtube.com/watch?v=7xTGNNLPyMI
- PyTorch tutorials → https://pytorch.org/tutorials/beginner/basics/intro.html
- Raschka, *Build a Large Language Model (From Scratch)* + code → https://github.com/rasbt/LLMs-from-scratch
- fast.ai *Practical Deep Learning for Coders* (optional alternative, top-down) → https://course.fast.ai/

**LLM / AI engineering**
- Chip Huyen, *AI Engineering* → https://huyenchip.com/books/
- Hugging Face LLM Course → https://huggingface.co/learn/llm-course/en/chapter1/1
- Hugging Face smol course (fine-tuning) → https://huggingface.co/learn/smol-course/unit0/1
- Hugging Face Agents Course → https://huggingface.co/learn/agents-course/unit0/introduction
- Maxime Labonne's LLM Course (a free, well-organized reading roadmap) → https://huggingface.co/blog/mlabonne/llm-course
- Anthropic, *Building Effective Agents* → https://www.anthropic.com/engineering/building-effective-agents
- Anthropic, *Writing effective tools for agents* → https://www.anthropic.com/engineering/writing-tools-for-agents
- Anthropic courses (prompt engineering, tool use) → https://github.com/anthropics/courses
- Claude API docs → https://docs.claude.com/en/api/overview
- Hamel Husain, *Your AI Product Needs Evals* → https://hamel.dev/blog/posts/evals/ · *Evals FAQ* → https://hamel.dev/blog/posts/evals-faq/
- sentence-transformers (embeddings) → https://www.sbert.net/
- Chroma (vector database) → https://docs.trychroma.com/
- Gradio → https://www.gradio.app/ · Hugging Face Spaces (free hosting) → https://huggingface.co/spaces
- Latent Space (podcast/newsletter for the AI engineer field) → https://www.latent.space/

**Engineering**
- FastAPI tutorial → https://fastapi.tiangolo.com/tutorial/
- pytest → https://docs.pytest.org/en/stable/getting-started.html
- Docker getting started → https://docs.docker.com/get-started/
- GitHub Actions quickstart → https://docs.github.com/en/actions/quickstart
- SQLAlchemy tutorial → https://docs.sqlalchemy.org/en/20/tutorial/
- Render → https://render.com/ · Fly.io → https://fly.io/
- Claude Code → https://docs.claude.com/en/docs/claude-code/overview · Cursor → https://cursor.com/

**SQL**
- LeetCode SQL 50 → https://leetcode.com/studyplan/top-sql-50/
- DataLemur → https://datalemur.com/
- Mode SQL tutorial → https://mode.com/sql-tutorial/

**Interviews and job search**
- *Machine Learning System Design Interview* (Aminian & Xu) → https://bytebytego.com/
- Chip Huyen, *Designing Machine Learning Systems* → https://huyenchip.com/books/ · free *ML Interviews Book* → https://huyenchip.com/ml-interviews-book/
- interviewing.io (mock interviews) → https://interviewing.io/
- Wellfound → https://wellfound.com/ · Work at a Startup → https://www.workatastartup.com/ · YC Jobs → https://www.ycombinator.com/jobs
- Devpost hackathons → https://devpost.com/hackathons · MLH → https://mlh.io/ · Luma → https://lu.ma/ · Meetup → https://www.meetup.com/
- Levels.fyi (compensation) → https://www.levels.fyi/
- GitHub Pages (free blog/portfolio) → https://pages.github.com/

---

# Glossary

Plain-English definitions of every term and acronym in this plan.

**Roles**
- **SWE (Software Engineer)** — builds software systems. Interviews focus on coding, algorithms, and system design.
- **MLE (Machine Learning Engineer)** — trains, deploys, and maintains machine learning models in production. At big companies often expects a master's/PhD or years of experience.
- **AI Engineer** — builds products on top of existing large models (like Claude or GPT): retrieval systems, agents, evaluation, fine-tuning, deployment. Newer role; values shipping ability over credentials. Your primary target.
- **Forward Deployed Engineer** — an engineer embedded with customers to build AI solutions on their problems. Common at AI startups; a good fit for someone with business-analyst experience.
- **Analytics Engineer / Data Engineer** — builds the data pipelines and models that analysts and ML use. Reasonable stepping-stone roles.

**Tools and workflow**
- **Git** — version control: tracks every change to your code so you can go back, branch, and collaborate. **GitHub** — the website where git repositories live and where employers look at your work.
- **Repo (repository)** — one project's folder tracked by git. **Commit** — a saved snapshot of changes with a message. **Push** — upload commits to GitHub. **Clone** — download a repo. **Branch** — a parallel line of work you later **merge** back. **PR (pull request)** — a proposed set of changes for someone to review and merge; how open-source contributions happen.
- **README** — the front page of a repo; explains what it is and how to run it.
- **CLI (command line interface) / terminal / shell** — typing commands instead of clicking. Engineers live here.
- **IDE / editor** — where you write code. VS Code is the standard.
- **uv** — a fast tool that installs Python and manages a project's packages. Replaces pip, venv, and conda for our purposes.
- **Virtual environment (venv)** — an isolated set of installed packages per project so they don't conflict. uv handles this.
- **Package / library** — reusable code someone else wrote (pandas, PyTorch). Installed with uv.
- **Jupyter notebook** — a document mixing code, output, and text. Great for exploration, bad for production code.
- **pytest** — the Python tool for writing and running automated tests. **Unit test** — a small automated check that one piece of code does what it should.
- **API (application programming interface)** — a way for programs to talk to each other over the web. An **endpoint** is one URL that does one thing (e.g., `POST /predict`). **FastAPI** — a Python framework for building APIs quickly.
- **Docker / Dockerfile** — packages your app with everything it needs so it runs identically anywhere. **Container** — a running instance of that package.
- **CI/CD (continuous integration / deployment)** — automation that runs your tests on every push (CI) and deploys if they pass (CD). **GitHub Actions** — GitHub's built-in CI.
- **Deploy** — put your app on a server so others can use it via a URL. Render, Fly.io, and Hugging Face Spaces do this for free at small scale.
- **Gradio / Streamlit** — Python libraries for building simple web interfaces for ML demos in a few lines.
- **SQLite / Postgres** — databases. SQLite is a single file, perfect for small projects. **SQLAlchemy** — Python library for talking to databases.
- **Claude Code / Cursor** — AI coding tools: Claude Code is a terminal agent that edits your codebase; Cursor is an editor with AI built in. **Copilot** — GitHub's AI autocomplete.
- **Open source** — code anyone can read, use, and contribute to. **Good first issue** — a label maintainers put on easy tasks for newcomers.

**Algorithms and interviews**
- **DS&A (data structures & algorithms)** — how data is organized (arrays, hash maps, trees, graphs) and the standard methods for operating on it (searching, sorting, traversal). The subject of coding interviews.
- **LeetCode** — the website where interview-style coding problems live. **NeetCode** — a free site that organizes the 150 most useful ones into a learning order with video explanations. **NeetCode 150** — that list.
- **Easy / Medium / Hard** — LeetCode difficulty labels. Interviews are mostly mediums.
- **Time / space complexity, Big-O** — how an algorithm's running time and memory grow with input size (O(n), O(n log n), O(n²)). You'll be asked for it after every solution.
- **Patterns** — two pointers, sliding window, hash map, stack, binary search, BFS/DFS, dynamic programming (DP), backtracking, greedy. Recognizing the pattern is 80% of solving the problem.
- **Dynamic programming (DP)** — solving a problem by breaking it into overlapping subproblems and remembering the answers.
- **System design interview** — a 45-minute discussion where you design a large system (or an ML/AI system) on a whiteboard, discussing trade-offs.
- **STAR** — Situation, Task, Action, Result: the structure for behavioral-interview stories.
- **Take-home** — a small project you're given a few hours or days to complete as part of interviewing.
- **Referral** — an employee submits your application internally. Dramatically increases the chance a human reads it.
- **Mock interview** — a practice interview with a peer or a service.

**Machine learning fundamentals**
- **Model** — a function learned from data that makes predictions. **Training** — the process of learning it. **Features** — the input columns. **Target / label** — what you're predicting.
- **Supervised learning** — learning from labeled examples (regression predicts a number, classification predicts a category). **Unsupervised** — finding structure without labels (clustering).
- **Train / validation / test split** — train on one part, tune on another, and measure real performance on a third that you touch exactly once.
- **Cross-validation (k-fold)** — repeating train/validate on k different splits and averaging, for a more reliable estimate.
- **Overfitting** — memorizing the training data instead of learning the pattern; great training score, bad real-world score. **Underfitting** — too simple to capture the pattern. **Bias/variance trade-off** — the formal name for this tension.
- **Regularization** — techniques that penalize complexity to reduce overfitting (ridge, lasso, dropout).
- **Loss function** — a number measuring how wrong the model is; training tries to minimize it. **Gradient descent** — the algorithm that does so by taking small steps downhill. **Learning rate** — the step size.
- **Metrics** — accuracy (fraction right), **precision** (of what I flagged, how much was right), **recall** (of what should be flagged, how much I caught), **F1** (their harmonic mean), **ROC/AUC** (how well the model ranks positives above negatives), **RMSE / R²** (regression error and fit).
- **Imbalanced classes** — when one category is rare (fraud, defaults). Accuracy is misleading here; use precision/recall.
- **Baseline** — the dumbest reasonable prediction (mean, majority class). If your model doesn't beat it, it's not a model.
- **Feature engineering** — creating better input columns from raw data.
- **Random forest / gradient boosting (XGBoost, LightGBM)** — ensemble methods that combine many decision trees. The workhorses of tabular ML.
- **PCA** — a way to compress many features into a few. **k-means** — a clustering algorithm.
- **scikit-learn** — the standard Python library for classical ML. **pandas** — the standard library for tables. **NumPy** — the standard library for numeric arrays.

**Deep learning and LLMs**
- **Neural network** — a model made of layers of simple units, each doing a weighted sum and a nonlinearity; can learn very complex patterns. **Deep learning** — neural networks with many layers.
- **Backpropagation** — the algorithm that computes how much each weight contributed to the error, so gradient descent knows which way to move. **Autograd** — software that does this automatically (PyTorch does; Karpathy's *micrograd* is a tiny version you build yourself).
- **PyTorch** — the dominant deep-learning library. **Tensor** — its multi-dimensional array type.
- **GPU** — graphics processor; makes neural network training 10–100× faster. Free ones on Google Colab.
- **Embedding** — turning a word, sentence, or item into a list of numbers (a vector) such that similar things get similar vectors. The foundation of search and retrieval.
- **Transformer** — the neural network architecture behind all modern language models. **Attention** — its core mechanism: each token looks at the other tokens to decide what matters. **GPT** — Generative Pre-trained Transformer, a transformer trained to predict the next token.
- **LLM (large language model)** — a very large transformer trained on huge text (Claude, GPT, Gemini, Llama). **Foundation model** — a broad term for these general-purpose models.
- **Token / tokenizer** — models read text in chunks called tokens (roughly ¾ of a word); the tokenizer splits text into them. Explains many LLM quirks (counting letters, math, spelling).
- **Pre-training / fine-tuning** — pre-training learns general language from huge data; **fine-tuning** adapts a pre-trained model to a task with a smaller dataset. **LoRA** — a cheap fine-tuning method that trains a small number of extra weights. **TRL / PEFT** — Hugging Face libraries for fine-tuning and LoRA. **SFT** — supervised fine-tuning.
- **Open-weight model** — a model whose weights you can download and run (Llama, Qwen, Mistral). **Frontier model** — the most capable current models, usually via API (Claude, GPT).
- **Hugging Face** — the hub where open models, datasets, and demos live, plus the *Transformers* library for using them.
- **Inference** — running a trained model to get outputs. **Latency** — how long a response takes. **Throughput** — how many per second. **Context window** — how much text the model can consider at once.
- **Prompt / prompt engineering** — the instructions you give a model, and the craft of writing them well. **System prompt** — the standing instructions set by the developer.
- **RAG (retrieval-augmented generation)** — find relevant documents first (retrieval), then have the LLM answer using them (generation). The standard way to give a model knowledge it wasn't trained on. **Chunking** — splitting documents into pieces for retrieval. **Vector database** — stores embeddings and finds the nearest ones fast (Chroma, pgvector). **Top-k** — the k most similar chunks retrieved. **Reranker** — a second model that reorders retrieved chunks by relevance. **Hybrid search** — combining keyword and vector search.
- **Agent** — an LLM that decides its own steps and calls tools in a loop to accomplish a task. **Tool use / function calling** — letting the model call your code (search, database, calculator). **Workflow** — a fixed sequence of LLM calls, as opposed to an agent's dynamic decisions. **Guardrails** — checks that keep an agent within bounds. **Human handoff** — passing to a person when the agent shouldn't proceed.
- **Evals (evaluations)** — systematic tests of whether an AI system does what you want, on a set of cases you built. **Eval set / golden set** — those hand-built cases with expected answers. **LLM-as-judge** — using a model to grade another model's outputs against a rubric or reference. **Retrieval hit rate** — how often the correct chunk appears in the retrieved top-k. **Error analysis** — reading failures one by one to find patterns.
- **Observability / tracing / structured logging** — recording what your system did (inputs, outputs, tokens, cost, latency) so you can debug and improve it.
- **Hallucination** — when a model states something false with confidence. Evals and RAG are how you measure and reduce it.
- **Model routing** — sending easy requests to a cheap model and hard ones to an expensive one. **Caching** — reusing previous results to save time and money.
- **MCP (Model Context Protocol)** — a standard for connecting AI models to tools and data sources.

**Compliance terms you already know from work**
- **GMP / GxP** — good manufacturing (and general good-practice) regulations in life sciences. **HIPAA** — US health-data privacy law. **21 CFR Part 11** — FDA rules on electronic records and signatures. **PHI** — protected health information. Relevant here only as the reason Rule 5 exists.

---

*Built September 2026. Revisit `diagnostic.md` whenever you doubt the progress. The version of you that doesn't recognize yourself is built one morning at a time.*
