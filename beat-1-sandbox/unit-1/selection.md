# Unit 1 — Issue Selection

Path: `beat-1-sandbox/unit-1/selection.md`

Record of the issue carried into Unit 2, and of the evaluation runs that produced
`eval-run.txt`. This file is graded at the path above; a copy kept anywhere else in
the repository is not read.

Complete every labelled field below. Each is graded on its own; content placed under the
wrong label is not graded.

---

## Selected issue

**Issue link**

https://github.com/codepath/pathreview-ai301-fa26-s1/issues/56

**Verdict output**

Live-mode run on four candidates (`claude -p "issue-select: grade these candidate first
issues: <#64 URL> <#56 URL> <#59 URL> <#58 URL>"`). #56 is the top-ranked, accepted
candidate; full multi-candidate output below, per `SKILL.md`'s ranked read-out format.

**The verdict must record `accept` for this issue.** Choose an issue your own skill
accepts. If your skill rejects every candidate you try, that is a signal about your
rubric rather than about the issues: revise it and re-run — retries are unlimited and a
partial re-run costs about $0.20 — or run the skill on different candidates. Output
recording `reject` for the issue you chose earns no credit for this field.

````
## Summary

**Repo-level facts** (apply to all four): not archived, last push 2026-09-16 (within 180 days of 2026-09-22), all recent commits authored by a human (Aburke225, 2026-09-16), no CONTRIBUTING.md/AI_POLICY.md found (silence → passes). All four issues have no comments, no assignees, no linked PRs.

| Issue | Repo checks | Bounded scope | Unclaimed | AI policy | Good-first-issue label | Small footprint | Verdict |
|---|---|---|---|---|---|---|---|
| #64 relevance scorer fixture | pass | pass (fix one test fixture) | pass | pass | pass | pass | accept |
| #56 structural chunker | pass | pass (fix one method) | pass | pass | pass | pass | accept |
| #59 faithfulness checker | pass | pass (fix one function) | pass | pass | fail (no label) | pass | accept |
| #58 bias detector patterns | pass | pass (regex patterns in one file) | pass | pass | fail (no label) | pass | accept |

All four are accepted — none are archived-repo, dead-maintainer, unbounded, claimed, or AI-policy-blocked. Ranked by fit (Python/AI-ML/backend engineering, concrete bounded outcome, avoid heavy domain-judgment work):

1. #56 — real production-code fix in the RAG ingestion pipeline (chunker fallback logic), "good first issue" label, single-function footprint.
2. #64 — "good first issue" labeled, trivially bounded (fix one test fixture), lowest risk first PR.
3. #59 — meatier RAG logic fix (semantic-ish support matching) with good engineering upside, but no beginner label.
4. #58 — bounded to one file, but fixing bias-language regex leans on subjective/domain judgment the fit profile says to avoid, and covers 9 failing tests (more surface area than the others).

```json
[
  {
    "item": "https://github.com/codepath/pathreview-ai301-fa26-s1/issues/56",
    "checks": [
      {"name": "Repo not archived", "grade": "pass", "evidence": "archived: false"},
      {"name": "Repo push-recent", "grade": "pass", "evidence": "pushed_at 2026-09-16, measured 2026-09-22 (6 days)"},
      {"name": "Human maintainer activity", "grade": "pass", "evidence": "last commits authored by Aburke225 (human) on 2026-09-16, within 30 days"},
      {"name": "Bounded scope", "grade": "pass", "evidence": "fix confined to StructuralChunker.chunk() returning empty list for headingless docs"},
      {"name": "Unclaimed", "grade": "pass", "evidence": "no assignees, no comments, no linked PRs"},
      {"name": "AI-contribution policy allows this workflow", "grade": "pass", "evidence": "no CONTRIBUTING.md/AI_POLICY.md found; silence passes"},
      {"name": "Approachable label", "grade": "pass", "evidence": "labels: bug, good first issue, ingestion, tier-1"},
      {"name": "Small footprint", "grade": "pass", "evidence": "single method fix in one file"}
    ],
    "verdict": "accept"
  },
  {
    "item": "https://github.com/codepath/pathreview-ai301-fa26-s1/issues/64",
    "checks": [
      {"name": "Repo not archived", "grade": "pass", "evidence": "archived: false"},
      {"name": "Repo push-recent", "grade": "pass", "evidence": "pushed_at 2026-09-16, measured 2026-09-22 (6 days)"},
      {"name": "Human maintainer activity", "grade": "pass", "evidence": "last commits authored by Aburke225 (human) on 2026-09-16, within 30 days"},
      {"name": "Bounded scope", "grade": "pass", "evidence": "fix confined to one test fixture in test_relevance_scorer.py"},
      {"name": "Unclaimed", "grade": "pass", "evidence": "no assignees, no comments, no linked PRs"},
      {"name": "AI-contribution policy allows this workflow", "grade": "pass", "evidence": "no CONTRIBUTING.md/AI_POLICY.md found; silence passes"},
      {"name": "Approachable label", "grade": "pass", "evidence": "labels: bug, good first issue, tests, tier-1"},
      {"name": "Small footprint", "grade": "pass", "evidence": "single test fixture change"}
    ],
    "verdict": "accept"
  },
  {
    "item": "https://github.com/codepath/pathreview-ai301-fa26-s1/issues/59",
    "checks": [
      {"name": "Repo not archived", "grade": "pass", "evidence": "archived: false"},
      {"name": "Repo push-recent", "grade": "pass", "evidence": "pushed_at 2026-09-16, measured 2026-09-22 (6 days)"},
      {"name": "Human maintainer activity", "grade": "pass", "evidence": "last commits authored by Aburke225 (human) on 2026-09-16, within 30 days"},
      {"name": "Bounded scope", "grade": "pass", "evidence": "fix confined to _is_supported() in faithfulness_checker.py"},
      {"name": "Unclaimed", "grade": "pass", "evidence": "no assignees, no comments, no linked PRs"},
      {"name": "AI-contribution policy allows this workflow", "grade": "pass", "evidence": "no CONTRIBUTING.md/AI_POLICY.md found; silence passes"},
      {"name": "Approachable label", "grade": "fail", "evidence": "labels: bug, rag, tier-1 — no good-first-issue/help-wanted/easy label, no comments at all"},
      {"name": "Small footprint", "grade": "pass", "evidence": "single function fix in one file"}
    ],
    "verdict": "accept"
  },
  {
    "item": "https://github.com/codepath/pathreview-ai301-fa26-s1/issues/58",
    "checks": [
      {"name": "Repo not archived", "grade": "pass", "evidence": "archived: false"},
      {"name": "Repo push-recent", "grade": "pass", "evidence": "pushed_at 2026-09-16, measured 2026-09-22 (6 days)"},
      {"name": "Human maintainer activity", "grade": "pass", "evidence": "last commits authored by Aburke225 (human) on 2026-09-16, within 30 days"},
      {"name": "Bounded scope", "grade": "pass", "evidence": "expand regex patterns in bias_detector.py to fix 9 named failing tests — enumerable set, one file"},
      {"name": "Unclaimed", "grade": "pass", "evidence": "no assignees, no comments, no linked PRs"},
      {"name": "AI-contribution policy allows this workflow", "grade": "pass", "evidence": "no CONTRIBUTING.md/AI_POLICY.md found; silence passes"},
      {"name": "Approachable label", "grade": "fail", "evidence": "labels: bug, safety, tier-1 — no good-first-issue/help-wanted/easy label, no comments at all"},
      {"name": "Small footprint", "grade": "pass", "evidence": "confined to one file (bias_detector.py)"}
    ],
    "verdict": "accept"
  }
]
```
````

---

## Eval iterations

Quote source text directly in each field below. Paraphrase does not satisfy them.

**Run history**

1. `--limit 4` smoke run on my first filled rubric: `agreement: 2/4 scored items`. Two clear-accept issues (issue-01, issue-04) both failed my "Bounded scope" check incorrectly.
2. `--only issue-01,issue-04` (re-run to confirm the smoke-run failures before editing anything): `agreement: 0/2 scored items` — same two misses, confirmed not a fluke.
3. After rewriting "Bounded scope" to stop treating a multi-step checklist or a terse "etc."-style list as automatically unscoped (it only fails now on an explicit umbrella/megaissue label, an open-ended/no-fixed-boundary ask, an unresolved design debate, or a stated core-internals blocker): `--only issue-01,issue-04,issue-05,issue-10,issue-15`: `agreement: 4/5 scored items`. issue-01 and issue-04 now correctly passed; issue-15 flipped to an incorrect `accept` (a 5-year-old, 97-comment issue whose thread reads as settled early on, but which has 2 abandoned closed PRs in its history).
4. After adding an explicit clause — an issue open more than 2 years with 2+ closed/unmerged linked PRs fails "Bounded scope" even if the visible thread looks resolved — `--only issue-15,issue-09` (issue-09 as a canary, since it also has one old closed PR and I needed to confirm the new clause didn't over-fire on a single abandoned attempt): `agreement: 2/2 scored items`. Both correct.
5. Full run to confirm: `agreement: 19/20 scored items  (bar: 18/20: PASS)`. Categories: `claimed 4/4  clear-accept 8/8  dead-repo 3/3  policy 1/1  scope 3/4`.
6. Final run with `--save-run eval-run.txt`: `agreement: 19/20 scored items  (bar: 18/20: PASS)` — identical to step 5, confirming the result is stable.
7. Live-mode run on 3 real Path Review candidates (#72, #61, #57) surfaced a different problem than any eval bundle did: all three were rejected on "Human maintainer activity," because that check required commits from *two different* human accounts within 30 days, and the Path Review repo has exactly one human committer (course staff). I loosened the check to require only one human account (see Check rationale/Trade-offs).
8. Canary re-check after loosening the check: `--only issue-02,issue-07,issue-17,issue-14`: `agreement: 4/4 scored items` — the three dead-repo rejects and the single-committer accept (`issue-14`) all still graded correctly.
9. Full run to reconfirm and re-save: `agreement: 19/20 scored items  (bar: 18/20: PASS)` — same single miss (`issue-20`) as before the change. **This is the run recorded in the committed `eval-run.txt`.**

**Issue analysis**

`issue-20` (source `excalidraw/excalidraw#11811`, category `scope`). My rubric's verdict: **accept**. Gold label: **reject** ("one-line feature wish with no spec and a product decision hiding inside"). My rubric's "Bounded scope" check graded this `pass` because the issue body reads as a specific, bounded ask on its surface — it names one new toolbar shape, gives concrete acceptance criteria ("logo tool in the shapes toolbar → place/resize/move like other elements → correct export"), and even states what's explicitly out of scope for v1. None of my check's fail conditions fire: it isn't self-described as a tracking issue, it doesn't span an open-ended slice of the codebase, there's no visible design debate in the (empty) thread, and no maintainer called out core-internals work. What my rubric can't see is that the spec's apparent completeness is hiding an unresolved product decision the checklist doesn't actually resolve — what the logo asset even is, where branding/upload settings should live, and whether the feature belongs in the core editor package at all ("possibly app wiring... if needed," "Logo asset TBD"). That is a judgment call about product ownership, not a fact I can point evidence at the way I can point at an explicit "megaissue" label or an open linked PR — my rubric only catches unscoped work when the issue announces it is unscoped, and this one doesn't announce it.

**Check rationale**

From `rubric.md` as uploaded, the "Human maintainer activity" check:

> Passes when EITHER: (a) at least one issue in the first-response sample got an owner/member/collaborator reply within 90 days of that issue being opened, OR (b) at least 1 of the last 5 default-branch commits is authored by a human account (username does not end in `[bot]`, and is not a bot merging its own scheduled job with no human co-author) dated within 30 days of the measurement date. A lone human maintainer with no other committers or issue replies yet (e.g. a freshly-opened repo) still passes on (b) alone — the bar is "a human is demonstrably behind this," not a headcount. Fails only when neither signal is present (e.g. a stale response sample AND commits that are old and/or bot-only).

Path (b) went through two versions. The first required commits from *two different* human accounts within 30 days, added after `issue-14` (a clear-accept, gold-labeled "quiet but living repo") failed on a draft that gated liveness on the maintainer-response sample alone — that bundle's sample had only one recently-updated issue with no reply, but its last 5 commits were from two different human contributors. That version passed the 20-issue eval set at 19/20, but when I ran the skill live on real Path Review candidates (issues #72, #61, #57), all three were incorrectly rejected: the course repo has exactly one human committer (course staff), so the "two different accounts" bar failed every candidate even though the repo had been pushed to 6 days earlier. I dropped the "two different" requirement to "one human account," since the actual signal Family 1 needs is "is a human behind this," not a minimum headcount.

**Trade-offs**

Loosening from two humans to one human buys back exactly the single-maintainer case above, but it means the check can no longer tell a repo with real, ongoing human maintenance apart from a repo where one person pushed once, a month ago, and has otherwise gone quiet — one recent human commit is now enough, regardless of whether that same person is still around. I re-ran the three dead-repo canaries (`issue-02`, `issue-07`, `issue-17`) and `issue-14` with `--only` after the change specifically to confirm this didn't quietly break anything: all four still graded correctly, because each dead-repo bundle's last commit is many months to years old, so the 30-day recency window — not the account count — is what was actually doing the work in those cases. The full 20-issue set still scored 19/20 after the change (same single miss as before, `issue-20`). The gap I accepted: a repo with one recent commit and zero issue engagement now passes on liveness alone, same as the Path Review course repo did, when in a non-course setting that could just as easily be a maintainer's last commit before going dark. I'd want a longer observation window (e.g. commits across more than one calendar week) before trusting this path on an unfamiliar repo I hadn't also checked by eye.

---

## Selection rationale

Graded on whether all three are answered, in your own words. Not on how good the
reasoning is, and not on length — a short honest answer to each earns the full marks.
This is also the basis for the claim comment you write in Unit 2.

**Selection rationale**

1. **Fit to interests and time.** I picked #56 over the other three accepted candidates
   (#64, #59, #58) because it's a real production-code bug in the RAG ingestion path —
   `StructuralChunker.chunk()` silently drops any document with no markdown headings,
   which is a genuine silent-data-loss failure mode, not just a broken test fixture (#64)
   or a pattern-matching tune-up that leans on subjective judgment (#58). It's also pure
   Python with a zero-dependency repro snippet given directly in the issue, so I can start
   immediately without setting up a database or any other service, which matters for how
   much time I actually have this week.
2. **What the verdict caught vs. what I weighed myself.** The rubric verified the
   mechanical facts across all four candidates: repo not archived, pushed 6 days ago, a
   human account behind recent commits, no assignee/comments/linked PRs, no stated
   AI-contribution policy, and each fix confined to one file or function. What it can't
   weigh is *why* two of the four (#59, #58) lack the "good first issue" label that #56
   and #64 carry — that's a curation signal from course staff about which issues are
   meant for this stage, not a fact my rubric's checks can see (they only check whether
   *some* approachable label exists, not what its absence implies about the other
   candidates in context). I weighed that signal myself, plus the fact that #56 is a
   real logic fix rather than #64's test-fixture-only correction, in choosing #56 over
   the other three accepted candidates.
3. **Anticipated difficulty claiming it.** Low-to-moderate. Reproducing the bug is
   trivial — the issue gives a one-line repro (`StructuralChunker().chunk(text, {})`
   returns an empty list). The actual fix requires a small design choice the issue
   raises but doesn't fully resolve: whether a headingless document should be emitted as
   a single chunk or handed to a different chunking strategy. I'll need to look at how
   other chunking strategies in the codebase are invoked before picking one, which is
   more investigation than a purely mechanical one-line fix, but still well within a
   first issue's scope.

---

Related paths: `eval-run.txt` in this directory; your skill's files in
`tools/issue-select/`.
