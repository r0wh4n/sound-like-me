# Learning a voice

Goal: a `~/.voice/VOICE.md` that makes drafts sound like the person, built from what they actually sent to people. It should take about five minutes of their time.

## 1. Collect messages they sent

Learn from messages sent to people, not from their prompts to AI. People write to an AI in a different register (instructions, often more formal or more clipped), so a voice learned from prompts comes out wrong.

- If a connected tool can search what they sent, use it: Slack `from:me`, Gmail `in:sent`, and so on. Pull 30 to 60 recent messages across different people and channels.
- Otherwise ask them to paste 15 to 20 messages they sent to a mix of people: a teammate, their manager, a group channel, someone outside their company.

Drop pasted logs or code, forwarded or quoted text, bare links, one-word replies ("ok", "done", "haan") and bot or template messages. They skew the numbers without saying anything about the voice.

Tag each remaining message with its audience: peer, manager, channel, external, plus any other group that clearly writes differently. Set three aside, from different audiences, for the test in step 5.

## 2. Ask only what the samples can't show

Ask these together in one message, and skip any the samples already answer:

1. Who do you write to most? (confirms the audience list)
2. What language and script? English, Hinglish in Roman script, a mix? Any words you always spell your own way?
3. Anything you never do? Emojis, em dashes, "hope this helps", sign-offs, exclamation marks, bullet points in chat.
4. What does AI keep getting wrong about how you sound?
5. Is there anyone you write to very differently from everyone else?

Question 4 usually gives the most. Turn each complaint into a Never rule.

## 3. Measure, per audience

From the samples, count rather than guess:

- typical length in words and lines, and whether they send one long message or several short ones
- casing, end punctuation, emoji use
- greeting and sign-off, if any
- language mix, roughly
- fillers, shortened spellings and pet phrases, with how often each one appears
- how they ask for something, push back or say no, give a status update, say thanks

Write rates in plain words: "most messages", "about half", "rarely". Leave out any quirk that shows up in fewer than about one message in ten. That's noise, not voice.

## 4. Write the file

Create `~/.voice/` if it's missing, and write `~/.voice/VOICE.md` from the template below. Examples go in word for word, apart from the privacy scrub described in SKILL.md. Keep the file under about 200 lines, because it's read on every draft.

```markdown
# Voice: <name>

_Updated YYYY-MM-DD · learned from <N> sent messages_

Use this file when drafting messages to other people on <name>'s behalf.
Not for replies to <name> directly, and not for code, docs or commit messages.

## Always
-

## Never
-

## Spellings and quirks
Use each at the rate given, not in every line.

| they write | instead of | how often |
|------------|------------|-----------|
|            |            |           |

## By audience

### Peer (DM)
- length:
- tone:
- language mix:

### Manager

### Team channel

### External

## Moves
- asking for something:
- pushing back or saying no:
- status update:
- thanks:

## Examples
Real messages, scrubbed. At most 20.

> **peer · slack**
> ...

## Corrections
```

## 5. Test against the held-out messages

For each of the three messages set aside in step 1, describe its situation in one line, draft it from the new file, and show your draft next to what they actually sent. Ask what's off. Log each answer as a Correction (see SKILL.md) and tighten the rules it points to. One round is usually enough.

## 6. Hook up their other tools

Tell them the file is at `~/.voice/VOICE.md` and that any other agent can use it with one line, such as "When drafting messages to other people, follow ~/.voice/VOICE.md." The README has the exact steps for Codex, ChatGPT and Cursor.
