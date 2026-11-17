# Kraya

Manage your Kraya CRM account by talking to your AI assistant. The plugin pairs the Kraya connector with three skills that teach the assistant how to make changes to a live account safely.

## Install

In Claude, open **Customize > Plugins > Add > Add marketplace** and paste `https://github.com/Kraya-AI/AI-Plugins`, then install **Kraya**. In Claude Code:

```
/plugin install kraya --marketplace Kraya-AI/AI-Plugins
```

## Use it

Connect the Kraya connector from the plugin's Connectors tab and sign in with your Kraya login. Then ask in plain language:

- "The AI is quoting the old price. Fix it." The assistant shows you the current wording and the proposed wording, tests the change in the Chat Playground, and shows you the test chat before leaving it live.
- "Create a follow-up sequence for leads who went quiet after the demo." The assistant drafts it, tells you who it will reach, and switches nothing on until you agree.
- "Why didn't Priya get a reply yesterday?" The assistant checks the lead, the conversation and your settings, and explains what happened.

Your account is live, so the assistant asks for your approval before any change that affects real leads.

## Data

The plugin sends your requests to your own Kraya account through api.kraya-ai.com, using the access you approve when you connect (view only, or view and change). It stores nothing itself. See the [Privacy Policy](https://kraya-ai.com/privacy-policy).
