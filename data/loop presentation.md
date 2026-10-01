# 0.1 What You'll Ship


Here is what your setup looks like at the end of this course. At 7am, while you are asleep or at the gym, a scheduled loop wakes up on your machine. It reads your GitHub backlog, pulls the top task labeled afk and ready, and ships it: writes the code test-first inside a locked-down container, passes the typecheck, passes the test suite, passes the pre-commit hook, opens a pull request, comments its reasoning on the issue, and sends you a one-line notification. At 9am you read a short report with coffee, merge or push back, and file what you noticed as new issues. Tomorrow at 7am it happens again.

Nothing in that paragraph is speculative. Every piece is a lesson in this course, every command already exists, and builders are running this today on real products.

We call that build the Daily Shipper, and it is the capstone in lesson 6.3. The acceptance bar for it is concrete: 5 consecutive scheduled runs, at least 3 PRs merged, zero interventions mid-run, and the morning report arriving on time. Everything between here and there exists to make that bar reachable, and safe.

The two-loop map
If you took Harness 101, you already know there is a loop inside every agent: reason, act, observe, repeat. That inner loop is what happens inside one agent run, and Harness 101 owns it. This course is about the outer loop: everything that happens around the whole agent so it can run without you. Gates that check its work. A sandbox that bounds its blast radius. A backlog that feeds it tasks. A schedule that wakes it up. Hold this picture once and you will not need it re-explained again:



The inner loop got good. Claude Code can already take a well-specified task and land it. What has not caught up is the outer loop, because for most builders the outer loop is still them: prompting, waiting, reading, prompting again. Lesson 0.2 makes that uncomfortable observation precise.

The course in seven sentences
The rule of the course: every module removes one reason you have to sit there watching.

0 Orientation - What it removes: The belief that watching is the job

1 Feedback Gates - What it removes: "Nobody checks the work if I leave"

2 The Sandbox - What it removes: "It might wreck something outside the repo"

3 The Loop Itself - What it removes: "Someone has to type the next prompt"

4 The Backlog - What it removes: "Someone has to decide what's next"

5 Routing - What it removes: "Some tasks genuinely need me" (true, so route only those to you)

6 Production - What it removes: "Someone has to start it every day"

By module 3 you will run your first unattended 30-minute session. By 4.5 an agent ships a real feature overnight. By 6.3 it happens on a schedule without you starting it.

Two lab lessons (1.4, 3.4) and two capstones (4.5, 6.3) are pure practice: the lesson is the lab. Everything else follows one shape: concept, one figure, then a Practice section you run on your own repo before moving on. Do the practices. The course compounds, and a skipped module 1 practice comes back as a mystery failure in module 3.

What this course is not
Three neighboring topics are deliberately out of scope, each with a better home:

Building the loop in code. Harness 101's Build It track constructs the inner loop in Python from scratch. Here the harness is Claude Code and the loop is about 50 lines of bash you will read in full.

Multi-agent orchestration. Fan-out and fan-in across agent teams is Harness 101 module 5 territory. This course runs one loop and one human, deliberately.

Writing skills from scratch. We install and customize skills from the vault; authoring your own is Agent Skills 101.

When a lesson brushes against one of these, you get a pointer and a one-sentence recap, never a re-teach.

Prerequisites, honestly
You need three things installed and one thing that is more of a decision:

Claude Code working in a terminal. Basics assumed at the Claude Code 101 level: you know what CLAUDE.md is, you have used plan mode, you have installed a skill (Claude Code 101 lessons 2.2 and 3.2 cover PRDs and skills; skim them if either sounds fuzzy).

The gh CLI, authenticated. The backlog in this course is GitHub issues, driven entirely through gh.

A repo with tests, or the willingness to add them in module 1. This is the decision. Unattended agents without machine checks is not a workflow, it is a incident report waiting to be written, and no lesson here will pretend otherwise.

Harness 101 is the theory prerequisite. You can take this course without it, but when we say "acceptance criteria are the stop condition" and point at Harness 101 lesson 5.2 instead of re-deriving it, that is where the derivation lives.

The companion repo
Everything you install in this course lives in one public repo: claude-code-vault. The /ship, /prd-to-backlog, and /grill-me skills, plus ralph/loop.sh, the bash loop the whole back half of the course runs on. You will read every line of it before you trust it, in 3.1.

🔧 Practice
Verify the toolchain in four commands. Run each and check the expected outcome:

````mermaid
claude --version
gh auth status
node --version
git --version
Expected: a Claude Code version number (anything current), gh showing Logged in to github.com with a green check, Node 18 or newer, any git. If gh auth status fails, run gh auth login and pick HTTPS.
````

Then clone the companion repo somewhere you keep projects:

git clone https://github.com/JayZeeDesign/claude-code-vault
ls claude-code-vault/.claude/skills
ls claude-code-vault/ralph
Expected: a skills/ directory containing ship, prd-to-backlog, and grill-me among others, and a ralph/ directory with loop.sh, once.sh, and prompt.md.

Optional but smart: open ralph/prompt.md and read it once now, cold. It is 17 lines. Module 3 will land harder when you already recognize every one of them.

Last step, 60 seconds: pick the repo you will run this course on. Your own side project beats a toy repo, because module 5 asks you to use the product like a user, and you cannot fake caring about a todo-list demo. Write the repo name down. That repo is about to get a lot of commits you did not type.
