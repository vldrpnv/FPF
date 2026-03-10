# First Principles Framework (FPF) — Core Conceptual Specification

> **An Operating System for Thought**  
> *Architecting transdisciplinary reasoning for systems, epistemes, and communities.*

**Version:** March 2026  
**Author:** Anatoly Levenchuk (with LLM assistance)  
**Status:** Normative kernel, "eternal alpha" — already used in working projects and increasingly acting in working development programmes, while still evolving.

## 📖 Overview

The **First Principles Framework (FPF)** is a rigorous, transdisciplinary architecture for thinking, written in human- and machine-readable pseudo-code (the informal "language of technical standards" with multiple "May", "Should", "Must"). It provides a generative pattern language to model complex systems, manage knowledge evolution, and ensure auditable assurance across engineering, research, and management domains. Internally, FPF also serves as a conceptual data schema for rational work that you look at, resonate with, and mine for patterns rather than a narrative textbook. 

FPF is not a specific methodology (like Agile or Waterfall) nor a static encyclopedia. It is an **episteme of method** — a structured specification of how to think — packaged as a set of architecture decision records (ADRs) and patterns that can be executed by humans and LLMs and consumed as pseudo-code by LLMs. It bridges the gap between **rigorous assurance** (audits, proofs) and **open-ended creativity** (innovation, novelty) by treating them as complementary engines within a single evolution.

FPF is not mainly a way to make a single model “smarter”. Its main value is to turn raw intelligence — human or machine — into organisationally usable reasoning: explicit bounded contexts, auditable artefacts, multi-view descriptions, and disciplined hand-offs between specialised actors. In practice this matters most when work is done by mixed collectives of humans and AI agents, not by one isolated expert. Its first-principles kernel is meant not only to catalogue current best practice, but also to help grow new conceptual architectures when existing categories stop being adequate.

FPF is a file (around 4MB, 50000 lines) and should be added only as a file (to the RAG), not pasted into the prompt window. Use it with a prompt in your preferred language, for example: “You have FPF in a file. Use it, but avoid FPF-specific terminology in the final answer. Speak as an engineer-manager and propose bounded contexts / decision criteria / alternatives / hand-offs when useful.”

### Why FPF when LLMs keep getting stronger?

* **Because coordination, not raw generation, becomes the bottleneck.** Stronger LLMs reduce local reasoning scarcity, but they do not remove the need for selection, auditability, safe delegation, and shared understanding across people, agents, time, and viewpoints.
* **Because `U.BoundedContext` is the unit of specialisation and hand-off.** It lets a very capable but specialised human/agent participate in a larger engineering or research process without pretending everyone shares one universal vocabulary.
* **Because many real projects cannot just “loop until tests pass.”** In product, field engineering, strategy, marketing, safety, or open-ended research, the real-world oracle is delayed, noisy, expensive, or risky. FPF aims to catch anti-patterns before contact with the world.
* **Because the same stack can serve both humans and AI.** AI agents can read the specification directly; humans can learn the same working model through didactic layers and the pedagogical companion.
* **Because FPF pays off past a complexity frontier.** It matters most when the problem becomes simultaneously compositional, collaborative, temporal, assurance-heavy, and generative.
 

### 🧠 FPF as an "Operating System for Thought"

Using the OS metaphor:

* **Runs "applications of thought".** FPF provides a canonical reasoning cycle (abduction–deduction–induction, `B.5`) and a canonical evolution cycle (`B.4`) that act as a generic *runtime* for research and engineering tasks.
* **Isolates processes and manages their interaction.** `U.BoundedContext` gives an "address space of meaning" and becomes the unit of specialisation, delegation, and semantic process isolation. Alignment bridges, congruence levels, and Concept-Set tables (`F.9`, `F.17`) define controlled hand-offs between contexts instead of global terminology soup.
* **Supports heterogeneous collectives.** The same context / bridge / publication machinery can coordinate human teams, specialised AI agents, and software services: each works locally, while cross-context exchange stays explicit and auditable.
* **Creates and terminates thought processes.** The holon → role → method → work chain makes "a process of thinking" explicit: from intention, through role assignment and method choice, to concrete Work records.
* **Manages memory and protects meaning.** `U.BoundedContext`, Evidence Graphs and context passports keep track of *where* statements hold, under which editions and planes, so that reasoning remains auditable instead of becoming folklore. 
* **Prepares resource management.** `Γ_work` (Gamma, composition operator) and the planned Resrc-CAL describe how time, money, energy, and other resources flow through work streams.
* **Provides a "conceptual file system" and I/O.** Cards, tables, records (RSR/RSCR, F-cluster) are the conceptual "files" and journals through which thinking interacts with the world, independently of any specific notation or tool. This is how FPF supports "thinking by modelling": you externalise thought into structured artefacts instead of keeping everything in your head, and can publish the same underlying work to engineers, managers, researchers, or auditors through different surfaces. 
* **Uses an extendable architecture.** At the core is a minimal transdisciplinary set of types and Γ-operators; domain-specific calculi, logics, CHR-packs and SoTA-packs (`Part C`, `Part G`) plug in like drivers and services above the kernel.

Loaded as a file into a RAG-enabled AI assistant (ChatGPT, Gemini, local models, etc.), FPF can act as a *bias-assistant* or “grimoire”, but that understates the point: it is better understood as a coordination and reasoning scaffold for mixed human/AI work. It steers the model toward first-principles, SoTA-oriented reasoning instead of generic marketing/management/pop-psychology boilerplate — but it will not think instead of you, and without good questions you can still get very confident, well-structured nonsense.

## 🎯 Who is this for?

*   **Engineers and systems engineers** building reliable physical or cyber-physical systems (`U.System`).
*   **Researchers** constructing trustworthy knowledge and theories (`U.Episteme`).
*   **Platform teams** designing AI-agent / human-in-the-loop work systems.
*   **Safety, assurance, and regulatory leads** who need auditable boundaries, evidence, and controlled delegation.
*   **Managers and product leaders** orchestrating collective intelligence, budgets, and evolutionary cycles.

## 🔑 Key Concepts & Commitments

FPF is built on a small kernel of non-negotiable "zero and first principles". If you are new, start with these core ideas, but they are not needed to use FPF; they are here mainly to explain what is inside:

1.  **Holonic Foundation (`A.1`):** Everything is a `U.Holon`—simultaneously a whole and a part. We strictly distinguish between physical actors (**Systems**) and knowledge artifacts (**Epistemes**).
2.  **Contextual Meaning (`A.1.1`, `F.0.1`):** Meaning is local. A term like "Service" or "Process" is defined strictly within a `U.BoundedContext`. Cross-context communication happens only via explicit **Bridges** with declared translation loss. In practice, a bounded context becomes the unit of specialisation, delegation, and safe integration in mixed human/AI work.
3.  **Strict Distinction (`A.7`):** We never confuse the map with the territory.
    *   **Role** (Assignment/Mask) $\neq$ **Method** (Recipe) $\neq$ **Work** (Execution/Occurrence).
    *   Documents do not "act"; only Systems enact Work.
4.  **Trust & Assurance Calculus (`B.3`):** Trust is not a feeling; it is a computed tuple **$\langle F, G, R \rangle$**:
    *   **F (Formality):** How rigorously is it expressed?
    *   **G (Claim Scope):** Where does it apply? (Set-valued over context slices).
    *   **R (Reliability):** How well is it supported by evidence?
5.  **Evolution & Creativity (`B.4`, `C.18`):** Systems must evolve. FPF operationalizes the "Bitter Lesson" by favoring general, scalable search methods (**NQD**: Novelty-Quality-Diversity) over hand-tuned heuristics, governed by explicit **Explore-Exploit policies**.
6.  **Universal Aggregation ($\Gamma$):** A single algebra (`B.1`) governs how parts combine into wholes, ensuring invariants like "Weakest-Link" reliability are preserved across scales.
7.  **First-Principles Generativity:** FPF is not only a catalogue of current SoTA. It tries to encode a small kernel of universal, falsifiable, cross-domain commitments from which new abstractions, discipline packs, and engineering architectures can be grown.

## ✅ What to expect (and what not to expect)

### Reasonable expectations

* **A SoTA- and first-principles-biased co-thinker.** When loaded into an LLM, FPF acts as a bias-assistant for strong engineering and research thinking: you still think, but you get sharper questions, better comparisons, and far less generic boilerplate.
* **A coordination fabric for mixed human/AI teams.** FPF helps specialised people and agents participate in one engineering/research process through bounded contexts, bridges, shared artefacts, and multi-view publication surfaces.
* **A DDD-style backbone for disciplines and organisations.** FPF can serve as the *DDD (domain-driven design) for science/engineering*: a way to model a discipline (or organisation) with explicit contexts, roles, calculi, and SoTA-packs rather than one more methodology slide-deck.
* **A machine for first-principles synthesis.** Use it not only to recall current best practice, but to grow new conceptual architectures when existing categories are misleading.
* **A kernel for development programmes.** In practice FPF already feeds programmes for engineer-manager development and research skill-building.

### Unreasonable expectations

* **"I'll just read it once and form my opinion."** The spec reads like OS source code, not like a popular book; it is meant to be *used* with tools, not consumed in one sitting.
* **"This is a plug-and-play tool for all work projects."** Today FPF is a research-grade framework that already helps in real projects as an MVP, but it is not yet a shrink-wrapped product; you still need to adapt, localise, and extend it for your discipline and organisation.
* **"It works without good framing and always gives the right answer."** LLM+FPF will not think instead of you. Without good questions, explicit problem frames, and minimal rational literacy you can still get confident nonsense—just more structured nonsense.
* **"A stronger AGI/LLM makes FPF unnecessary."** As models get stronger, the bottleneck often moves from local reasoning to coordination, selection, safe delegation, and cross-role auditability.
* **"Adoption should be decided only by transferable benchmark wins from other organisations."** Frameworks such as Agile or Copilot-like practices are often adopted as architectural bets under high variation. FPF is similar: the justification is usually logical fit to your coordination/problem structure, not a neat benchmark that transfers unchanged across organisations.
* **"If I ignore first principles, FPF will fix everything."** FPF amplifies whatever style of thinking you bring: if you use it to chase fashion, it will help you catalog fashion; if you use it to chase first principles, it will help you do that more systematically.


## 📂 Repository Structure

The specification is divided into clusters of patterns (think about it as source code for an evolvable reasoning architecture rather than a traditional expert system; you do not need to read all of it to use FPF):

### **Part A: Kernel Architecture Cluster**
The immutable ontological core.
*   **Ontology:** Holons, Systems, Epistemes, and Bounded Contexts.
*   **Transformation:** The `Transformer` quartet (Agent, Method, Description, Work).
*   **State Space:** Characteristics, Scales, and Dynamics.

### **Part B: Trans-disciplinary Reasoning Cluster**
The logic of composition and trust.
*   **$\Gamma$ Algebra:** How to aggregate systems (`Γ_sys`), knowledge (`Γ_epist`), and resources (`Γ_work`).
*   **Assurance:** The `F-G-R` calculus and evidence graphs.
*   **Transduction Graph Architecture (E.TGA):** Eulerian graphs of flows and "from principles to work" (P2W) paths that make architectures of reasoning and work explicit.
*   **Evolution:** The canonical loops for observing, refining, and deploying updates.

### **Part C: Architheory Specifications**
Pluggable domain-specific calculi (CAL), logics (LOG), and characterizations (CHR).
*   **Sys-CAL:** Physics and conservation laws.
*   **KD-CAL:** Knowledge dynamics and truth-maintenance.
*   **NQD-CAL:** Novelty, Quality, and Diversity search.
*   **Kind-CAL:** Typed reasoning and taxonomy.

### **Part D: Ethics & Conflict-Optimisation**
*   Multi-scale ethics (from agent to planetary).
*   Bias audits and trust-aware mediation.

### **Part E: Constitution & Authoring**
The governance of the framework itself.
*   **The 11 Pillars:** Constitutional invariants (e.g., *Cognitive Elegance*, *Didactic Primacy*).
*   **Guard-Rails:** DevOps Lexical Firewall, Notational Independence.
*   **MVPK:** Multi-View Publication Kit for generating consistent views/documents for different roles and surfaces.

### **Part F: The Unification Suite**
Techniques for aligning vocabularies across disciplines and specialised agents using **SenseCells**, **Concept-Sets**, and **Alignment Bridges**.

### **Part G: Discipline SoTA Kit**
Tools for harvesting "State of the Art" (SoTA) knowledge, benchmarking methods, and creating selector-ready portfolios of solutions rather than prematurely collapsing to a single winner.

> *"A principle that works in only one world is local folklore; a first principle architects every world."* — **Pattern A.8**

## 🚀 Using FPF within LLM environment (Worked Prompt Examples)

FPF is designed to be loaded as a file into an AI assistant with LLM and RAG (ChatGPT, Gemini, local models with RAG, etc.). It is too large to paste as a prompt, so load it as a file. Then ask the model to think with you about concrete projects. The highest-leverage use is not to request generic essays, but to make the model externalise reasoning into bounded contexts, term sheets, decision criteria, alternative portfolios, P2W chains, gates, and multi-view artefacts. There is no magic prompt library for FPF: what matters is your ability to have a rational conversation with the model about real problems, not memorise incantations. LLM+FPF will not solve everything automatically: you remain the principal, and the model is an agent that follows your problem framing and constraints. Start with something like: “You have the FPF specification as a file. Use it, but avoid FPF-specific terminology in the final answer. Speak as an engineer-manager.”

In practice the most productive usage is to treat FPF as a grimoire/design kit: ask for concrete name cards, bounded-context maps, chains of thought, patterns, UTS blocks, P2W paths, Q-bundles, decision gates, and hand-off artefacts for your domain, then iterate.

Below are example prompts that have been used in practice; adapt them to your domain and language.

### 1. Characterisation & indicators for a new project

**Goal:** get a step-by-step chain from “vague idea” to measurable characteristics, indicators, scoring and decision criteria.
**Prompt:** 
> You have the FPF specification loaded as a file.  
> We are starting work on <brief description of project>, design has not yet begun.  
> Propose a step-by-step chain for characterising the objects of our project, normalising measurements, defining indicators, scoring alternatives, and choosing design decisions.  
> Include steps that I may have forgotten.  
> Write in the language of engineer-managers, not in FPF jargon.*

Typical follow-ups:
* “Now take object <X> from this chain and work it through in detail: list 10–15 characteristics, their scales, indicators, and a rough dashboard format for decision-makers.”
* “Show how this chain maps to P2W in E.TGA for this project.”

### 2. UTS (Unified Term Sheet) for a domain

**Goal:** build a disciplined vocabulary for a niche field using FPF Part F.
**Prompt:**
> You have the FPF specification loaded.  
> Produce a Unified Term Sheet (UTS) block for the core terms of <your domain>: at least 10 rows.  
> Use F.17 and F.18: distinguish Tech vs Plain names, show SenseCells for 2–3 key bounded contexts, and flag risky aliases.

Follow-up for quantitative structure:
* “For the same domain, propose a Q-bundle that captures the quality of <your object/process> and produce a UTS block for its characteristics (CHR) and indicators.”

### 3. Naming via F.18 (Name Cards)

**Goal:** design better names for roles, programs, artefacts when existing labels are misleading.
**Prompt:**
> Using F.18, develop a complete Name Card for what to call <current name of an Entity> in the following situation:  
> <short narrative of current practice and complaints about existing name>  
> Do not assume current names are correct; perform an honest search on the local Pareto-front of candidate names and explain trade-offs.

### 4. P2W (from principles to work) paths with E.TGA

**Goal:** make “from principles to work” explicit for a concrete project.
**Prompt:**
> Using E.TGA and TEVB, unpack the canonical P2W flow for my situation <describe your project>.  
> Give the list of nodes (P1…Pn), their Kinds, and explain each node in engineer-manager language.

Follow-up:
* “Now build a mini Flow specification table for this P2W graph”.

### 5. Mixed human/AI bounded contexts and hand-offs

**Goal:** turn a set of people, copilots, and specialised agents into a disciplined work architecture.
**Prompt:**
> We have the FPF specification loaded as a file.  
> We need to organise a mixed team of humans and AI agents for <project/programme>.  
> Propose a bounded-context map: contexts, local vocabularies, roles, bridges, hand-off artefacts, decision gates, and where human approval is required.  
> Keep the final answer practical for engineers/managers and avoid FPF jargon.

Typical follow-ups:
* “Now define autonomy budgets, allowed tools, escalation paths, and publication surfaces for each context/agent.”
* “Show which bridges are high-risk because translation loss or ambiguity is likely.”

### 6. SoTA harvesting & discipline packs

**Goal:** use Part G to organise a frontier discipline around first principles.
**Prompt:**
> We are in search for SoTA of <discipline>.
> Using G.2 and G.4, extract: (a) TraditionCards for competing schools of thought; (b) OperatorCards for their main operators / update rules; (c) a first draft of a SoTA Pack and selector-ready portfolio. This is expected to be a long text, therefore start with only TraditionCards.
