# How I work: the technical side

*Companion to the [transparency note](README.md). Work in progress.*

## How a piece of work gets made

It starts with context. When I open a session, the agent is handed a short brief on where my projects stand and what happened in the last sessions, so we pick up where we left off.

Then I describe the problem the way I would brief a colleague, sometimes by voice, often in rough notes. For complex work, the agent comes back with a plan first, and I approve or change it before anything is built.

The work then fans out. The main agent sends helpers to read documentation or search past projects, and they come back with conclusions and their sources rather than raw dumps. On larger pieces, several sessions run in parallel, each on its own track.

Everything is built against reality. Forms, data pipelines and dashboards are made first in a test environment, with synthetic data or a faithful copy, then checked where they will actually live: on an emulated phone, or against the server's own answer. "It should work" is not a result.

Then come fresh eyes. For forms, dashboards, BI code and scripts, a separate reviewer agent, which knows nothing of how the thing was made, scores the work against our standards, and corrections come in waves. Then I review. Anything addressed to a person goes out after I have read it; emails, for instance, are prepared as drafts that I send myself. Once I have approved a direction, some technical loops run on their own, such as publishing a draft dashboard to an internal workspace, exporting its pages, looking at them, fixing and repeating. I look at the result before I share it.

I am now testing agents that go further on their own, including on live systems: deploying forms, migrating records, changing user permissions. That always comes after a rehearsal on a copy, and only on my explicit go-ahead; the largest run so far moved several thousand records without losing one. On a well-defined task, I sometimes let an agent work for hours on its own, then review what it did.

Sessions end with notes on what was decided and what comes next. Local copies that hold personal data are kept only as long as the project needs them, then deleted.

And every mistake becomes a rule: a few lines, dated, with the story of what went wrong. There are about sixty of them now, and the agent reads them at the start of every session. Over time the rules have become the method, and they are probably the most useful thing I have built.

## The setup

Nothing exotic, and mostly plain text. A working memory (an index, one file per project, a session log and a "where we left off" note), the rules, and 26 skills, which are packaged procedures for recurring jobs such as building a form, designing a dashboard, analysing a dataset or writing a document in the house style. One copy of the skills is shared by two different agent tools. Five reviewer agents each have a narrow brief. Connectors reach the systems I administer, and the agent can drive a browser and a phone emulator when it needs to see what a user would see.
