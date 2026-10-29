# Praenox Pro
**Biometric Sound Synthesis — Arlej Tech**

Web Praenox: https://praenox.com
---
Web Arlej Tech: https://arlejtech.com
---

## What Is Praenox Pro?

Praenox turns your saved health data into a reproducible therapeutic soundscape:

`Health day → Biometric fingerprint → Generated soundscape → Play / Export / Feedback / Milestones`

Praenox Pro is the full engine: continuous fingerprint-based synthesis, a three-stage predictive layer (Fusion) that learns your trends over weeks, an Outcome Learning system that tracks whether each session actually helped, a personal sleep optimizer, and a full points/levels/streaks/badges system.

**One-time purchase. Lifetime licence.** No subscription.

## Before You Start — Important

**Always use earbuds or headphones. Never speakers.**

Praenox uses binaural beats, layered frequencies, and stereo-panned audio that only work correctly when each ear receives a separate channel. On speakers the layers collapse into each other and the effect is lost. In-ear earbuds give the best result; over-ear headphones also work well.

## License Required

Praenox Pro **cannot be used without a valid license.** This is different from Praenox Free, which needs no license at all.

On launch, Pro shows a license prompt before you can enter the app. You must enter a valid key to continue — there's no limited or trial mode without one.

After purchasing (via Buy Me a Coffee), you'll receive your key by email, typically within 24 hours. Enter it exactly as sent when prompted. Keep it somewhere safe — you'll need it again if you reinstall or move to a new machine.

## Windows Security Warning — Why Does It Appear?

When you download or run Praenox Pro for the first time, Windows may show a warning:

- **Browser:** "Keep" / "Delete" prompt when downloading
- **SmartScreen:** "Windows protected your PC" before running

This is expected. The app is safe. It appears because Praenox is not signed with a paid code-signing certificate — a system where developers pay a Certificate Authority to verify their identity so Windows trusts the app automatically. There is no malware, no virus, no hidden code.

To run it:
1. When the browser prompts "Keep" or "Delete" — click **Keep**.
2. If SmartScreen appears — click **More info**, then **Run anyway**.

You only need to do this once. Windows remembers your choice after the first run.

## App Overview

| Section | Purpose |
|---|---|
| Home | Entry screen, navigation hub, first-run guide |
| Generator | Save/select health days, choose palette/style/duration, generate soundscapes, mark listened/skipped |
| Charts | Compare saved days and graph health trends over time |
| Player (Immersion) | Play saved soundscapes only — does not generate new sessions, does not award points |
| Data Vault | Import/export health history, local backups, full profile export |
| Milestones | Points, levels, streaks, shields, badges, export confirmation, sick/vacation controls |
| Profile | User identity, HRV reference context, multi-user management |

## Step-by-Step Workflow

1. Go to **Generator**.
2. Enter a manual health day, or select an existing saved day. HRV is the only required field, but deep sleep %, REM %, resting HR, stress score, and sleep duration all feed generation.
3. Save/update the day.
4. Select the saved day.
5. Choose palette (20 categories — Nature, Ocean, Fire, Instruments, Solfeggio, Tibetan Bells, and more), music style (16 styles across Grounding / Meditative / Expressive / Energetic, or Auto), and duration.
6. Click **Generate**.
7. Play in Immersion or export the soundscape.
8. After real use, come back and mark **LISTENED** or **SKIPPED** — this feeds Outcome Learning and your Milestones points.

Once generated, the health day **locks**: fields become read-only and the delete button is disabled. If you edit a locked day, Praenox asks for confirmation — the edit updates future generations only; the soundscape you already made keeps its original data permanently.

## How Generation Actually Works

Every health day produces a biometric **fingerprint** — each of the five input metrics drives a separate part of the synthesis (HRV shapes the primary binaural beat, resting HR shapes carrier frequency and breath pace, deep sleep % shapes sub-bass and delta layer weight, REM % shapes theta layer and solfeggio choice, stress shapes noise color and ambient intensity). A 1-unit change in any metric produces a measurably different result — the protocol name is a label on top of that continuous math, not a fixed bucket.

**Recovery Score** (0–100) is shown two ways: **CURRENT (live)**, recomputed against your latest baselines, and **SNAPSHOT (frozen)**, locked at the moment of generation and used for all playback/export going forward.

**Baselines** are auto-calibrated from your own history (median for HRV/HR/stress, 75th percentile for deep sleep and REM) and recalculate on every save or import.

**Protocols:**

| Protocol | Trigger |
|---|---|
| Maintenance | Recovery ≥ 70, no deficit detected |
| Delta Induction | Deep sleep deficit > 25% below target |
| Cortisol Reset | Stress load > 30% above baseline |
| REM Restore | REM deficit > 28% below target |
| Cardiac Calm | Resting HR elevation > 18% above baseline |
| Parasympathetic Restore | General multi-metric deficit, no single metric dominant |

The generation rationale always states *why* a protocol was chosen, for full transparency.

## Sleep Debt

Praenox uses your **personal** sleep baseline instead of a fixed 7-hour target: fewer than 14 samples uses a 420-minute fallback, 14–20 samples uses the 75th percentile of your own history, and 21+ paired nights uses a recovery-optimal target (the sleep window most correlated with your best next-day recovery).

Sleep debt mode only activates when three conditions are met at once: 4+ recent sleep samples, 3+ deficit nights in the last 7 days, and more than 360 minutes of accumulated debt. When active, it's the single highest-priority layer in the app — it overrides both Outcome Learning's preference weighting and any Fusion-forced protocol for that session, so a genuine recovery-debt night is never diluted by prediction or preference. Everything resumes normally once debt clears.

## Fusion — Prediction Engine

Fusion watches your biometric trends and escalates through three stages as your history grows:

| Stage | Unlocks at | Behavior |
|---|---|---|
| 1 — Signal | 0–20 HRV entries | Shows a Watch/Act banner. Nothing is forced. |
| 2 — Locked | 21–59 HRV entries | An Act signal force-applies a protocol; that session becomes preventive. |
| 3 — Predictive | 60+ HRV entries, accuracy > 40% | Predictive mode, with sub-labels: Calibrating (< 55%), Tuning (55–69%), Predictive (≥ 70%) |

A persistent **FUSION STAGE X** badge is always visible, and a progress indicator shows how many more entries until the next stage (e.g. "14 more HRV days until Stage 2 unlocks"). Fusion also tracks its own prediction accuracy — every time you mark a session listened or skipped, it compares its predicted next-day recovery against what actually happened, and adjusts its own thresholds over time.

## Outcome Learning

Praenox closes the loop between what it generates and what actually happens to you the next day. Once you mark a session **LISTENED**, the next day's real recovery score is compared to the frozen snapshot and classified as **Helped**, **Hurt**, **Stabilized**, or **Neutral**. (Skipped sessions are excluded — they say nothing about whether the combination works.)

Once a specific protocol, style, palette category, layer, or duration has at least 3 evaluated sessions, its accumulated verdict becomes a learned weight that gently reinforces what's worked for you and quietly de-emphasizes what hasn't — never all-or-nothing, since your biometrics can still call for something on a given day.

**Precedence, top to bottom:** Sleep Debt Delta Recovery → Fusion-forced protocol → Outcome-learned weighting → plain biometric fingerprint. Each layer only takes over if nothing above it is already deciding the session.

You can see all of this — the active layer for the selected day, live Fusion accuracy, and the full learning report — under **Learning Report** on the Home screen.

## Sleep Optimizer

Under the Planner tab, Praenox derives your personal optimal sleep target and gives bedtime/wake-time recommendations. Confidence is Low under 14 samples, Medium at 14–20, and High at 21+ paired nights (once it's using the recovery-optimal bucket analysis instead of a simple percentile).

## Milestones

Points are only ever awarded for an explicit, verifiable action — never for passively opening the Player. That means **Export** and self-reported **LISTENED** are the two ways to earn points; playing a soundscape in Immersion by itself awards nothing (it's also used for testing/verification, so passive playback intentionally isn't rewarded).

**Points:**

| Event | Points |
|---|---|
| Soundscape generated | +5 |
| Exported | +8 |
| Export confirmed listened | +13 |
| Health data entered | +10 |
| Sick day logged | +5 |
| Session skipped | −5 |
| Preventive session skipped | −8 |
| Missed day penalty | −10 |
| 3-day streak bonus | +20 |
| 7-day streak bonus | +50 |
| 14-day streak bonus | +75 |
| 30-day streak bonus | +150 |

Points floor at zero, and same-day duplicate entries/listens are blocked. **Streak shields** protect your streak automatically — you earn one every 7 streak days (max 2 held), and a shield fires on its own if you miss 2+ days.

**Levels** run from 1 (Newcomer, 0 pts) to 10 (Praenox Legend, 13000 pts), and higher levels unlock longer session lengths (45-minute at Level 3, 60-minute at Level 5).

**Badges** span five categories — Progression, Streaks, Resilience, Fusion, and Accuracy — including things like *First Listen*, *Week Warrior* (7-day streak), *Resilient* (listened on a low-recovery day), *Protocol Locked* (first Fusion Stage 2 force), and *Oracle* (Fusion accuracy above 82% over 30 days).

## Data Vault

- **Export health history** — full XLSX of your saved data.
- **Export full profile** — a ZIP with your health entries, baselines, Fusion profile, and Milestones progress, importable on another account/machine to reproduce the same recovery scores.
- **Automatic backups** — created every time you successfully generate a soundscape.

All data is stored locally on your machine. No health data is transmitted over the network.

## Multi-User Profiles

Praenox supports multiple users on one install. Each profile's health entries, soundscapes, achievements, and Fusion state are completely isolated from every other profile.

## Tips for Best Results

- Enter real data daily — Fusion and Outcome Learning both need consistent history to work well.
- Mark sessions **LISTENED** or **SKIPPED** after real use — this is what actually earns points and trains Outcome Learning.
- Listen at a comfortable, moderate volume, earbuds only.
- Protect your streak — shields help, but consistency is what the learning systems are built around.

## Frequently Asked Questions

**Can I use Pro without a license?**
No. Unlike Free, Pro requires a valid license key at launch before the app opens at all.

**What's the difference between CURRENT and SNAPSHOT recovery scores?**
CURRENT is recalculated live against your latest baselines. SNAPSHOT is frozen at the moment a soundscape was generated and is what playback/export always use — so a soundscape never silently changes after the fact.

**Why didn't playing a session in the Player give me points?**
That's intentional. Only Export and self-reported LISTENED count, since the app can't verify real-world listening from in-app playback alone.

**I lost my license key — what do I do?**
Contact Arlej Tech support with your purchase email and it'll be resent.

---
*Praenox Pro — Arlej Tech*
