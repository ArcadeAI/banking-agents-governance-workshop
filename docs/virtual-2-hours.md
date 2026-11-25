# Building & Governing Banking Agents with Managed Deep Agents & Arcade.dev

The two-hour virtual workshop, Wednesday December 9 2026, 9:00 to 11:00am ET, on Zoom webinar. LangChain hosts it with Arcade. The landing page and registration are at [fieldevents.langchain.com/buildinggoverningbankingagents-dec9](https://fieldevents.langchain.com/buildinggoverningbankingagents-dec9). Speakers on the page: Srimanth Tangedipalli (LangChain), Thierry Damiba and Ilja Herdt (Arcade).

It is the same workshop as the half-day "From Prompts to Policies" from ODSC AI West and the 90-minute [AI Summit NYC session](./nyc-90-minutes.md) the day after: the same story, the same code on the `start` tag, and the same attendee portal. What changes is time. Unlike NYC, this one keeps the evals and the deploy.

## Run of show

The clock times are the ones on the landing page.

| Elapsed | Clock (ET) | Block | Module page |
| --- | --- | --- | --- |
| 0:00 to 0:15 | 9:00 to 9:15 | Welcome and setup | [00-setup](./modules/00-setup.md) |
| 0:15 to 0:25 | 9:15 to 9:25 | Building and deploying agents with Deep Agents and LangSmith (LangChain) | [01-build](./modules/01-build.md) |
| 0:25 to 1:00 | 9:25 to 10:00 | Connecting agents to business systems with just-in-time authorization, then governing agent actions with policy hooks and human approval (Arcade) | [02-connect](./modules/02-connect.md), [03-govern](./modules/03-govern.md) |
| 1:00 to 1:45 | 10:00 to 10:45 | Observing, evaluating, and taking agents to production with LangSmith (LangChain) | [04-observe](./modules/04-observe.md) |
| 1:45 to 2:00 | 10:45 to 11:00 | Wrap-up and Q&A | [05-wrap-up](./modules/05-wrap-up.md) |

The module pages carry the AI Summit NYC timings and cuts. For this session the timings above apply, and the skill exercise and the evals and deploy items are in.

ODSC gave connect and govern 90 minutes together. Here they get 35, so the [pre-work](./pre-work.md) matters as much as it does in NYC: accounts and installs before the day.

## What is different online

- **No floor helpers.** Nobody can walk to a stuck laptop. Decide before the day where attendees ask for help (Zoom Q&A, or the workshop Slack the portal joins them to) and who watches it.
- **The portal is the room.** Attendees follow the steps in the portal at https://workshop.arcade.dev at their own pace while the speakers present, and the instructor dashboard shows where everyone is.
- **The approver.** One of the speakers plays the approver for the $95K escalation.

## Instructor prep

- The portal room is "Building & Governing Banking Agents (virtual)", slug `banking-agents-virtual-2026-12-09`. It is a draft with enrollment closed.
- Decide how registrants get in: load the registration list from LangChain as the roster, or open enrollment so the join code is enough.
- Model access for the room: one LangSmith LLM Gateway key from LangChain, as at ODSC. Set a spend cap and a key that expires the day after, and revoke it after.
- The LangSmith workshop link for attendees' Managed Deep Agents access, from LangChain.
- Send the pre-work mail with the join code and the LangSmith link.
- Give LangChain's instructor access to test the portal.
- Dry run with both teams.

## Open questions

- Roster or open enrollment.
- Who sends the pre-work mail, and when.
- Where attendees ask for help during the session, and who answers.
- Who plays the approver.
