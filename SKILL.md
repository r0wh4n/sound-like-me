---
name: sound-like-me
description: Draft messages to other people in the user's own voice, and learn that voice from messages they actually sent. Use whenever the user asks you to write, draft, reply to, or rephrase a message for someone else (Slack, Teams, email, WhatsApp, LinkedIn, PR or issue comments), or says things like "reply to him", "send it like how I talk", "in my tone", "make it sound like me", "learn my voice" or "update my voice". Also use when the user rewrites a draft you made, so the correction gets saved. Not for code, docs, commit messages, or how you talk to the user directly.
---

# Sound like me

The person's voice lives in one file: `~/.voice/VOICE.md`. Every agent they use reads that same file, so it stays plain markdown with nothing tool-specific in it.

## Which job is this?

- **No `~/.voice/VOICE.md` yet, or they ask to learn or rebuild their voice**: read `setup.md` in this skill's folder and follow it.
- **They want a message drafted**: see Drafting.
- **They changed your draft, pasted what they really sent, or said "no, I'd say it like..."**: see Corrections.

## Drafting

1. Read `~/.voice/VOICE.md`. If it doesn't exist, say so in one line and offer to set it up. For this one message, write plainly and briefly rather than guessing at a voice.
2. Work out the audience: who it's going to and where (peer DM, manager, team channel, someone external). Use the matching section under "By audience". If it's unclear, take the closest one and name it in a few words instead of stopping to ask.
3. Write the draft. Follow Always and Never. Use each spelling or quirk at the rate the file gives. People use their quirks some of the time, and a draft that crams every quirk into every line reads like a parody, which is worse than plain text.
4. Before showing it, hold it next to two or three examples from the same audience. Similar length? Same casing and punctuation? Same language mix? Anything from Never? Fix whatever doesn't match.
5. Show the draft ready to copy, with at most one line around it.

The voice changes how something is said, not what is said. Keep facts, numbers, names, dates and links exactly as given.

Don't send it. Sending is the person's call, even when you have a tool that can, unless they told you to send this specific message. A message in someone's voice that they never saw is impersonation, and it can't be unsent.

The voice is for messages to other people. Keep talking to the user the way you normally do, and leave code, docs and commit messages alone.

## Corrections

The gap between your draft and what they actually send is the best signal there is. When you see one:

1. Append a line under `## Corrections` in `~/.voice/VOICE.md`:
   `- YYYY-MM-DD · <audience>: "<what you wrote>" → "<what they sent>" (<the lesson in a few words>)`
2. Apply the lesson to the current draft straight away.
3. Once Corrections reaches about 20 lines, fold them in: turn repeated lessons into Always, Never or Spellings rules, adjust any rates that were off, then delete the folded lines. Tell the person in one line what changed.

When they share a fresh message they sent that shows the voice well, add it to Examples and drop the oldest one from the same audience. Keep Examples to 20 at most, because the whole file is read on every draft.

## Privacy

VOICE.md holds only the person's own messages. Before saving any example or correction, swap other people's names for roles (`<teammate>`, `<manager>`), and strip emails, phone numbers, links, ticket IDs and anything that looks like a credential. The file stays on their machine. Don't paste it into another service unless they ask.
