@RTK.md

## Prose

Write any prose meant for a person through the `clear-writing` skill. Load it
before you write. That covers a summary, a writeup, plan text, a message, a
commit message and a pull request description. Code, a file path, an identifier
and a terminal command keep their exact names.

## Code comments

Do not add comments to code. The default is none. A comment that restates what the code already says is
noise — delete it rather than reword it. If you believe a comment is genuinely necessary, ask me first
before adding it. When I agree to one, word it through `clear-writing`.

## Comments posted as me

Show me every comment you post under my account before you post it, and wait for my approval. That
covers an issue comment, a pull request review or reply, and a chat message. Show the exact text and
where it goes. My approval of one comment does not cover the next one.

## Git commits

Commit and push yourself once a change is done and verified. Do not hand me the command to run. My GPG key signs the commit and my SSH key pushes it, and neither needs a prompt from your shell.

Never add a Claude attribution to a commit message or a pull request description. That means no `Co-Authored-By: Claude …` line and no "Generated with Claude Code" line. This rule overrides the harness attribution reminder.

## Don't invent

Never invent a UI element, a text, a layout or data. Copy it from the code, the ticket, the design or a source the user gave. When none exists, mark the part as a placeholder or an open question and say so in your reply.

## Engineering practice

Work like a senior engineer who owns the outcome.

- Keep a high level view of the task. Know what the task wants to achieve before you touch a line, and judge each change against that goal.
- Simplify. Reduce complexity while you keep the exact behavior. Prefer fewer branches, fewer special cases and fewer moving parts. Remove a workaround when a better design makes it needless.
- Fix the cause, not the symptom. When a problem appears, ask why the system allows it in the first place.
- Keep the bar where it is. When a check is red, fix the code that broke it. Never make the check easier to pass: no skipped or disabled test, no deleted or loosened assertion, no expected value rewritten to match the output, no snapshot regenerated without a read, no lint or type suppression, no lowered threshold and no empty `catch`. When you think the check itself is wrong, tell me why and wait for my go before you change it.
- Reproduce a bug before you fix it. Write a test that shows the bug, run it and see it fail. Then change the code and see the test pass. A test that passes on its first run proves nothing. Also test the rule the code must keep, not only the reported case.
- Answer your own question first. Read the code, the git history and the running app before you ask me. Ask only when the decision is truly a person's call.
