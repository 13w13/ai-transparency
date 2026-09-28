# How I work with AI

*Work in progress. Version 0.3, 28 September 2026. A personal note about my own practice; it does not speak for my employer.*

I work in information management: the data an organisation collects, and the tools and systems around it. A large share of that work now goes through AI tools, mostly agents that can work directly on my files and on the systems I look after. I would rather say so plainly than leave anyone guessing. This page describes how I work with these tools, what I keep for myself, and why.

## Where my time goes now

In my experience, information management has long meant producing things: data collection forms, cleaning scripts, databases, dashboards, and the documentation that goes with them. Agents have made that production cheap. A script that took a day takes an hour. A first version of a dashboard takes an afternoon. Agents read several hundred pages of vendor documentation in minutes.

What has not become cheap is everything around the production. Knowing what a team actually needs. Agreeing on what a number means before anyone draws it. Checking that the figure on the screen matches what happened on the ground. Building something a team can run without me, and helping the people who will use it get comfortable with it.

That is where I try to put my hours now. For me, the gain from these tools is time, moved from producing to the parts of the job that need a person.

The tools help with the thinking too, and not only with the making. I brainstorm with an agent, ask it to challenge a plan or to test a method against published standards, and use it to reflect on how this job is changing. This page started as one of those conversations.

Two things keep me honest. The first is attention. The limit is rarely the speed of the tools; it is how much I can read and check, and reading is the one step I cannot hand over. The second is the temptation to polish. When building is cheap, it is easy to perfect the wrong thing. I once watched a dashboard go through seven mock-ups before we noticed that its headline figure was off by a factor of more than three: the counting rule had never been agreed with the person who owned it. Speed had hidden the question. Since then, definitions come first and visuals after.

## Like a DJ

The image I keep coming back to is a DJ. A DJ does not play every instrument. They know their records, choose what fits the room, cue the next track while the current one plays, cut what drags, and keep an eye on the crowd.

My records are different models and agents, several working sessions running side by side, vendor documentation, community tools, what colleagues know, and the data itself. I rarely take one output as it comes. I combine drafts, keep the strongest parts, change the order, and finish by hand. The crowd is the people the work is for: if it does not land with them, the mix was wrong, however clever it sounded.

Information management is also a craft, and on some days the agents feel like the power tools of a workshop: faster and straighter than my hands, with no opinion on what to build. On other days it feels like managing a small team. I brief, I review, I send work back, and I write down what should change next time. Either way, the set has my name on it.

## How a piece of work gets made

It starts with context. When I open a session, the agent is handed a short brief on where my projects stand and what happened in the last sessions, so we pick up where we left off.

Then I describe the problem the way I would brief a colleague, sometimes by voice, often in rough notes. For complex work, the agent comes back with a plan first, and I approve or change it before anything is built.

The work then fans out. The main agent sends helpers to read documentation or search past projects, and they come back with conclusions and their sources rather than raw dumps. On larger pieces, several sessions run in parallel, each on its own track.

Everything is built against reality. Forms, data pipelines and dashboards are made first in a test environment, with synthetic data or a faithful copy, then checked where they will actually live: on an emulated phone, or against the server's own answer. "It should work" is not a result.

Then come fresh eyes. For forms, dashboards, BI code and scripts, a separate reviewer agent, which knows nothing of how the thing was made, scores the work against our standards, and corrections come in waves. Then I review. Anything addressed to a person goes out after I have read it; emails, for instance, are prepared as drafts that I send myself. Once I have approved a direction, some technical loops run on their own, such as publishing a draft dashboard to an internal workspace, exporting its pages, looking at them, fixing and repeating. I look at the result before I share it.

Sessions end with notes on what was decided and what comes next. Local copies that hold personal data are kept only as long as the project needs them, then deleted.

And every mistake becomes a rule: a few lines, dated, with the story of what went wrong. There are about sixty of them now, and the agent reads them at the start of every session. Over time the rules have become the method, and they are probably the most useful thing I have built.

## The setup

Nothing exotic, and mostly plain text. A working memory (an index, one file per project, a session log and a "where we left off" note), the rules, and 26 skills, which are packaged procedures for recurring jobs such as building a data collection form, designing a dashboard, analysing a dataset or writing a document in the house style. One copy of the skills is shared by two different agent tools. Five reviewer agents each have a narrow brief. Connectors reach the systems I administer, and the agent can drive a browser and a phone emulator when it needs to see what a user would see.

## What stays with me

Deciding what to build and when to stop. Agreeing definitions with the people who own them. Reading everything that goes out to a person. Answering for the result, whoever typed the first draft. And the time with people, explaining and training, which is where the hours saved by the tools should go.

## The tools

| Tool | Provider | Part in my work |
|---|---|---|
| Claude, mainly through Claude Code | Anthropic | Main working environment: agents, code, analysis, drafting, working notes |
| Codex | OpenAI | A second agent tool, using the same skills |
| Microsoft Copilot | Microsoft, within my employer's Microsoft 365 | Questions over internal documents, and assistants built on them |

I use more than one model and switch between them depending on the job. Provider policies: [Anthropic](https://code.claude.com/docs/en/data-usage), [OpenAI](https://help.openai.com/en/articles/5722486-how-your-data-is-used-to-improve-model-performance), [Microsoft Copilot](https://learn.microsoft.com/en-us/microsoft-365/copilot/microsoft-365-copilot-privacy).

## What happens to information

My working notes live in my work environment. The agent reads them to pick up context: which projects are open, what was decided, what comes next, who asked for what. Nobody else reads them.

What the providers do with what the agent sends them:

- **To answer**, every message goes to the provider's servers, notes included.
- **Training**: I turn it off wherever I can. OpenAI trains on personal accounts by default (Codex has a second switch); business plans and Microsoft Copilot don't train on your data.
- **Safety**: automated systems scan conversations; flagged ones can be kept for up to two years at Anthropic.
- **Research and ads**: Anthropic studies usage in aggregate, read by a model rather than by people. ChatGPT's Free and Go plans show ads matched to the conversation; paid plans don't, and Claude has no ads.
- **Retention**: 30 days for Claude with training off; longer for feedback, flagged content or a court order (in 2025 a US court made OpenAI keep deleted chats for months).
- **Profiling**: turning training off doesn't stop it. Providers log account, device and usage data and build a profile of the account holder, meaning me (memory, and at OpenAI, age estimation). Research also shows these models can infer personal traits such as location, income or age from ordinary text.

Training is the step that matters most. European regulators consider that a model trained on personal data is not anonymous by default: it can memorise, and fragments can be extracted through queries ([EDPB, 2024](https://www.edpb.europa.eu/documents/opinion-of-the-board-art-64/opinion-282024-on-certain-data-protection-aspects-related-to_en); [CNIL, 2025](https://cnil.fr/fr/ia-analyser-le-statut-dun-modele-dia-au-regard-du-rgpd)). That is why I switch it off wherever I can.

The line I watch most is personal data about the people my organisation serves. When the work touches it, the agent handles it through scripts that report structure and counts rather than content, on test servers or local copies wherever possible, and none of it goes into my notes. Passwords and keys are kept out of my notes and prompts; most live in the operating system's credential store. The system is not perfect: when a safeguard fails, I record it, fix the rule that let it through, and tell my organisation's data protection officer if personal data was involved.

## What I'm uneasy about

These tools are not neutral on authors' rights. They were built by vacuuming up a huge share of humanity's written knowledge, often without the authors' consent, turning that common knowledge into private products. Rules are arriving (Anthropic agreed to pay $1.5 billion to the authors of pirated books; the EU AI Act now requires model providers to respect authors' opt-outs and publish a summary of their training data), but the question is far from closed. I use the tools anyway, because I think we need to master them to use them for good, and I don't consider the question settled.

Who checks what the providers promise? No one in real time. Auditors review their processes, and regulators and courts step in after the fact. What I can check is my own settings and what I choose to send.

I would like to move to open models running on my own machine, so that nothing leaves it. Doing that well takes time: the right hardware, the right model, and a workflow as good as the one I have now. I haven't had that time yet. For now I use proprietary models because they are the most effective for my work and I lack the time and resources to do otherwise. It is a trade-off, and I keep it open.

## A word on style

I edit what I write against a style guide that strips out the usual marks of machine writing. That is a matter of taste, and this page exists so that nobody has to guess what sits behind it.

## Reuse

Feel free to copy this page for your own practice. A link back is welcome but not required.

---

## En français

*Document en cours. Version 0.3, 28 septembre 2026. Note personnelle sur ma pratique ; elle n'engage pas mon employeur.*

Je travaille en gestion de l'information : les données qu'une organisation collecte, et les outils et systèmes qui les entourent. Une grande partie de ce travail passe aujourd'hui par des outils d'IA, surtout des agents qui travaillent directement sur mes fichiers et sur les systèmes dont je m'occupe. Je préfère le dire clairement.

La production (formulaires, scripts, bases, tableaux de bord) est devenue bon marché. Ce qui ne l'est pas : comprendre ce dont une équipe a besoin, s'accorder sur ce qu'un chiffre veut dire avant de le dessiner, vérifier qu'il correspond à la réalité, construire quelque chose que l'équipe fera vivre sans moi, et accompagner les personnes qui l'utiliseront. C'est là que je mets mon temps.

Ces outils servent aussi à réfléchir, pas seulement à produire : brainstormer, mettre un plan à l'épreuve, confronter une méthode aux standards publiés, réfléchir à l'évolution du métier. Cette page est née d'une de ces conversations.

Je travaille un peu comme un DJ : plusieurs modèles et agents, plusieurs sessions en parallèle, la documentation des éditeurs, des outils communautaires, le savoir des collègues et les données elles-mêmes. Je prends rarement une sortie telle quelle : je combine, je garde le meilleur, je réordonne et je finis à la main. Le public, ce sont les personnes pour qui je travaille ; si ça ne leur parle pas, le mix était mauvais.

Le travail suit en général la même boucle : du contexte au départ, un plan validé avant de construire, des agents qui lisent et cherchent en parallèle, des formulaires et tableaux de bord construits en environnement de test puis vérifiés là où ils vivront, un relecteur indépendant, puis ma relecture. Rien ne part vers une personne sans que je l'aie lu. Chaque erreur devient une règle écrite ; il y en a une soixantaine.

Mes notes de travail restent dans mon environnement de travail et n'accueillent aucune donnée personnelle des personnes que mon organisation accompagne. Quand le travail touche ces données, les agents passent par des scripts qui rapportent la structure et les comptes plutôt que le contenu, sur des serveurs de test ou des copies locales autant que possible. Le système n'est pas parfait : quand un garde-fou lâche, je le consigne, je corrige la règle, et je préviens le délégué à la protection des données de mon organisation si des données personnelles sont en jeu.

Je désactive l'entraînement des modèles partout où je le peux, parce qu'un modèle entraîné sur des données personnelles n'est pas anonyme par défaut (CEPD, CNIL). Pour le reste, les fournisseurs gardent la main (30 jours de conservation pour Claude dans mon cas, davantage en cas de signalement ou de décision de justice), désactiver l'entraînement n'empêche pas le profilage, et personne ne le vérifie en temps réel. Ces outils ont aussi été construits en aspirant une part immense du savoir écrit de l'humanité, souvent sans le consentement des auteurs, transformant ce savoir commun en produits privés. Je pense pourtant qu'il faut apprendre à les maîtriser, pour les utiliser à bon escient. J'aimerais passer à des modèles ouverts, installés sur ma machine ; faute de temps et de moyens, j'utilise pour l'instant des modèles propriétaires, les plus efficaces pour mon travail. C'est un compromis, que je garde ouvert.
