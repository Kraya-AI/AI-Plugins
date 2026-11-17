# Kraya Plugins

Plugins that let your AI assistant manage your [Kraya](https://kraya-ai.com) account.

## Kraya

Manage your Kraya CRM account by talking to Claude. The plugin pairs the Kraya connector with three skills that teach Claude how to change a live account safely:

| Skill | Ask for it when |
|---|---|
| Improve AI replies | The AI gave a wrong answer, quotes an old price, or should ask different questions |
| Build follow-ups | You want a follow-up sequence, a Smart Trigger, a broadcast or a template |
| Investigate an issue | A lead didn't get a reply, or a sequence or trigger didn't behave as expected |

Your account is live, so Claude shows you what will change and asks before changing anything that affects real leads.

### Install in Claude (web or desktop app)

1. Open **Customize > Plugins > Add > Add marketplace** and paste `https://github.com/Kraya-AI/AI-Plugins`.
2. Install **Kraya** from the list.
3. Open the plugin's **Connectors** tab, connect Kraya, and sign in with your Kraya login.

### Install in Claude Code

```bash
claude plugin marketplace add Kraya-AI/AI-Plugins
```

```bash
claude plugin install kraya@kraya-ai-plugins
```

### Data

The plugin sends your requests to your own Kraya account through api.kraya-ai.com, using the access you approve when you connect. The plugin stores nothing itself. Changes you approve are saved in your Kraya account, and Kraya keeps a record of the actions your assistant takes there. See the [Privacy Policy](https://kraya-ai.com/privacy-policy).
