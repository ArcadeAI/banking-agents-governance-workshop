# Building & Governing Banking Agents: Who Is Your Agent Acting As?

The 90-minute workshop at The AI Summit New York, Javits Center, Thursday December 10 2026, 2:30 to 4:00pm ET. Shub Argha leads. This branch, `arcade-langchain`, is the version co-hosted with LangChain: the agent runs on LangChain Deep Agents, every run is traced in LangSmith, and LangChain teaches build and observe. The `main` branch is the Arcade-only version.

It is a 90-minute cut of the half-day "From Prompts to Policies" workshop from ODSC AI West, built from [`ArcadeAI/deep-agents-governance`](https://github.com/ArcadeAI/deep-agents-governance). The story, the code and the attendee portal are the same. What changes is time: setup moves before the day, and evals and deploy are cut.

## Abstract

Banking agents are easy to demo but hard to approve, because security wants to know who the agent acts as and what it can do. In this 90-minute hands-on workshop, you'll build a loan-processing agent with LangChain Deep Agents and use Arcade to add the guardrails that answer those questions: just-in-time authorization scoped to each user, policy checks that block out-of-bounds actions, human approval for high-value decisions, and redaction of sensitive data before it reaches the model. Bring a laptop.

## The story

A loan officer asks the agent to approve a $95K loan for Northwind Bakery (LN-2291). Arcade's hooks refuse it, because $95K is over her $50K authority. The refusal tells the agent how to escalate, the request reaches an approver in Slack, the retry passes once he approves, and the borrower gets an email from her own Gmail. Every step lands as an audit row on the live panel.

The thesis, from the [README](../README.md#why-we-built-this): treat the LLM as an adversary, and put the controls somewhere it cannot reason around.

## Run of show

Order follows the portal: the Arcade setup runs before the agent starts.

| Elapsed | Clock (ET) | Block | Module page |
| --- | --- | --- | --- |
| 0:00 to 0:10 | 2:30 to 2:40 | Welcome, the end state on screen, setup check | [00-setup](./modules/00-setup.md) |
| 0:10 to 0:30 | 2:40 to 3:00 | Connect: Arcade project, identity, workshop Slack, Loan Desk MCP server | [02-connect](./modules/02-connect.md) |
| 0:30 to 0:45 | 3:00 to 3:15 | Build: start your Deep Agent, first tool calls (LangChain) | [01-build](./modules/01-build.md) |
| 0:45 to 1:10 | 3:15 to 3:40 | Govern: hooks, policy, end to end, Make it safer | [03-govern](./modules/03-govern.md) |
| 1:10 to 1:20 | 3:40 to 3:50 | Observe: the $95K refusal as a LangSmith trace and as its audit row (LangChain) | [04-observe](./modules/04-observe.md) |
| 1:20 to 1:30 | 3:50 to 4:00 | Wrap-up, Q&A, feedback QR, booth #1022 | [05-wrap-up](./modules/05-wrap-up.md) |

ODSC ran the same material in 240 minutes: setup 15, build 30, connect 45, break 15, govern 45, observe 60, wrap-up 30. The 90-minute cut drops the break, the evals and deploy, and the agent skill exercise, and it only fits if attendees do the [pre-work](./pre-work.md) before the day.

## Facilitator notes

- **Govern is the abstract.** Protect its 25 minutes. If the room runs late, cut observe to a one-minute look at the panel, not govern.
- **Show the end before the start.** In the welcome, run the $95K refusal and open `/panel` with its Access, Pre and Post lanes, so everyone knows where the 90 minutes go.
- **Connect in 20 minutes needs pre-work.** ODSC gave it 45. Check at 2:40 who has an Arcade account and a project key, and send floor helpers to the rest first.
- **Build, items 1 to 5 are the floor.** Item 6, the credit-memo skill, is cut. If port 2024 is busy, an old agent is running: `lsof -ti :2024 | xargs kill`. `ask.py` prints "Asking as <email>"; if it names someone else, rerun it with `--sign-in`.
- **Loan ids are per seat.** LN-2291 reads LN-1491 in seat 14.
- **The approver.** Someone in the room plays the approver for the $95K escalation (TBD).
- **Feedback QR before the session ends**, not after, then point people to booth #1022.
- **Fallbacks.** With the model down, the agent runs its scripted model (`agent/scripted.py`), which still proves the sign-in, the Engine call and the hooks. With the wifi down, the `/walkthrough` page has the four acts as diagrams for a talk-through.

## Instructor prep

- Create the workshop in the portal (instructor dashboard, New workshop) and set its links to `workshop.arcade.dev`. Bank laptops dropped `arcadeworkshop.dev` at Toronto because the domain was too new for their web filters.
- Add co-instructors on the portal's Instructors page. Anyone signing in with an arcade.dev Google account is already an instructor.
- Send the pre-work mail with the join code (owner and date TBD).
- Model access for the room: one LangSmith LLM Gateway key from LangChain, as at ODSC (to confirm with LangChain). Set a spend cap and a key that expires the day after, and revoke it after.
- The LangSmith workshop link for attendees' Managed Deep Agents access, from LangChain.
- Full dry run on venue-like wifi, at full capacity.

## Open questions

- LangChain instructors for build and observe, and the room's gateway key.
- Who plays the approver for the $95K escalation.
- Room, AV, power, wifi, attendee count and walk-ins.
- Floor helpers, and the hand-off from the room to booth #1022.
