# Before the day

The session is short (90 minutes at AI Summit NYC, two hours online), so the installs and accounts happen before it starts. This takes about 15 minutes. The portal keeps your place, so anything you finish now is done on the day.

## Install

- git
- [uv](https://docs.astral.sh/uv/)
- Python 3.12 (the agent supports 3.11 to 3.12)

## Get the code

    git clone https://github.com/ArcadeAI/banking-agents-governance-workshop
    cd banking-agents-governance-workshop
    git fetch --tags --force
    git checkout start
    cd agent
    cp .env.example .env
    uv sync --group evals

Running `uv sync` now means nothing downloads during the session.

## Make your accounts

- **Arcade**: sign up at [arcade.dev](https://www.arcade.dev/), then create a project API key in the dashboard under API keys. You paste it in as `ARCADE_API_KEY` on the day.
- **LangSmith**: an account with Managed Deep Agents on, from the workshop link in your welcome mail ([details](./modules/00-langsmith.md)). The model key is shared by the room; you bring none.
- **Slack**: you join the workshop Slack from the portal on the day.

## Sign in to the portal

Open https://workshop.arcade.dev and sign in with your email and the workshop code from your welcome mail. Do the **Welcome** and **Check your access** steps. That is everything until the day.

## Bring

A laptop, charged.
