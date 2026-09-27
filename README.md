# How I work with AI

**Status: work in progress.** Version 0.1, 27 September 2026. A personal note about my own practice; it does not speak for my employer. It will change, and the git history keeps every version.

I work in information management: data, documents, and the systems that hold them. This page explains how tools built on large language models (LLMs) fit into that work, what happens to what you send me, and what you can ask me to do differently. It exists so that the answer to "was this written with an AI?" is public, dated and versioned, rather than reconstructed after the fact.

## In short

- LLM-based tools are part of my daily work: drafting, analysis, code, data structures, working notes.
- What you send me (emails, documents, data extracts) may pass through these tools and be summarised in my working notes.
- I read and sign off everything I send. Nothing goes out without me.
- Personal data about the people my organisation serves stays out of these tools; see the safeguards, and their limits, below.
- You can set your preferences at any time (no LLM on what you send me, no LLM-drafted replies, nothing kept in my notes): use the preference form linked from my email signature, or reply to one of my emails.

## How I see it

I think of information management as a craft. The tools are the power tools of the workshop: they cut faster and straighter than I do by hand, but they do not decide what to build, for whom, or whether the piece is good enough to leave the shop. That decision, and the responsibility that goes with it, stays with me.

In practice I work less like a writer with an assistant and more like the manager of a small team of agents: I brief them, I review, I send work back, I write down the rules they must follow next time.

And I mix. I rarely take one output as it comes. Like a DJ, I combine drafts from several models and agents, cut what is weak, re-sequence, and finish by hand. The result is mine, even when most of the words were first typed by a machine.

## Why say it at all

Two reasons. Transparency: if a tool helps me write to you, you should know. Accountability: writing it down, with a date, is cheaper than explaining it later.

A third, more personal one. I edit my texts against a style guide that removes the usual marks of machine writing. Without this page, that could look like concealment. With it, it is a matter of style.

## The tools

| Tool | Provider | What I use it for | Contract and training setting | Provider policy |
|---|---|---|---|---|
| Claude (Claude Code, claude.ai) | Anthropic | Drafting, document and data analysis, code, forms, dashboards, agents that keep my working notes | To confirm: type of offer, and whether my content may be used for training. I will state it here once verified. | [Anthropic privacy policy](https://www.anthropic.com/legal/privacy) · [Privacy center](https://privacy.claude.com/) |
| Codex | OpenAI | Same tasks; second opinion on code and structure | To confirm, same as above. | [OpenAI privacy policy](https://openai.com/policies/privacy-policy) |
| Microsoft Copilot | Microsoft, inside my employer's Microsoft 365 tenant | Email, meeting notes, Office documents | Enterprise contract. Microsoft states that prompts, responses and data accessed through Microsoft Graph are not used to train its foundation models. | [Data, privacy and security for Microsoft Copilot](https://learn.microsoft.com/en-us/microsoft-365/copilot/microsoft-365-copilot-privacy) |

Other tools may appear for a specific task (speech to text, translation). I will add them here when they become part of the routine.

## What the tools do

- Draft: emails, reports, guides, presentations, this page.
- Analyse: read a document or a data export and answer my questions about it; profile a dataset; compare versions.
- Build: data collection forms, scripts, data pipelines, dashboards.
- Remember: keep my working notes up to date (see "What is kept").
- Check: review a form, a script or a dashboard against my organisation's standards before I release it.

## What I do

1. **Brief.** I frame each request: context, constraints, expected output. For complex work the tool proposes a plan first, and I approve or change it before anything is built.
2. **Demand sources.** The tools must cite what they read. A claim without a source is not accepted, and "verify before asserting" is one of the written rules they load at every session.
3. **Iterate.** I correct, the tool revises. For critical outputs (a data collection form going to an operational team, a published dashboard), a second agent with no memory of the drafting reviews the result.
4. **Test.** Forms and data pipelines run on a test server with synthetic data before they touch production.
5. **Review and sign.** I read everything before it leaves: emails (the tools can prepare a draft in my mailbox, never send), documents, forms, dashboards. One nuance, for honesty: once I have approved a dashboard design, the tool may publish, check and correct several iterations on its own in my organisation's BI workspace. I review the result before anyone else sees it.
6. **Write the rule.** Each mistake becomes a written rule that the tools load at the start of every session. Over time, the rules are the method.

## What may be processed

- Emails and messages you send me, and attachments I open.
- Working documents: questionnaires, forms, data exports, reports, meeting notes, proposals.
- Structure and metadata of the systems I administer (data collection platform, data warehouse, BI): field names, counts, logs.
- My own working notes.

What stays out, as a rule: see "Sensitive data".

## What is kept: three different things

People often merge these. They are not the same.

1. **My working notes.** Files in my work environment, sometimes called my "vault". At the start of a session the tools read them to recover context: which projects are open, what was decided, what comes next. An exchange with you may end up there as a short summary: who asked what, the decision, the next step. These notes contain no personal data about the people my organisation serves. Nobody else reads them. When a tool loads them, they travel to the provider like any other conversation content (see points 2 and 3). If you ask, I will tell you what they say about you.
2. **Conversation history at the provider.** Depending on the product and its settings, the provider may keep a copy of my conversations to run the service. The retention rules are the provider's; see the links in the table.
3. **Model training.** A separate question from retention. Whether a provider may use my content to improve its models depends on the contract and on settings I control. I will state the position for each tool in the table above once verified.

## Sensitive data

What never goes into these tools:

- Personal data about the people my organisation serves (case files, names, contact details, health information). When I work on such systems, I use test servers, synthetic records, or exports stripped of identifying fields.
- Passwords, keys, tokens.
- HR and finance data about identified colleagues.
- Documents a partner or a funder marked confidential.

How I enforce it: test environments by default; written rules, loaded at every session, that forbid displaying or noting such data; scripts that pass structure (field names, counts) rather than content; a check of what the tools wrote to my notes when I close a session.

When a safeguard fails: I record the incident, fix the tooling or the rule that let it through, and inform my organisation's data protection officer if personal data is involved.

## Your options

**Set your preferences.** Use the preference form linked from my email signature, or reply to any of my emails and say so. You can ask me, in any combination:

- not to submit the content you send me to external LLM tools: I will handle our exchanges by hand;
- not to send you content generated or drafted with LLMs;
- not to keep what you write to me, or summaries of it, in my working notes.

You can also ask me what my working notes say about you. I will confirm by email once your choice is applied.

What a request cannot change: what was processed before I received it, and copies the providers already hold under their own retention rules. In those cases, ask me and I will tell you what I know and what I can delete.

**Questions or concerns.** Write to me. On request, I will give you the contact of my organisation's data protection officer.

## Reuse

You are welcome to copy this page for your own transparency note. A link back is appreciated, not required.

## Changes

- 2026-09-27, v0.1: first draft.

---

## Résumé en français

Cette page explique comment des outils fondés sur des grands modèles de langage (LLM) entrent dans mon travail de gestion de l'information. Note personnelle, en cours de rédaction ; elle n'engage pas mon employeur.

- Ces outils (Claude, Codex, Microsoft Copilot) font partie de mon travail quotidien : rédaction, analyse, code, formulaires, tableaux de bord, notes de travail.
- Ce que vous m'envoyez peut passer par ces outils et être résumé dans mes notes de travail. Ces notes sont des fichiers de mon environnement de travail, lus par les outils en début de session ; ce n'est ni la mémoire du modèle, ni son entraînement.
- Je relis et j'assume tout ce que j'envoie. Rien ne part sans moi.
- Les données personnelles des personnes que mon organisation accompagne n'entrent pas dans ces outils ; je travaille sur des serveurs de test et des données synthétiques.
- Vous pouvez à tout moment garder vos messages en dehors : le formulaire de préférence lié depuis ma signature de mail, ou une réponse à l'un de mes mails. Vous pouvez aussi me demander ce que mes notes disent de vous.

Je vois ce métier comme un artisanat : les outils sont les machines de l'atelier, elles ne décident ni quoi construire, ni si la pièce peut sortir. Je travaille comme le chef d'une petite équipe d'agents : je cadre, je relis, je renvoie, j'écris la règle pour la fois suivante. Et je mixe, comme un DJ : je prends rarement une sortie telle quelle, je combine, je coupe, je finis à la main.
