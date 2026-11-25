# Building & Governing Banking Agents with Managed Deep Agents & Arcade.dev

The two-hour virtual workshop, Wednesday December 9 2026, 9:00 to 11:00am ET, on Zoom webinar. LangChain hosts it with Arcade. The landing page and registration are at [fieldevents.langchain.com/buildinggoverningbankingagents-dec9](https://fieldevents.langchain.com/buildinggoverningbankingagents-dec9). Speakers on the page: Srimanth Tangedipalli (LangChain), Thierry Damiba and Ilja Herdt (Arcade).

It is the same workshop as the half-day "From Prompts to Policies" from ODSC AI West and the 90-minute [AI Summit NYC session](./nyc-90-minutes.md) the day after: the same story, the same code on the `start` tag, and the same attendee portal. What changes is time. Unlike NYC, this one keeps the evals and the deploy.

## Abstract

From the landing page, word for word (read November 25 2026):

> Build a loan-processing agent and take it from first run to a governed, observable deployment.
>
> Learn how to build a loan-processing agent and take it from first run to a governed, observable deployment. The patterns carry over to any agent that touches customer data, moves money or changes records.
>
> Not in financial services? You're still in the right room. If your agents approve refunds, update orders or adjust pricing and inventory, they need the same guardrails as a loan agent: access scoped to each user, policy checks and human sign-off on big decisions. You'll build each one hands-on.

## What the abstract promises, and where you do it

The portal steps named here are the ones in the portal's LangChain journey today.

| The abstract says | What the attendee does | Block |
| --- | --- | --- |
| Build a loan-processing agent | Starts the Deep Agent from the `start` tag on their own laptop and makes its first tool calls (portal steps "Start agent", "First tool: Slack", "Loan Desk tools"). | Build, Connect |
| Access scoped to each user | The agent posts to Slack and sends from Gmail as the attendee: the first call returns a sign-in link, they authorize once, and the grant is theirs alone. | Connect |
| Policy checks | Asks for the $95K approval and their own policy refuses it, because it is over their limit ("Make it safer"). | Govern |
| Human sign-off on big decisions | The refusal routes the request to an approver. Once the approver says yes, the same ask goes through. | Govern |
| Observable | Finds the $95K refusal as a LangSmith trace and matches it to its audit row on `/panel` ("Observe, evaluate"). | Observe |
| Deployment | Deploys the agent with `mda` and scores its runs ("Deploy, score"). | Observe |

The redaction ask in "Make it safer" is not on the landing page. It stays in, because it takes a minute and the portal step has it.

## Run of show

The clock times are the ones on the landing page. Who teaches each block is the split from AI Summit NYC (LangChain on build and observe, Arcade on connect and govern) and is not confirmed for this session.

| Elapsed | Clock (ET) | Block | Who | Module page |
| --- | --- | --- | --- | --- |
| 0:00 to 0:15 | 9:00 to 9:15 | Welcome and setup | LangChain hosts, Arcade on the portal | [00-setup](./modules/00-setup.md) |
| 0:15 to 0:25 | 9:15 to 9:25 | Building and deploying agents with Deep Agents and LangSmith: the agentic development lifecycle | Sri | [01-build](./modules/01-build.md) |
| 0:25 to 1:00 | 9:25 to 10:00 | Connecting agents to business systems with just-in-time authorization, then governing agent actions with policy hooks and human approval | Thierry and Ilja | [02-connect](./modules/02-connect.md), [03-govern](./modules/03-govern.md) |
| 1:00 to 1:45 | 10:00 to 10:45 | Observing, evaluating, and taking agents to production with LangSmith | Sri | [04-observe](./modules/04-observe.md) |
| 1:45 to 2:00 | 10:45 to 11:00 | Wrap-up and Q&A | All three | [05-wrap-up](./modules/05-wrap-up.md) |

The module pages carry the AI Summit NYC timings and cuts. For this session the timings above apply, and the skill exercise and the evals and deploy items are in.

## The schedule does not match the portal's order yet

The landing page puts build at 9:15 and the Arcade blocks at 9:25. The portal runs the other way round: the attendee makes their Arcade project, identity, Slack seat, Loan Desk server, contextual access and policies (steps 2 to 8) before "Start agent" (step 13). So nobody can start their agent hands-on in the 9:15 block unless that setup is already done.

It also leaves 35 minutes, 9:25 to 10:00, for twelve portal steps: the seven setup steps and the five build steps from "Start agent" to "Make it safer". AI Summit NYC gives the same steps 60 minutes with the pre-work done, and ODSC gave them 120.

Two ways to make it fit, to settle on the prep call:

- **Setup before the day.** The [pre-work](./pre-work.md) grows to cover portal steps 2 to 8, and the welcome is a check that everyone is through them. Then 9:15 is a real hands-on start, and 9:25 to 10:00 is the tool calls and the govern asks.
- **Setup during the talk.** The 9:15 block is Sri presenting, attendees work through steps 2 to 8 while they listen, and the hands-on build moves into the Arcade block. This keeps the pre-work short and makes 35 minutes tight.

Either way govern is what the audience came for. If the session runs late, take the time from observe, which has 45 minutes.

## What is different online

- **No floor helpers.** Nobody can walk to a stuck laptop. Decide before the day where attendees ask for help (Zoom Q&A, or the workshop Slack the portal joins them to) and who watches it.
- **The portal is the room.** Attendees follow the steps in the portal at https://workshop.arcade.dev at their own pace while the speakers present, and the instructor dashboard shows where everyone is.
- **The approver.** One of the speakers plays the approver for the $95K escalation.
- **Opening the parts.** The instructor dashboard can hold the room at one part of the portal and open the next when the session gets there.

## Instructor prep

- The portal room is "Building & Governing Banking Agents (virtual)", slug `banking-agents-virtual-2026-12-09`. It is a draft with enrollment closed.
- Decide how registrants get in: load the registration list from LangChain as the roster, or open enrollment so the join code is enough.
- Model access for the room: one LangSmith LLM Gateway key from LangChain, as at ODSC. Set a spend cap and a key that expires the day after, and revoke it after.
- The LangSmith workshop link for attendees' Managed Deep Agents access, from LangChain.
- Send the pre-work mail with the join code and the LangSmith link.
- Give LangChain's instructor access to test the portal.
- Dry run with both teams.

## Open questions

- Setup before the day or during the 9:15 talk (above).
- Who teaches which block, and how Thierry and Ilja split connect and govern.
- Roster or open enrollment.
- Who sends the pre-work mail, and when.
- Where attendees ask for help during the session, and who answers.
- Who plays the approver.

## What is proven and what is not

- **Run:** the portal room exists, as a draft with enrollment closed.
- **Read:** the abstract and the schedule, from the landing page on November 25 2026. The portal's steps and their order, from the portal's code. That the instructor can open the portal part by part, from the same code. The registration count, the speakers and the two-hour length, from the shared Slack channel.
- **Assumed, confirm in the dry run:** that the steps fit the blocks above. That a registrant with a LangSmith workshop link and the room's gateway key gets through "Check your access". That the room's Slack channels exist. Nobody has run this session's room start to finish yet.
