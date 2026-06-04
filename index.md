---
title: Master's Thesis — MAS ETH in AI and Digital Technology
layout: default
---

# Master's Thesis - MAS ETH in AI and Digital Technology

---

## About the thesis

The master's thesis is the capstone of the [MAS ETH in AI and Digital Technology](https://mas-aid.ethz.ch/masaid.html), offered by the Department of Computer Science (D-INFK) at ETH Zurich. It is undertaken in the final phase of the programme, after completing the three CAS components and the AI Project and Cyber Security courses.

Participants write an independent thesis on a topic of their choice that is relevant to their work or personal interest. The topic is freely selectable but must be approved by the thesis supervisor in advance. The final product must be sufficiently rigorous from a science and technology perspective and integrative of the skills developed throughout the programme — it can involve coding, empirical analysis, or system design, and may incorporate policy or market context, but cannot be purely non-technical.

Each thesis is co-supervised by one TA and Dr. Carlos Cotrini. The project description is submitted in myStudies and confirmed during the kick-off meeting (22–27 June). **Up to six theses** will be launched in this round, starting 1 July 2026.

---

## How topic selection works

Demand for thesis places typically exceeds the number of slots. To keep the process fair and transparent, places are awarded by a **publicly verifiable random draw** — nobody, not the TAs and not Carlos, can influence or predict who is selected, and anyone can re-check the result.

Each participant ends up sending **one email to the Head TA** proposing one thesis topic. There are two paths:

**Path A — Pick a topic from a TA's list.**

1. Browse the [TA sections](#teaching-assistants--topics) below and find a topic that interests you.
2. Email Winston [wrohmann@ethz.ch](mailto:wrohmann@ethz.ch) and the thesis TA in cc, quoting the topic title and a short statement of motivation.
3. You will receive an automatic **receipt** once the TA's acknowledge your email, followed by a **pool-entry confirmation** that includes your assigned submission id (a 16-character hex string). From that point your submission appears — by id and topic — in the public list at [`submissions/`](https://github.com/carloscotrini/mas-mt-hs26/tree/main/submissions).

**Path B — Propose your own idea.**

1. Draft a short proposal (title + a few sentences on motivation, expected methods, and deliverable) and email it to Winston [wrohmann@ethz.ch](mailto:wrohmann@ethz.ch).
2. One or more TA's may express interest. If interest is conditional, a brief affinity conversation follows so the TA can confirm you are a suitable candidate.
3. Your idea is added to the pool of candidates of one TA and you will then receive receipt and pool-entry confirmation as in Path A.

Both paths end with your name in that TA's selection pool. After the deadline each TA runs an independent draw over their own pool, using a shared public random seed. The rank-1 participant is offered the place; if they decline or do not respond within 48 hours, the offer rolls down to rank 2, then rank 3, and so on within the same TA's pool.

> **One submission only.** Each participant may enter only one pool with one submission. Withdraw by emailing the Head TA before 15 June 23:59.

---

## Selection procedure

The draw is implemented in [`selection.py`](https://github.com/carloscotrini/mas-mt-hs26/blob/main/selection.py) in the [public repository](https://github.com/carloscotrini/mas-mt-hs26). 

After the `draw` tag is published, anyone can audit the result:

```
pip install -r requirements.txt
python verify_draw.py
```

This recomputes the ranking from the frozen submissions and beacon, checks it against the published `result.json`, and verifies the drand cryptographic signature. Full details in [PROCEDURE.md](https://github.com/carloscotrini/mas-mt-hs26/blob/main/PROCEDURE.md).

---

## Key dates

| Date | Event |
|------|-------|
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
[ccarlos@inf.ethz.ch](mailto:ccarlos@inf.ethz.ch) · [people.inf.ethz.ch/ccarlos](https://people.inf.ethz.ch/ccarlos/)

Carlos is a lecturer at the Institute of Machine Learning at ETH Zurich. He holds a doctorate in information security from ETH Zurich, where he developed expertise in privacy-preserving machine learning and security analysis. His current research focuses on robust machine learning algorithms, privacy-preserving technologies, and educational methodologies.

---

## Teaching Assistants & Topics

### Winston Rohmann (Head TA)
[wrohmann@ethz.ch](mailto:wrohmann@ethz.ch)

Hi, as a mechanical engineer currently conducting his own master thesis at ETH and EMPA, I can provide you with research and topic related guidance. One of my last projects was to automate a quality control process and another one involved monte carlo simulations and machine learning. I am a teaching assistant at ETH for more than three years now, where I have also been a student since 2022, when I started my Bachelor's program. I am happy to support your own ideas and I am looking forward to the problem that we will explore together! Although theses are generally written in English, our meetings could be held in German.

**Offered topics**

| Title | Description |
|-------|-------------|
| Agentic AI for Stock Prediction: Can an LLM Trader Earn Enough to Pay for Itself? | During this thesis we would explore the finanical management capabilities of LLM's with a focus on automated information retrieval, prompt engineering and reasoning capabilities. |
| Comparing sovereign and open Swiss LLM Apertus to frontier models to identify potential pathways for corporations | Apertus was developed by the Swiss AI Initiative - a collaboration between EPFL, ETH Zurich, and CSCS - and represents a paradigm shift toward complete transparency in AI development, offering unprecedented access to training data, architecture details, and development processes. It is fully open: open weights, open data, and full training details including all data and training recipes. 
This thesis aims to explore the cutting edge of two converging forces: AI adoption in regulated industries and the sovereignty vs. capability tradeoff that every corporate board is now navigating.
 |

---

### Christina Tsakanika 
[ctsakanika@ethz.ch](mailto:ctsakanika@ethz.ch)

Hello, I'm Christina, currently pursuing an MSc in Electrical Engineering at ETH Zurich with a specialisation in Machine Learning, and working as a Teaching Assistant for Prof. Carlos Cotrini. I hold an integrated BSc & MSc in Computer Science from the National Technical University of Athens, and I have professional experience of 3 years as a software and data engineer. I enjoy collaborating with students, exchanging ideas, exploring different implementation approaches, and working together toward a thesis that delivers a meaningful result! 

**Offered topics**

| Title | Description |
|-------|-------------|
| *Topic title* | *Brief description — to be filled in by 5 June.* |
| *Topic title* | *Brief description.* |

---

### Daniele Russica
[drussica@ethz.ch](mailto:drussica@ethz.ch)

Hi, I'm Daniele, currently pursuing a Master in Data Science at ETH Zurich. I hold a Bachelor in Computer Science and Engineering. Past projects I've contributed to range from business automation for a real SME, to GPU acceleration of retrieval methods for approximate nearest-neighbour search, to deep model-based reinforcement learning. I'm interested in probabilistic AI modelling, agentic systems, and model deployment in real-world settings. I'd be happy to discuss your own ideas or any of the topics below — feel free to reach out!

**Offered topics**

| Title | Description |
|-------|-------------|
| *Topic title* | *Brief description — to be filled in by 5 June.* |
| *Topic title* | *Brief description.* |

---

### Francesco Caperna
[fcaperna@ethz.ch](mailto:fcaperna@ethz.ch)

Hi, my academic background is in Mathematics and AI. My main interests include LLMs (including security), explainability, Topological Data Analysis, Reinforcement Learning, Agentic AI, Graph Neural Networks and the development of ML models for both scientific research and real-world decision-making.
I am proposing two example thesis directions: the first is more research-oriented, while the second is more applied and business-oriented. These are initial draft ideas and I would be happy to adapt them depending on the student’s interests or to discuss other possible ideas.
If you are interested, please feel free to contact me by email.

**Ideas of topics**

| Title | Description |
|---|---|
| **Interpretable AI in Cancer Research** | In this thesis, we would explore how interpretable AI can support biomedical insight discovery in cancer drug response analysis. Building on my previous work on predicting treatment response in cancer cell lines, the project would focus on using machine learning model explanations to identify which samples or drugs behave similarly and why. The goal would be to construct explanation-based graphs that may reveal patterns linked to drug sensitivity, resistance, and potential biomarkers. |
| **From High-Dimensional Customer Profiles to LLM Inputs** | In this thesis, we would explore how complex, high-dimensional customer profiles can be summarized into compact, structured inputs for LLMs. The project would combine machine learning and interpretability techniques to identify the key drivers behind individual customer outcomes and translate them into structured representations. These representations would enable LLMs to generate better personalized recommendations or next-best actions. |


---

### Ghali Berbich
[ghali.berbich@ethz.ch](mailto:ghali.berbich@ethz.ch)

Hi, I'm Ghali, I am a master's student in Computer Science specializing in machine learning. I did my bachelor's in Computer Science and Math and my bachelor thesis was on multimodal generative transformers for video generation. I'm mainly into ML, LLMs and large scale AI but also find the intersections with finance and social sciences pretty interesting. I would be happy to discuss and align on something that fits what you want to explore and covers themes you actually care about. Feel free to reach out!

**Offered topics**

| Title | Description |
|-------|-------------|
| From context limits to organisational substitution: benchmarking LLMs for enterprise roles| LLMs are being deployed across businesses but it remains unclear what they can actually replace and why. This thesis takes a unified approach: benchmarking RAG, fine-tuning and long-context strategies on enterprise tasks stratified by cognitive demand, while grounding the results in what context window size fundamentally constrains mathematically and architecturally. The output is both a practical benchmark and a framework mapping current LLM capabilities onto organisational roles, from routine task execution up to strategic coordination. |
| *Topic title* | *Brief description.* |

---

### Syrmatenia Lampaki 
[slampaki@ethz.ch](mailto:slampaki@ethz.ch)

Currently pursuing a Master's in Physics at ETH Zurich, following an integrated Master's degree in Electrical and Computer Engineering. My research interests lie at the intersection of machine learning, explainable AI, mathematical neuroscience and neuroinformatics, with a particular emphasis on mathematical approaches and on meaningful real-world relevance in medicine and beyond. Starting from the proposal, there is room to reshape the project together depending on your own interests and ideas. I look forward to working on a problem that brings together theoretical depth and real-world relevance, and to the shared learning that naturally comes with exploring it together.

**Offered topics**

| Title | Description |
|-------|-------------|
| *Topic title* | *Brief description — to be filled in by 5 June.* |
| *Topic title* | *Brief description.* |

---

## What makes a strong thesis

Strong theses in the MAS AID context typically:

- address a question that is technically grounded (not purely policy or market analysis)
- draw on methods and concepts from the MAS AID curriculum
- produce a concrete deliverable — an implemented system, empirical study, technical comparison, or similar artefact
- are scoped realistically for a part-time effort starting 1 July

---

## Contact

**General questions** go to Winston Rohmann: [wrohmann@ethz.ch](mailto:wrohmann@ethz.ch).

---

*MAS ETH in AI and Digital Technology · [Department of Computer Science, ETH Zurich](https://inf.ethz.ch/)*
