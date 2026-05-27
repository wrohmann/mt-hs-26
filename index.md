---
title: Master's Thesis — MAS ETH in AI and Digital Technology
layout: default
---

# Master's Thesis
*MAS ETH in AI and Digital Technology · ETH Zurich, D-INFK*  
**Submission deadline: 15 June 2026, 23:59**

---

## About the thesis

The master's thesis is the capstone of the [MAS ETH in AI and Digital Technology](https://mas-aid.ethz.ch/masaid.html), offered by the Department of Computer Science (D-INFK) at ETH Zurich. It is undertaken in the final phase of the programme, after completing the three CAS components and the AI Project and Cyber Security courses.

Participants write an independent thesis on a topic of their choice that is relevant to their work or personal interest. The topic is freely selectable but must be approved by the thesis supervisor in advance. The final product must be sufficiently rigorous from a science and technology perspective and integrative of the skills developed throughout the programme — it can involve coding, empirical analysis, or system design, and may incorporate policy or market context, but cannot be purely non-technical.

Each thesis is co-supervised by Dr. Carlos Cotrini (primary supervisor) and one TA. The project description is submitted in myStudies and confirmed during the kick-off meeting (22–27 June). **Up to six theses** will be launched in this round, starting 1 July 2026.

---

## How topic selection works

Demand for thesis places typically exceeds the number of slots. To keep the process fair and transparent, places are awarded by a **publicly verifiable random draw** — nobody, not the TAs and not Carlos, can influence or predict who is selected, and anyone can re-check the result.

Each participant ends up sending **one email to one TA** proposing one thesis topic. There are two paths:

**Path A — Pick a topic from a TA's list.**

1. Browse the [TA sections](#teaching-assistants--topics) below and find a topic that interests you.
2. Email that TA directly, quoting the topic title and a short statement of motivation (≈ 150 words).
3. You will receive an automatic **receipt** once the TA acknowledges your email, followed by a **pool-entry confirmation** that includes your assigned submission id (a 16-character hex string). From that point your submission appears — by id and topic only, never by name — in the public list at [`submissions/`](https://github.com/carloscotrini/mas-mt-hs26/tree/main/submissions).

**Path B — Propose your own idea.**

1. Draft a short proposal (title + a few sentences on motivation, expected methods, and deliverable) and email it to **all TAs simultaneously** at [wrohmann@ethz.ch](mailto:wrohmann@ethz.ch).
2. One or more TAs may express interest. If interest is conditional, a brief affinity conversation follows so the TA can confirm you are a suitable candidate.
3. Once a TA confirms interest, email **that TA only** with your final proposal. You will then receive receipt and pool-entry confirmation as in Path A.
4. If no TA expresses interest by **13 June**, you may revise and resubmit or switch to Path A before the deadline.

Both paths end with your name in that TA's selection pool. After the deadline each TA runs an independent draw over their own pool, using a shared public random seed. The rank-1 participant is offered the place; if they decline or do not respond within 48 hours, the offer rolls down to rank 2, then rank 3, and so on within the same TA's pool.

> **One submission only.** Each participant may enter only one pool with one submission. If multiple submissions from the same participant are detected, all of them are voided. Once you receive pool-entry confirmation you cannot switch paths, change topic, or change TA. Withdraw by emailing the TA before 15 June 23:59.

---

## Selection procedure

The draw is implemented in [`selection.py`](https://github.com/carloscotrini/mas-mt-hs26/blob/main/selection.py) in the [public repository](https://github.com/carloscotrini/mas-mt-hs26). Its fairness rests on three time-stamped, signed Git tags — each one locks in a commitment *before* the information that could game it becomes available:

| Tag | Created | What it fixes |
|-----|---------|---------------|
| `pre-deadline` | Before submissions open | The draw script, verification tooling, and the exact drand round number |
| `post-deadline` | After deadline, before drand round | The full list of confirmed submissions |
| `draw` | After drand round is published | The beacon value and the computed `result.json` |

**Scoring.** For each submission the script computes:

```
score = sha256(f"{beacon_value}|{ta}|{submission_id}")
```

Within each TA's pool, submissions are sorted by score from smallest to largest. The smallest score is rank 1. Because `beacon_value` is unknown when submission ids are assigned and unknown to everyone until drand publishes it, every entry has an equal 1/*n* chance of rank 1.

**Randomness source.** The beacon value comes from [drand](https://drand.love), a public distributed randomness beacon operated by the League of Entropy. No single party can predict or control its output. The relevant round number is committed under the `pre-deadline` tag before submissions open.

**Verification.** After the `draw` tag is published, anyone can audit the result:

```
pip install -r requirements.txt
python verify_draw.py
```

This recomputes the ranking from the frozen submissions and beacon, checks it against the published `result.json`, and verifies the drand cryptographic signature. Full details in [PROCEDURE.md](https://github.com/carloscotrini/mas-mt-hs26/blob/main/PROCEDURE.md).

---

## Key dates

| Date | Event |
|------|-------|
| 29 May | TAs submit mini-CVs |
| 5 June | TAs publish thesis topic lists |
| 8 June | Participants notified by email — submissions open |
| 13 June | Path B: latest recommended date to send group proposal |
| **15 June, 23:59** | **Submission deadline** |
| 16 June | `post-deadline` tag published; pool committed |
| 19 June | drand round published; `draw` tag and `result.json` published; selected participants notified |
| 22–27 June | Kick-off meeting with TA; project description submitted in myStudies and confirmed by Carlos |
| **1 July** | **Thesis start** |

---

## Primary supervisor

### Dr. Carlos Cotrini
*Senior Scientist (Focus Education) · Institute of Machine Learning · ETH Zurich*  
📧 [ccarlos@inf.ethz.ch](mailto:ccarlos@inf.ethz.ch) · 🌐 [people.inf.ethz.ch/ccarlos](https://people.inf.ethz.ch/ccarlos/)

Carlos is a lecturer at the Institute of Machine Learning at ETH Zurich, working under Prof. Joachim Buhmann. He holds a doctorate in information security from ETH Zurich (supervisor: Prof. David Basin), where he developed expertise in privacy-preserving machine learning and security analysis. His current research focuses on robust machine learning algorithms, privacy-preserving technologies, and educational methodologies. Recent publications include work on differentially private boosted decision trees (ACM CCS 2024) and automated large-scale analysis of cookie notice compliance (USENIX Security 2024).

All theses are co-supervised by Carlos and one TA.

---

## Teaching Assistants & Topics

Each TA section below lists their background and the topics they are offering for Path A. TAs are also open to Path B proposals in their research area — send your proposal to the [group address](#contact).

---

### Winston Rohmann *(Head TA)*
*[Role] · [Research Group] · ETH Zurich*  
📧 [wrohmann@ethz.ch](mailto:wrohmann@ethz.ch)

[Bio placeholder — Winston to fill in.]

**Offered topics**

| # | Title | Description |
|---|-------|-------------|
| WR-1 | *Topic title* | *Brief description — to be filled in by 5 June.* |
| WR-2 | *Topic title* | *Brief description.* |

---

### Christina Tsakanika
*[Role] · [Research Group] · ETH Zurich*  
📧 [christina.tsakanika@\[domain\]](mailto:christina.tsakanika@[domain])

[Bio placeholder — Christina to fill in: 2–3 sentences on research focus, methods, and the kind of student who would thrive working with you.]

**Offered topics**

| # | Title | Description |
|---|-------|-------------|
| CT-1 | *Topic title* | *Brief description — to be filled in by 5 June.* |
| CT-2 | *Topic title* | *Brief description.* |

---

### Daniele Russica
*[Role] · [Research Group] · ETH Zurich*  
📧 [daniele.russica@\[domain\]](mailto:daniele.russica@[domain])

[Bio placeholder — Daniele to fill in.]

**Offered topics**

| # | Title | Description |
|---|-------|-------------|
| DR-1 | *Topic title* | *Brief description — to be filled in by 5 June.* |
| DR-2 | *Topic title* | *Brief description.* |

---

### Francesco Caperna
*[Role] · [Research Group] · ETH Zurich*  
📧 [francesco.caperna@\[domain\]](mailto:francesco.caperna@[domain])

[Bio placeholder — Francesco to fill in.]

**Offered topics**

| # | Title | Description |
|---|-------|-------------|
| FC-1 | *Topic title* | *Brief description — to be filled in by 5 June.* |
| FC-2 | *Topic title* | *Brief description.* |

---

### Ghali Berbich
*[Role] · [Research Group] · ETH Zurich*  
📧 [ghali.berbich@\[domain\]](mailto:ghali.berbich@[domain])

[Bio placeholder — Ghali to fill in.]

**Offered topics**

| # | Title | Description |
|---|-------|-------------|
| GB-1 | *Topic title* | *Brief description — to be filled in by 5 June.* |
| GB-2 | *Topic title* | *Brief description.* |

---

### Syrmatenia Lampaki
*[Role] · [Research Group] · ETH Zurich*  
📧 [syrmatenia.lampaki@\[domain\]](mailto:syrmatenia.lampaki@[domain])

[Bio placeholder — Syrmatenia to fill in.]

**Offered topics**

| # | Title | Description |
|---|-------|-------------|
| SL-1 | *Topic title* | *Brief description — to be filled in by 5 June.* |
| SL-2 | *Topic title* | *Brief description.* |

---

## What makes a strong thesis

Strong theses in the MAS AID context typically:

- address a question that is technically grounded (not purely policy or market analysis)
- draw on methods and concepts from the MAS AID curriculum
- produce a concrete deliverable — an implemented system, empirical study, technical comparison, or similar artefact
- are scoped realistically for a part-time effort starting 1 July

TAs are happy to advise on scope during Path B affinity conversations, or by email for Path A topics.

---

## Contact

**Path A submissions** go directly to the individual TA whose topic you selected (see their section above).

**Path B proposals and general questions** go to Winston Rohmann (Head TA): [wrohmann@ethz.ch](mailto:wrohmann@ethz.ch) — Path B proposals sent here reach all TAs simultaneously.

> Do not email multiple TAs individually with the same submission. Only Path B group proposals are intended to reach all TAs at once.

---

*MAS ETH in AI and Digital Technology · [Department of Computer Science, ETH Zurich](https://inf.ethz.ch/) · [Repository, draw script & procedure](https://github.com/carloscotrini/mas-mt-hs26) · [drand randomness beacon](https://drand.love)*
