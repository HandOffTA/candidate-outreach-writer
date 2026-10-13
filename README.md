# candidate-outreach-writer

A Claude Skill that turns a hiring-manager intake transcript into candidate positioning, a LinkedIn DM, and a four-touch outreach sequence.

## What it does

Outreach fails for one of two reasons: it's about the company instead of the candidate, or it asks for too much too early. The intake call is where the cure lives — it holds the specifics that separate a real message from templated noise. This skill mines those specifics and turns them into messages that sound like a person wrote them.

- **Mines the transcript** for the real problem, scope, team, proof of momentum, and the honest hard parts
- **Builds the positioning** — one-line pitch, who it's for, who it *isn't* for, three ranked hooks, the honest tradeoff, and the objections you'll actually hear
- **Writes the LinkedIn DM** in 2–3 variants at different angles, within the ~300 character connection-note limit
- **Builds the four-touch sequence** where every touch has a distinct reason to exist

## The sequence

| Touch | Day | Channel | Job of this message |
|---|---|---|---|
| 1 | 0 | InMail or email | The pitch. Strongest hook, one ask. |
| 2 | +3 | LinkedIn DM | New angle — a detail not in touch 1. |
| 3 | +7 | Email | Value regardless of interest (comp, team's work). |
| 4 | +12 | Email | Close the loop, leave the door open, invite a referral. |

Every message stands alone, no sentence repeats across touches, and the final touch asks for nothing but permission to stop — which is usually the highest-replying message in the set.

## Install

**In Claude (web or desktop):**
1. Download `SKILL.md` from this repo.
2. Open Claude's **Settings**.
3. Find the **Skills** section (under Capabilities).
4. Choose **Upload skill** and select the file.

**In Claude Code:**
1. Open a terminal.
2. Run `mkdir -p ~/.claude/skills/candidate-outreach-writer`
3. Copy `SKILL.md` into that folder.
4. Restart Claude Code.

## How to use it

Paste an intake transcript, call notes, or a job spec and say what you need:

- "Here are my notes from the kickoff call — write me outreach."
- "My InMails are getting ignored for this role, can you fix them?"
- "Draft a four-touch sequence for this req."
- "Write something I can send this candidate."

Works best with an intake transcript. With only a job spec it will say the positioning is thinner and ask the two or three questions that close the biggest gaps.

## What you get back

```
### Positioning
### LinkedIn DM — 3 variants      (angle + character count each)
### Four-touch sequence           (day, channel, subject, body)
### Personalization slots         (where to swap in candidate detail)
### What I couldn't source        (gaps left blank, not invented)
```

## Notes

- It will not invent specifics. Fabricated detail surfaces at the screen when a candidate asks a follow-up question.
- It avoids the standard recruiter tells: "I came across your profile," "exciting opportunity," "hope this finds you well."
- Register adapts by market — trades outreach leads with pay rate, schedule, location, start date; startup tech leads with scope, stage, and who they'd build with.

## Contents

```
candidate-outreach-writer/
├── SKILL.md
└── README.md
```

## License

MIT
