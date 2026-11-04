# Life system facts (from Omkar's notes, 5 Nov 2026)

## Challenge
- 143 days, 1 Sep 2026 to 22 Jan 2027. Day 1 is 1 Sep 2026. Plans work backwards from 22 Jan.
- German: FOM Deutsch exam 13 Nov 2026 (A1 to A2). Goals: solid A2 by 22 Jan 2027, B1 exam summer 2027.
- Wake time: `[CONFIRM: wake time used by the detector]`.

## Tiers
- Tier 1 (protect): M.Sc. studies, gym, diet and food prep.
- Tier 2: German, job applications.
- Tier 3 (cut first): skills, projects, content, savings review.
- Never cut Tier 1 to rescue Tier 3.

## Weekly budgets and targets
german_h 10, study_h 6, gym_sessions 4, applications 2. Other weekly properties: batch_cooks, days_under_2_meals, skills_h, clips, money_spent_eur, avg_energy, avg_mood, avg_sleep_h, completion_rate.

## Bad-week mode
- Trigger: energy or mood at 2 or lower for two days in a row.
- Minimum day: 20 min gym or walk, one cooked meal, 30 min study, 10 min German.
- Back to the full plan after two decent days.
- Low mood for more than a week: say so plainly and suggest talking to someone he trusts or a professional.
- Detector: no "start" message by wake time plus 45 min, or a first message sent from bed, means the day runs the minimum version.

## Named patterns (his words)
1. Avoids anything that can fail or reject him. Hours go to the safest track.
2. Deadline panic cycle: avoid, panic late, deliver, regret.
3. Answers pressure with resolutions ("I will start") instead of data.
4. Goes all in when stressed. Oversized plans break.
- German trigger: a missed session leads to falling behind, then not understanding, then dropping it. Rule: no gap longer than one day, minimum 10 min.

## Daily log template (properties are numbers so charts work)
```
---
type: daily-log
date: YYYY-MM-DD
energy:        # 1-5
mood:          # 1-5
sleep_h:
gym:           # session name, "rest" or "none"
food_meals:
protein_logged:
study_h:
german_min:
applications:
skills_h:
content_clips:
money_eur:
[CONFIRM: extra private field]
---
# YYYY-MM-DD
Day X of 143.
- Gym / Food / Good today / Bad today / One fix for tomorrow
## Claude's read
## Tomorrow's first block
```

## Weekly review template
Properties: german_h (budget 10), study_h (budget 6), gym_sessions (target 4), batch_cooks, days_under_2_meals, applications (target 2), skills_h, clips, money_spent_eur, avg_energy, avg_mood, avg_sleep_h, completion_rate.
Sections: hours per track against budget (table), trends, the one pattern that cost the most, milestones due, changes for next week, a state snapshot a new chat can start from.

## Paths
- Daily logs: `Daily/YYYY-MM-DD.md`. Sunday reviews: `Weekly/YYYY-Www.md`. Track notes: `Tracks/`.
