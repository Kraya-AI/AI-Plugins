---
name: improve-ai-replies
description: Change what Kraya's AI says to leads and test it before it stays live. Use when the user wants to fix a wrong or unhelpful AI answer, update prices or offers the AI quotes, change the questions it asks or the order of the conversation, change its tone or language, add or edit an FAQ, give it a new document or website link, or asks "what would the AI say if a lead asks X".
---

# Improve the AI's replies

The person is a salesperson, not a technical user. They know their business and how they want leads handled, and they are relying on you to find the right setting and to stop them breaking something. Use plain language and the names on the Kraya dashboard (AI Playbook, FAQ, Knowledge Source, Chat Playground). Never show internal IDs, tool names or raw data. Look things up instead of asking, and ask one question at a time when you must.

## The account is live

There is no test copy of the account. A saved change reaches real leads within minutes, most changes have no undo, and a message that has gone out cannot be recalled. The only way back is to save the old wording again, so always keep it.

`test_ai_reply` is the Chat Playground. It sends nothing and uses no credits, but it tests the settings that are saved. So a change can only be tested after it is saved, when real leads are already getting it. The steps below work around that.

## Steps

1. **Find the cause.** Read `account_settings` and `knowledge_base`. If the person is reporting a bad reply, find the real conversation with `search_leads` and `conversation_messages`, then find the wording in the AI Playbook, FAQ or a knowledge file that produced it. If the setup doesn't explain the reply, say so and use the investigate-issue skill instead of guessing at a fix.

2. **Record the "before".** Run `test_ai_reply` with three or four messages a real lead of theirs would send, chosen to hit the thing being changed, plus one or two ordinary ones to catch side effects. When the change is to a message partway through a conversation, play the chat at least one lead reply past that message, so anything odd that shows up later can be compared with how it behaved before. Keep the replies.

3. **Propose the smallest change.** Show the current wording, the new wording, and what leads will notice. Edit the one part that needs it. Text fields are replaced whole when saved, so send back the full text with only that part changed, and never rewrite the whole AI Playbook to fix one answer. Keep the exact old wording in the chat.

   When the person gives exact wording for a message, check whether the AI Playbook tells the AI to send that message exactly as written. Without such a line the AI treats the text as guidance and rewords it, often pulling in phrases from the company description. If the line is missing, include adding it in the same proposal.

4. **Decide with the person whether to pause the AI.**
   - For a small addition, such as one new FAQ answer or a corrected price, saving directly is usually fine.
   - For anything that changes the conversation flow, the qualifying questions or the tone, recommend pausing AI Auto-Reply while you change and test.
   - Before pausing, tell them the cost: leads who write in during the pause get no AI reply, and AI replies waiting to go out are dropped.
   - Read what `automation_settings_write` says about turning AI Auto-Reply back on for their kind of account. If turning it on would do more than resume, for example going back through existing chats and replying, tell them before pausing and suggest saving directly at a quiet time instead.
   - If they agree to pause, check which numbers, Instagram accounts and team members have AI Auto-Reply on (`account_settings`, `user_settings`, `team_members`), turn off only what is needed, and write down in the chat exactly which ones you turned off.

5. **Wait for a clear yes** to this specific change, then save it with `knowledge_base_write`. A newly added file or link takes a few minutes before the AI can use it, so wait before testing.

6. **Test again with the same messages.** If the change affects how a conversation develops (question order, repeats, hand-offs, qualification, stage moves), play the conversation through turn by turn as `test_ai_reply` describes. A single message only shows the first reply.

7. **Show the result as a readable chat**, with "Lead:" and "AI:" lines, before and after. Point out what changed and anything that surprised you.

8. **Finish cleanly.**
   - If they approve: turn AI Auto-Reply back on for exactly the ones you turned off, and confirm each is on.
   - If they don't: save the old wording again, run the test once more to confirm it behaves as before, then turn the AI back on.

Never leave AI replies paused without saying so clearly. If the conversation is winding down while the AI is still paused, raise it before anything else.

## Things that need extra care

- **Deleting** an FAQ category deletes every article in it, and deletes cannot be undone. Confirm first.
- **Templates the AI may send** go out to real leads as soon as they are added. Confirm the template and when it should be sent.
- **The product catalog** is one file. Uploading a new one replaces the old one.
- **Renaming the organization** happens through the same AI Setup edit. Don't change the organization name unless asked.

## Finish with a summary

Say what changed, what you tested, whether AI Auto-Reply is on or off for each number right now, and anything the person still needs to do.
