---
name: build-follow-ups
description: Create or change Kraya's automated outreach - follow-up sequences, Smart Triggers, broadcasts, WhatsApp templates, bump-up messages and the automation on/off switches. Use when the user wants to follow up with leads automatically, message leads who went quiet, set a rule like "when a lead moves to X, do Y", send a message to many leads at once, edit the wording or timing of an existing sequence, or turn an automation on or off.
---

# Build follow-ups and automations

The person is a salesperson, not a technical user. They know their business and how they want leads handled, and they are relying on you to find the right setting and to stop them breaking something. Use plain language and the names on the Kraya dashboard (Sequences, Smart Triggers, Broadcasts, Templates, Bump-Up Messages). Never show internal IDs, tool names or raw data. Look things up instead of asking, and ask one question at a time when you must.

## The account is live

There is no test copy of the account. Everything here sends real messages to real leads, and a sent message cannot be recalled. Most changes have no undo, so keep the old wording and settings in the chat before you change them.

For every change:

1. **Look first.** Read `account_settings`, then what already exists: `list_sequences` and `get_sequence`, `list_triggers`, `list_broadcasts`, `list_whatsapp_templates`. Often the right move is a small edit to something that exists, or the thing they want is already there and switched off.
2. **Show the plan.** Give the exact wording of every message, the timing, who receives it and roughly how many leads that is, and when the first message would go out.
3. **Wait for a clear yes** to that specific change. A yes to creating something is not a yes to switching it on.
4. **Make it, then read it back** and show the person what was saved.

Each write tool describes what its change does to leads who are already enrolled or already match. Read that each time and tell the person, in plain words, what applies to them.

## Sequences

- **A new idea is a new sequence.** Editing an existing sequence changes what every lead already on it receives: new wording goes out with each lead's next message, and a new step or a changed delay re-schedules all of them. Before editing, tell the person how many leads are on the sequence and what will change for them. If they want something different for new leads only, duplicate the sequence and edit the copy.
- When a save comes back with a lead count instead of saving, that is the tool asking for confirmation. Take that number to the person; don't confirm on their behalf.
- A test call places a real phone call. Confirm the number with the person first.

## Smart Triggers

- A trigger acts on leads by itself: it moves stages, starts sequences, assigns leads and sends messages.
- Create it switched off, read it back to the person, and switch it on only when they agree.
- Before switching on a trigger based on "no response" or "days in stage", tell them it will act within minutes on every existing lead already past the threshold, and how many leads that is.
- Check the order against the existing triggers so two rules don't fight over the same lead.

## Broadcasts and messages to leads

- Show the exact message and exactly who will receive it, with the count, before sending.
- Sending to many leads who have not messaged first carries a risk of the WhatsApp number being restricted. Say so when a broadcast is large or the audience is cold, and don't turn off the recommended sending limits unless the person insists after hearing the risk.

## WhatsApp templates

- A new template has to be approved by WhatsApp before it can be used, which can take time and can be refused. Tell the person, and check its status before building anything that depends on it.

## Automation switches

- Turning on AI Auto-Reply, Auto Follow-up, Bump-Up Messages, Auto Lead Creation or the welcome message starts automated messages to real leads. Confirm first, and say what will start.
- Turning them off drops or pauses messages that were waiting. Say which.
- By default a switch changes the person's own settings. To change it for a specific number or Instagram account, name that number or account.

## Deleting

Deletes cannot be undone, and leads on a deleted sequence stop receiving it. Offer switching it off instead, and delete only when the person confirms.

## If something looks wrong

Stop, put the previous setting back, then tell the person what happened.

## Finish with a summary

Say what was created or changed, what is switched on and off right now, when the first message will go out and to whom, and anything the person still needs to do.
