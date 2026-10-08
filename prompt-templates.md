# Prompt Templates

One chat, worked through one bucket at a time. The first message sets the rules once, so every later message stays short. Fill in everything in [BRACKETS] before sending.

## Time Plan (30 min)

| Time | Step | Messages |
|---|---|---|
| 0–3 | Write framework, hypothesis, and shared assumptions (no AI) | 0 |
| 3–5 | Send the setup message; Claude does bucket 1 | 1 |
| 5–17 | Review each bucket, correct if needed, move to the next | 1 per bucket |
| 17–20 | Send the synthesis message | 1 |
| 20-25 | Perform my own synthesis and create notes in my style | 0 |
| 25–30 | Rehearse the 5-minute talk out loud (no AI) | 0 |

A 4-bucket framework uses about 6 messages total.

## Before Sending Anything (3 min, no AI)

- **Framework:** [file name, plus any bucket borrowed from another framework]
- **Hypothesis:** [one-sentence answer you expect to give]
- **Shared assumptions:** [3–5 numbers or facts, e.g. client revenue, employee count, timeline]

## 1. Setup Message

Paste `deloitte-role.md` and the framework file above this text.

```
I am a candidate in a Deloitte case interview with 30 minutes to prepare a 5-minute verbal recommendation. Above are the role description and the framework I am using. We will work through the framework one bucket at a time.

CASE:
[paste case]

SHARED ASSUMPTIONS (use these in every bucket; do not replace them):
[paste list]

MY HYPOTHESIS:
[paste one sentence]

SELECTED FRAMEWORK:
[paste selected framework]

RULES FOR EVERY BUCKET:
- Cover only the current bucket. If something belongs in another bucket, flag it in one line at the end.
- Stay under 200 words, with no introduction or summary.
- Label any assumption you add as "NEW ASSUMPTION: [value] because [one-line reason]" and keep using it in later buckets. The reason must be a case fact, simple logic, or a typical industry range. If it is a rough guess, say so. Never invent a specific source or statistic.
- Use this format:
  1. Key questions: the 3 questions this bucket must answer for this case.
  2. Analysis: your answers, with any math shown step by step.
  3. Finding: one sentence on whether this bucket supports or challenges my hypothesis.
  4. Risks: the top 1–2 risks within this bucket.
  5. Ask the interviewer: one piece of data that would strengthen this bucket.

Start with bucket 1. Wait for me before moving on.
```

## 2. Moving to the Next Bucket

After Claude answers a bucket, read it and send one of these two messages. [N] is the number of the next bucket.

**Option A: The answer looks right.** Just ask for the next bucket:

```
Bucket [N].
```

**Option B: Something is wrong.** Give the fix and ask for the next bucket in the same message, so the fix doesn't use up an extra message:

```
Fix: [what is wrong and what to use instead]. Then do bucket [N].
```

Example, after Claude finishes bucket 1 with an adoption rate that seems too high:

```
Fix: 80% adoption is too high for a unionized workforce; use 40% and update the finding. Then do bucket 2.
```

## 3. Synthesis Message

```
All buckets are done. Create a new Google Doc titled "[Case name] – Synthesis" and write everything below into it, using a heading for each numbered section. In chat, reply only with the link to the doc. If you cannot create the doc, write the full content in chat instead.

1. Conflicts: list any places where bucket findings contradict each other or rely on different assumptions. Keep this short.
2. Speaking notes for a 5-minute verbal presentation, as short bullets I can glance at:
   - Recommendation: one sentence, stated first.
   - Three supporting points, each tied to a framework bucket, each with its key number.
   - Biggest risk and how to reduce it.
   - Next steps: 2–3 concrete actions.
3. Likely questions: the 5 questions an interviewer is most likely to ask about my reasoning or numbers, with a one-line answer for each.
4. Bucket summaries: one line per framework bucket, in order, giving its finding and key number.
```

## Emergency: All Buckets at Once

Use only if time or messages are running out. Paste the role and framework above it, as with the setup message.

```
I am a candidate in a Deloitte case interview with 30 minutes to prepare a 5-minute verbal recommendation. Above are the role description and the framework I am using.

CASE:
[paste case]

SHARED ASSUMPTIONS (use these; do not replace them):
[paste list]

MY HYPOTHESIS:
[paste one sentence]

Work through each framework bucket in order. For each bucket, under 100 words: the key question, your analysis with math shown, and a one-sentence finding. Give a one-line reason for every assumption you add (a case fact, simple logic, or a typical industry range); if it is a rough guess, say so, and never invent a specific source or statistic. Then give speaking notes for a 5-minute presentation: a one-sentence recommendation, three supporting points with numbers, the biggest risk, and 2 next steps.
```
