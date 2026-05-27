---
title: Thesis Topic Selection — [Course/Lab Name]
layout: default
---

# Thesis Topic Selection
*[Course / Lab Name] · [Year]*  
**Deadline: [DATE TBD]**

---

## How it works

Each participant submits **one email to one TA** proposing one thesis topic. There are two paths to reach that final email. Both lead to the same outcome: your name entered into that TA's selection pool for the draw.

After the submission deadline, each TA draws one email at random from their pool using a [publicly verifiable procedure](#selection-procedure). The selected participant is paired with the TA on the proposed topic, co-supervised by the course instructor and the TA. A maximum of **six theses** will be launched in total.

---

## Path A — Pick from a TA's list

1. Browse the [TA sections](#teaching-assistants--topics) below and find a topic that interests you.
2. Email that TA directly, quoting the topic title and a short statement of motivation (≈ 150 words).
3. You will receive an **automatic receipt** immediately, and a **pool-entry confirmation** within 48 h once the TA has acknowledged your submission.

## Path B — Propose your own idea

1. Draft a topic proposal (≈ 300 words: title, motivation, expected methods, deliverables) and email it to **all TAs simultaneously** using the [group address](#contact).
2. One or more TAs may express interest. If interest is conditional, a brief *affinity conversation* follows so the TA can confirm you are a suitable candidate.
3. Once a TA confirms interest, email **that TA only** with your final proposal. You will then receive pool-entry confirmation.
4. If no TA expresses interest within 5 working days, you may revise and resubmit, or switch to Path A.

> **One submission only.** Once you receive pool-entry confirmation you cannot switch paths, change topic, or change TA. Withdraw by emailing the same TA before the deadline.

---

## Selection procedure

The draw is designed to be **publicly verifiable**: anyone can reproduce the result from public data alone, without trusting the organiser.

**Commitment step (at deadline).** The instructor commits to the final pool by publishing a hash of the submission list in a public Git commit. The commit hash is announced on this page.

**Randomness step (after deadline).** Randomness is sourced from the [drand public randomness beacon](https://drand.love), a decentralised, bias-resistant beacon run by a consortium of independent institutions. The relevant round number is announced in advance.

**Draw step.** A deterministic script combines the committed pool with the drand output to select one entry per TA. The script and full inputs are published so the result can be independently verified.

The draw script is in the [`draw/` directory of the public repository](https://github.com/[your-org]/[repo]).

---

## Teaching Assistants & Topics

Each TA section below lists their background and the topics they are offering for Path A. TAs are also open to Path B proposals related to their research area — email the [group address](#contact) with your idea.

---

### TA One Name
*PhD Candidate · [Research Group] · [University]*  
📧 [ta1@university.edu](mailto:ta1@university.edu)

[Short bio: 2–3 sentences. Research focus, methodology, relevant publications or projects. What kind of student would thrive working with you?]

**Offered topics**

| # | Title | Description |
|---|-------|-------------|
| A1 | Topic title goes here | Brief description: what the student will do, what methods they'll use, what the deliverable looks like. 2–4 sentences is ideal. |
| A2 | Topic title goes here | Brief description. |
| A3 | Topic title goes here | Brief description. |

---

### TA Two Name
*PhD Candidate · [Research Group] · [University]*  
📧 [ta2@university.edu](mailto:ta2@university.edu)

[Short bio for TA Two.]

**Offered topics**

| # | Title | Description |
|---|-------|-------------|
| B1 | Topic title goes here | Brief description. |
| B2 | Topic title goes here | Brief description. |

---

### TA Three Name
*PhD Candidate · [Research Group] · [University]*  
📧 [ta3@university.edu](mailto:ta3@university.edu)

[Short bio for TA Three.]

**Offered topics**

| # | Title | Description |
|---|-------|-------------|
| C1 | Topic title goes here | Brief description. |
| C2 | Topic title goes here | Brief description. |
| C3 | Topic title goes here | Brief description. |

---

## Key dates

| Date | Event |
|------|-------|
| [DATE TBD] | Site published; submissions open |
| [DATE TBD] | Path B: proposal emails to all TAs (latest recommended) |
| **[DATE TBD]** | **Submission deadline — 23:59 [AoE](https://www.timeanddate.com/time/zones/aoe)** |
| [DATE TBD] | Pool committed (hash published in repo) |
| [DATE TBD] | drand round used for draw (announced in advance) |
| [DATE TBD] | Results announced; selected participants contacted |

---

## Contact

**Path A submissions** go directly to the individual TA whose topic you selected (see their section above).

**Path B proposals** go to the group address: [thesis-proposals@\[domain\]](mailto:thesis-proposals@[domain]) — this reaches all TAs simultaneously.

**General questions** about the process: [instructor@\[domain\]](mailto:instructor@[domain])

> Do not send the same submission to multiple TAs individually. Only Path B group proposals are intended to go to all TAs at once.

---

*[Course/Lab Name] · [Institution] · [Year] · [Repository & draw script](https://github.com/[your-org]/[repo]) · [drand randomness beacon](https://drand.love)*
