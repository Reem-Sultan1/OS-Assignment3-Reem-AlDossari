# 📝 MY_WORK: Student Information, Development Log, Reflection & Answers

> This is the **only file** your instructor reads to grade Parts 3 and 4 (documentation and video). Everything you write here must be **in your own words**.

---

## 🛑 STOP: Read This Before You Do Anything Else

> ### 1️⃣ Read the whole `README.md` first
> The `README.md` in this repository contains the full instructions: how this assignment continues Assignment 1, the Chapter 5 recap, class descriptions, feature specifications, question prompts and the video script. **If you skip it, you will lose marks.**
>
> ### 2️⃣ Understand the full code before answering any question
> Open `SchedulerSimulationSync.java` and read it **from top to bottom**. You must be able to explain what `SharedStats`, `ReadyQueue`, `CpuWorker`, `RaceWindow.pause()`, `ReentrantLock` and `Semaphore` do **before** you write a single answer in Parts B and C. **Run the original starter first** (it is intentionally broken) and **save its output**: you need it for Question 1 of Part C.
>
> ### 3️⃣ Use only the code of this repository
> Work **only** on `SchedulerSimulationSync.java` from this repository. Do **not** copy or paste code from your previous assignments.
>
> ### 4️⃣ Commit many times, not once
> A single commit, or all commits made in the last hour, costs you **-0.5 mark**. See the [Commit Rules](#-commit-rules-mandatory) below.

**How to use this file:**
1. Fill in your **Student Information** (below) right now.
2. Follow the steps in the **Work Roadmap** in order.
3. Update the **Development Log** *every time* you work on the assignment, not at the end.
4. Do not delete any section header. Replace the `[...]` placeholders with your own text.

---

## 👤 Student Information

> ⚠️ **WARNING:** Fill this in first. Your name and ID must match the student ID you set in `SchedulerSimulationSync.java` (line 304) and the one you say in your video.

| Field | Your Answer |
|-------|-------------|
| **Full Name** | Reem AlDossari |
| **Student ID** | 446051846 |
| **University Email** | 446051846@std.psau.edu.sa |
| **GitHub Username** | Reem-Sultan1 |
| **Repository Link** |https://github.com/Reem-Sultan1/OS-Assignment3-Reem-AlDossari. |
 
---

## 🎥 Video Link

**Video Link**: [Watch my Assignment 3 demo](https://drive.google.com/file/d/15T3pMzC0YnMdKf2zy3I6owjrz1odZcFY/view) 

> ⚠️ **WARNING:** The video must be **publicly accessible** ("Anyone with the link can view") on **Google Drive**, **YouTube (Unlisted or Public)** or any other cloud file-sharing system. A private, restricted or broken link counts as a **missing video (-1 mark)**.
>
> 💡 **TIP:** Open the link in a **private/incognito window** before you submit. If it asks you to log in or request access, it is not public.
>
> 📌 **NOTE:** The link goes in **this file only** (`MY_WORK.md`), **not** in `README.md`. Name your video file `StudentID_Assignment3_Demo.mp4`. It must last **2 to 3 minutes**.

---

## 🗺️ Work Roadmap (follow in this order)

| Step | What to do | Where | Marks |
|:----:|------------|-------|:-----:|
| 0 | Read `README.md`, read the full code, **run the original starter and save its output** (it fails on purpose) | Your IDE | – |
| 1 | Fork, rename, keep the repo **PUBLIC**, set your student ID (line 304), **commit** | GitHub + code | Part 1 (1) |
| 2 | Feature 1: Mutex lock on the ready queue, **commit** | Code | Part 2 (0.25) |
| 3 | Feature 2: Mutex lock(s) on the shared statistics, **commit** | Code | Part 2 (0.25) |
| 4 | Feature 3: Counting semaphore instead of busy waiting, **commit** | Code | Part 2 (0.5) |
| 5 | Development Log (5+ entries, different dates) | This file, Part A | Part 3 (0.5) |
| 6 | Reflection (4 questions) | This file, Part B | Part 3 (0.5) |
| 7 | Technical Answers (4 questions) | This file, Part C | Part 3 (0.5) |
| 8 | Record the video, upload it, paste the link above | Video + this file | Part 4 (1.5) |
| 9 | Final check, then submit the repo link on Blackboard | Blackboard | – |

> 💡 **TIP:** Tick each step off as you go. Do not leave the log, the reflection or the video for the last day.

---

## 🔁 Commit Rules (MANDATORY)

> ### ⚠️ MANY COMMITS ARE REQUIRED. A single bulk commit is penalized (-0.5 mark).

**Minimum: 4 meaningful commits. Aim for 7 or more.**

| # | Commit | Example message |
|:-:|--------|-----------------|
| 1 | Student ID set | `Set my student ID: 441234567` |
| 2 | Feature 1: Ready queue lock | `Feature 1: Protected the ready queue with a ReentrantLock` |
| 3 | Feature 2: Statistics locks | `Feature 2: Added locks to the shared statistics counters` |
| 4 | Feature 3: Semaphore | `Feature 3: Replaced busy waiting with a counting semaphore` |
| 5 | Development log entries | `Docs: Added development log entries 1-3` |
| 6 | Reflection and answers | `Docs: Completed reflection and technical answers` |
| 7 | Video link | `Docs: Added demo video link` |

**Rules:**
- ✅ **One commit per feature.** Do not put all three features in one commit.
- ✅ **Commit after each work session**, and after each part of this file.
- ✅ **Spread your commits over different dates.** Not all in one day.
- ❌ **Do not make all commits in the last hour** before the deadline (November 14, 2026).
- ❌ **No vague messages** like `done`, `update` or `final version`.

> 💡 **TIP:** Your commit history is checked and you **show it in your video** (at least 4 commits visible). Your development log dates should match your commit dates.
>
> 💡 **TIP:** **Use VS Code** (see *Recommended Development Environment* in `README.md` for the full setup). Sign in to GitHub in VS Code, then commit from the Source Control panel (Ctrl+Shift+G) → stage → write a message → Commit → Sync/Push. You can edit and commit this file the same way. **Pushing** matters: commits that are not pushed to GitHub are invisible to the instructor.

---

# Part A: Development Log (0.5 mark)

> ⚠️ **WARNING:** Minimum **5 entries**, spread over **different dates**. Five entries written on the same day, or written all at once at the end, will lose marks and look like a copy. Entry dates should be **between the start of the assignment and the deadline (November 14, 2026)**.
>
> 💡 **TIP:** Write an entry at the **end of each work session**, while you still remember what happened. It takes 5 minutes.
>
> 💡 **TIP:** Be specific. "Worked on the code" is a weak entry. "Added a `ReentrantLock queueLock` to `ReadyQueue` and wrapped the body of `poll()` in `lock()` / `try` / `finally { unlock() }`" is a strong one.
>
> 📌 **NOTE:** Each entry needs: date and time, what you did, details, challenges, solution, and time spent. Real challenges are fine (and expected). Do not invent fake ones.

## Example Entry (do not copy it, write your own)

### Entry 1 - [November 2, 2026, 4:30 PM]
**What I did**: Forked the repository, set my student ID, and ran the original starter

**Details**:
- Forked the starter repository and renamed it
- Changed student ID on line 304 to my actual ID (441234567)
- Ran the original program: 4 CPUs started, three of them picked `P1`, then `IllegalThreadStateException` and the watchdog stopped the program
- Saved the output in a text file for Question 1
- Committed and pushed: `Set my student ID: 441234567`

**Challenges**: I did not understand why the same process was picked by three CPUs

**Solution**: Read `ReadyQueue.poll()` again and found the `RaceWindow.pause()` between reading the head and removing it

**Time spent**: 45 minutes

---

## Your Development Log

### Entry 1 - November 15, 2026, approximately 10:35 PM

**What I did**:
Set up my GitHub repository and ran the starter simulation.

**Details**:
I forked the official starter repository, renamed my fork, and cloned it in VS Code. I changed studentID to 446051846, committed the change, and pushed it to GitHub. I ran the starter and saved its verification output before making any synchronization changes.

**Challenges**:
Git initially refused to create my commit because my name and email were not configured. The starter also reported failures in the verification block.

**Solution**:
I configured my Git name and university email for this repository, then completed the commit and push. I saved the original output so I could compare it with the results after implementing synchronization.

**Time spent**:
30 minutes.

---

### Entry 2 - November 15, 2026, approximately 11:05 PM

**What I did**:
Implemented and tested Feature 1 to protect the shared ready queue.

**Details**:
I added a ReentrantLock named queueLock to ReadyQueue. I used it in add(), poll(), processOf(), and snapshot() to protect accesses to list and map. Every lock was released in a finally block. I tested this feature five times.

**Challenges**:
I accidentally duplicated the local thread declaration in add() and missed a closing brace while editing snapshot(). The verification counters also continued to show mismatches after the queue changes.

**Solution**:
I removed the duplicate declaration and corrected the closing brace. I checked that all four queue methods used the same lock. The runs completed all 10 processes, while the remaining statistics mismatches and busy waiting were left for Features 2 and 3.

**Time spent**:
 35 minutes.
---

### Entry 3 - November 15, 2026, approximately 11:50 PM

**What I did**:
Implemented Feature 2 to protect the shared statistics.

**Details**:
I added one ReentrantLock named statsLock in SharedStats. I used it in the three update methods and the three getters. Each method releases the lock in a finally block. I chose one lock to keep the locking rules simple, although separate locks could allow independent counters to be accessed concurrently.

**Challenges**:
After Feature 1, the simulation completed all processes, but contextSwitchCount and totalServiceTime still differed from their expected values. Concurrent updates could read the same old value and overwrite each other.

**Solution**:
I protected each complete read-modify-write sequence and used the same lock for the getters. In the first three test runs, the results matched 17 context switches, 10 completed processes, and 62665 ms of service time. Busy-waiting polls remained above zero for Feature 3 to address.

**Time spent**:
 20 minutes.
---

### Entry 4 - November 16, 2026, approximately 5:45 PM

**What I did**:
Implemented Feature 3 using a counting semaphore and a clean shutdown signal.

**Details**:
I initialized availableProcesses to zero because the ready queue starts empty. Each add() call releases one permit after adding a process. CpuWorker calls waitForAvailableProcess() before polling the queue. I removed the busy-waiting branch and added a completion check after acquiring a permit.

**Challenges**:
CPUs waiting on acquire() needed to wake up when all processes finished. I also accidentally pasted signalShutdown() twice, which caused duplicate declarations.

**Solution**:
I removed the duplicate code and used shutdownSignaled under queueLock to send the shutdown signal once. signalShutdown() releases SharedStats.totalCPUs permits so waiting CPUs can exit. The verification output showed 17 context switches, 10 completed processes, 62665 ms of service time, and zero busy-waiting polls.

**Time spent**:
 25 minutes.

---

### Entry 5 - November 17, 2026, approximately 9:00 PM

**What I did**:
Started completing the assignment documentation in MY_WORK.md.

**Details**:
I entered my name, student ID, university email, GitHub username, and repository link. I documented the setup, ready queue lock, statistics lock, and semaphore implementation using my actual work dates and saved outputs.

**Challenges**:
I needed to distinguish the original starter failures from the results after each feature. I also needed to explain why some verification mismatches remained during the intermediate stages.

**Solution**:
I used my saved starter output and screenshots to describe the results at each stage. I recorded how Feature 1 protected the queue, Feature 2 corrected the statistics, and Feature 3 reduced busy-waiting polls to zero.

**Time spent**:
 20 minutes so far.

---

### Entry 6 - [Optional - Date and Time]
**What I did**:

**Details**:

**Challenges**:

**Solution**:

**Time spent**:

---

## Development Log Summary

> 💡 **TIP:** Fill this in **last**, after all entries are written.

**Total time spent on assignment**: [X hours]

**Most challenging part**:

**Most interesting learning**:

**What I would do differently next time**:

---

# Part B: Reflection (0.5 mark)

> 🛑 **STOP:** Do **not** start this part until you have read the `README.md`, read the **entire** `SchedulerSimulationSync.java`, run it, and finished the three features.
>
> ⚠️ **WARNING:** Each answer must be **5 to 7 sentences**, in **your own words**. Copied or AI-generated answers without understanding get **0 marks for the whole assignment**. You may be asked to explain them in person.
>
> 💡 **TIP:** Mention concrete things you actually did: a method you wrote, an error you hit, a line of output you saw. Generic answers score low.
>
> 💡 **TIP:** Draft your answer in a few bullet points first, then turn them into sentences.

## Question 1: What did you learn about synchronization?

> 💡 **TIP:** Talk about race conditions (read-modify-write), critical sections, mutual exclusion with `ReentrantLock` and `try/finally`, the role of a counting semaphore, and what surprised you when the starter failed.

**Your Answer:** *(5-7 sentences)*

I learned that shared data can become inconsistent when several threads access it at the same time. A counter update involves reading a value, changing it, and writing it back, so two threads can overwrite each other's updates. In ReadyQueue, I used queueLock to protect the queue and its map, including iteration in snapshot(). In SharedStats, I protected both the updates and the getters with statsLock. I learned that finally releases a lock even when a method returns from inside try. The semaphore also showed me how CPUs can block until work becomes available and wake up when the simulation finishes.

## Question 2: What was the most challenging part of this assignment?

> 💡 **TIP:** Pick **one** specific challenge (understanding why the starter failed, choosing the lock granularity, the initial value of the semaphore, the shutdown of the CPUs, Git, the video) and say *why* it was hard.

**Your Answer:** *(5-7 sentences)*

The most challenging part was handling the shutdown of CPUs waiting on the semaphore. When the queue is empty, acquire() blocks a CPU until a permit becomes available. After the last process finishes, there may be no more add() calls to release permits. I needed to understand how those waiting CPUs would wake up and stop. I used signalShutdown() to release totalCPUs permits and checked completion immediately after acquire(). I also protected shutdownSignaled with queueLock so the shutdown signal would be sent only once.

## Question 3: How did you overcome the challenges you faced?

> 💡 **TIP:** Describe your method: reading the slides and the documentation, adding `System.out.println` to debug, running the program many times, re-reading the README, testing after each small change, asking for help.

**Your Answer:** *(5-7 sentences)*

I worked on one feature at a time so I could understand what each change affected. I saved the original verification output before modifying the synchronization code. I asked for step-by-step help and checked where each lock and semaphore operation belonged. When I duplicated a declaration or misplaced a brace, I reviewed the surrounding method and corrected it. I ran the program repeatedly and compared the observed statistics with the expected values. Seeing the first three checks pass after Feature 2 and all four pass after Feature 3 helped me connect each change to its result.

## Question 4: Where can synchronization concepts be applied in real-world applications?

> 💡 **TIP:** Use real applications you know (banking and money transfers, ticket or seat booking, a shared counter on a website, a print queue, a database) and connect each one to what you built here (shared data, critical section, lock or semaphore).

**Your Answer:** *(5-7 sentences)*

Synchronization can be used in applications where several threads share data or resources. In a banking application, concurrent updates to the same account balance must be coordinated to prevent lost updates. In a ticket booking system, checking and reserving the same seat must be coordinated so two customers cannot both reserve it. A print service can use a shared queue protected by a lock, similar to ReadyQueue in this assignment. A counting semaphore can make worker threads wait until a new print job arrives. Shared website statistics also need protected updates, similar to the counters in SharedStats.

### Optional: What would you like to learn more about?

[Any topics related to synchronization or operating systems that you're curious about?]

### Optional: How confident do you feel about synchronization concepts now?

[Beginner / Intermediate / Confident. What do you understand well? What needs more practice?]

### Optional: Feedback on the assignment

[Any comments? Was it helpful? Too easy or hard? Suggestions?]

---

# Part C: Technical Answers (0.5 mark)

> 🛑 **STOP:** You cannot answer these questions without understanding the code. Re-read `SchedulerSimulationSync.java` and **run it** first. Your answers must reference **your own code and your own output** (your student ID makes your output and your expected values unique).
>
> ⚠️ **WARNING:** Each answer must be **3 to 5 sentences**, with specific examples from your code or output. Use correct terms: race condition, critical section, mutual exclusion, mutex lock, semaphore, busy waiting, deadlock, producer, consumer.
>
> 💡 **TIP:** Keep the output of the **original starter** and the output of your **final version** in text files or screenshots, so you can copy real snippets for Question 1.

## Question 1: Race Condition in Your Own Output

**Question**: Run the **original starter** (before any fix) and paste the **verification block** of that run. Which value was wrong (expected vs observed)? Explain **step by step**, with two named threads/CPUs, how **one lost update** happens on one of the shared variables (read, `RaceWindow.pause()`, write). Why can the same bug happen on a real machine even without `RaceWindow`, and why is it hard to detect?

> ⚠️ **WARNING:** The snippet must come from **your own run** (with your student ID), not from a classmate or from this README.
>
> 💡 **TIP:** Use a small timeline: *CPU-1 reads `contextSwitchCount` = 12 → CPU-2 reads 12 → CPU-1 writes 13 → CPU-2 writes 13 → one increment is lost.* If your starter run crashed before printing numbers, run it several times (or paste the exception and the watchdog message and explain it).

**Your Answer:** *(3-5 sentences)*

In my original starter run, the observed context switches, completed processes, and total service time were all zero, compared with expected values of 17, 10, and 62665 ms. The output also contained an exception trace through ReadyQueue.snapshot(), so these zero values do not by themselves demonstrate a lost counter update. After Feature 1, one run completed all 10 processes but recorded only 14 of the expected 17 context switches, showing three missing increments. A lost update can occur when two threads read the same counter value and then both write the same incremented value. On a real machine, thread preemption can cause this interleaving without RaceWindow.pause(), and the timing makes the bug difficult to reproduce consistently.

Verification block of the **original starter**:

```
═══ VERIFICATION (expected values are computed from YOUR seed) ═══
  Context switches (quanta executed)     expected 17       observed 0        ✘ MISMATCH
  Completed processes                    expected 10       observed 0        ✘ MISMATCH
  Total service time (ms)                expected 62665    observed 0        ✘ MISMATCH
  Busy-waiting polls (must be 0)         expected 0        observed 0        ✔
  ✘ At least one check failed (see the ✘ lines above): a race condition or busy waiting is still present.
```

Verification block of **my final version**:
```
═══ VERIFICATION (expected values are computed from YOUR seed) ═══
  Context switches (quanta executed)     expected 17       observed 17       ✔
  Completed processes                    expected 10       observed 10       ✔
  Total service time (ms)                expected 62665    observed 62665    ✔
  Busy-waiting polls (must be 0)         expected 0        observed 0        ✔
  ✔ All shared values are consistent.
```

**Explanation of the timeline:**
For example, suppose contextSwitchCount is 5. A process thread running on CPU-1 reads 5 into its local tmp and pauses inside RaceWindow.pause(). A process thread running on CPU-2 also reads 5 before either thread writes its update. Both threads then write 6, so the final value is 6 instead of 7. statsLock prevents this by protecting the entire read-pause-write sequence.

## Question 2: Critical Sections and Lock Granularity

**Question**: List the **critical sections** you protected (variables and methods) and the lock(s) you used. **Lock granularity:** did you use **one lock** for the three statistics or **one lock per variable**? Why, and what is the trade-off? Why is the **ready queue** protected by a **different** lock than the statistics? Explain how your solution provides **mutual exclusion**, and discuss **progress** and **bounded waiting** (a default `ReentrantLock` is not fair: what does that imply?).

> 💡 **TIP:** The three counters are independent: does updating `contextSwitchCount` need to block an update of `totalServiceTime`? Also think about what could go wrong (deadlock, or long waiting) if the queue lock and the statistics lock were the **same** lock and a thread held it while doing something slow.

**Your Answer:** *(3-5 sentences)*

I used queueLock to protect list and map in ReadyQueue.add(), poll(), processOf(), and snapshot(), and to protect shutdownSignaled in signalShutdown(). I used one statsLock for the three statistics update methods and their three getters because it keeps the locking rules simple, although it serializes accesses to independent counters. The queue uses a separate lock so queue operations and statistics operations can proceed independently. Mutual exclusion is provided by acquiring the appropriate lock, and finally releases it so waiting threads can continue. The critical sections are finite and contain no semaphore waits, which supports progress, but the default nonfair ReentrantLock does not guarantee bounded waiting or acquisition in arrival order.

| Critical section (variable / method) | Lock used | Why it needs protection |
|---|---|---|
| list and map in ReadyQueue.add() | queueLock | Adds both entries before another CPU accesses them. |
| list in ReadyQueue.poll() | queueLock | Makes checking, reading, and removing the head atomic relative to other queue operations. |
| map in ReadyQueue.processOf() | queueLock | Coordinates reads with map updates. |
| list and map in ReadyQueue.snapshot() | queueLock | Prevents changes during iteration. |
| shutdownSignaled in ReadyQueue.signalShutdown() | queueLock | Ensures shutdown permits are released once. |
| contextSwitchCount in incrementContextSwitch() and getContextSwitchCount() | statsLock | Prevents lost increments and coordinates reads. |
| completedProcessCount in incrementCompletedProcess() and getCompletedProcessCount() | statsLock | Protects the completion count used by the CPUs. |
| totalServiceTime in addServiceTime() and getTotalServiceTime() | statsLock | Prevents lost additions and coordinates reads. |

## Question 3: Busy Waiting vs Semaphore

**Question**: Describe the **busy waiting** of the starter and its cost (give the `Busy-waiting polls` number from your **starter** run). What does the **value of your semaphore** represent? What is its **initial value** and why? What is its value right after the `numProcesses` initial `add()` calls? Why does the last CPU call `release(totalCPUs)` at the end, and what would happen if it did not?

> 💡 **TIP:** Think about what a CPU does when the queue is empty in the starter, and what a CPU does in your final version (is it running, ready or blocked?). Also check what happens to a CPU blocked in `acquire()` when no process will ever be added again.

**Your Answer:** *(3-5 sentences)*

The starter repeatedly polled an empty queue, slept for 20 ms, and tried again, causing repeated wakeups and unnecessary checking. My original starter run recorded zero busy-waiting polls while failing the other checks, whereas one run after Feature 1 recorded 61 polls. During normal operation, availableProcesses tracks permits for queued work, and acquire() blocks a CPU when no permit is available. Its initial value is zero because the queue starts empty, and after the 10 initial add() calls it is 10 before the CPUs start acquiring permits. At completion, signalShutdown() releases totalCPUs permits once so blocked CPUs wake up, detect completion, and exit, otherwise they could remain blocked indefinitely.

## Question 4: Classical Problems and Deadlock

**Question**: The CPUs and the ready queue look like a classical synchronization problem of Chapter 5. **Name it**, and say who plays the **producer** and the **consumer** roles (careful: here the CPUs also re-enqueue processes). If the ready queue were **bounded** (capacity `K`), name the **three semaphores** you would need and their **initial values**. Describe a **deadlock scenario** that appears if a thread acquired the **mutex before** waiting on the semaphore (or if two locks were acquired in different orders), and say **which of the four necessary conditions** you would break to prevent it.

> 💡 **TIP:** Recall the bounded-buffer solution of the slides (`empty`, `full`, `mutex`) and the order of `wait()` calls in the producer and the consumer. For the deadlock, think about a producer that holds the mutex while waiting for a free slot that only a consumer (who needs the mutex) can create.

**Your Answer:** *(3-5 sentences)*

**Classical problem and roles**:
This is the producer-consumer problem with a shared ready queue. main produces the initial processes, while CPUs consume queued work and also act as producers when they re-enqueue unfinished processes.

**Semaphores for a bounded queue (name and initial value)**:
For an initially empty queue of capacity K, the three semaphores are empty initialized to K, full initialized to 0, and mutex initialized to 1.

**Deadlock scenario and prevention**:
If the queue is full and a producer acquires mutex before waiting on empty, it holds mutex while waiting for a consumer to free a slot, but the consumer also needs mutex to remove an item. Acquiring the resource semaphore before mutex prevents this scenario by avoiding holding the mutex while waiting for a queue resource, breaking hold and wait in this scenario.

## Summary

**Key concepts I understood through these questions:**
1. How race conditions cause lost updates and how locks protect critical sections.
2. How a counting semaphore blocks CPUs until work is available.
3. Why waiting CPUs need a shutdown signal when all processes finish.

**Concepts I need to study more:**
1. Lock fairness, starvation, and bounded waiting.
2. Deadlock prevention and synchronization in bounded queues.

---

# ✅ Final Checklist (complete before submitting)

> ⚠️ **WARNING:** Go through every line. Blackboard does not accept submissions after the deadline, which is **November 14, 2026**.

**Repository**
- [ ] Repository is **PUBLIC** (Settings → Danger Zone → Visibility)
- [ ] Repository is renamed to `OS-Assignment3-YourFirstName-YourLastName`
- [ ] GitHub account uses the university email (`@std.psau.edu.sa`)

**Code**
- [ ] Student ID is set in `SchedulerSimulationSync.java` (line 304)
- [ ] My code is based **only** on the starter of this repository (nothing copied from previous assignments)
- [ ] Code compiles and runs with no errors, and terminates by itself (no `⛔ WATCHDOG`)
- [ ] Feature 1 (ready queue lock), Feature 2 (statistics locks) and Feature 3 (semaphore, no busy waiting) all work
- [ ] **The four verification lines are ✔ in 5 consecutive runs**
- [ ] Every lock is released in a `finally` block
- [ ] `RaceWindow`, `Config`, the verification block and the watchdog are **unchanged**
- [ ] Each feature has clear comments

**Commits**
- [ ] **At least 4 meaningful commits, ideally 7 or more**
- [ ] **One commit per feature**
- [ ] Commits are spread over **different dates** (not all in the last hour)
- [ ] Everything is **pushed** to GitHub

**This file (`MY_WORK.md`)**
- [ ] Full name and student ID filled in at the top
- [ ] Development log has **5+ entries** on different dates
- [ ] Reflection: 4 questions, 5-7 sentences each
- [ ] Technical answers: 4 questions, 3-5 sentences each, with examples from **your** output (starter output **and** final output pasted in Question 1)
- [ ] No `[...]` placeholders left
- [ ] No section headers deleted

**Video**
- [ ] 2-3 minutes long, named `StudentID_Assignment3_Demo.mp4`
- [ ] Shows your name, ID, repository, 3 features (and your lock granularity choice), IDE execution with the verification block, one synchronization concept, and commit history
- [ ] Link is **public** (tested in an incognito window) and pasted in the **Video Link** section above

**Blackboard**
- [ ] Submit **only** the link to your public GitHub repository

> 🎯 **Good luck!** Start early, commit regularly, and make sure you can explain every line you submit.
