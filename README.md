# DeciderHQ — IND vs WI T20 Decider Fan Hub

**Your match-day hub for the India vs West Indies 5th T20I series decider.**

Live demo: https://abhiramunni.github.io/deciderhq/

## What it does

DeciderHQ is a single-page fan experience built around a real fixture: the **India vs West Indies 5th T20I on Saturday, 17 October 2026, 7:00 PM IST at M. Chinnaswamy Stadium, Bengaluru** — the series decider with the contest level at 2–2. It gives cricket fans everything they need on match day in one attractive, animated page:

- **Cinematic stadium intro** — floodlight sweeps over a night crowd, tap-to-skip, auto-dismisses in ~4s
- **Live countdown** — flip-style tiles counting down to the first ball, plus a sticky match strip that follows you
- **The Predictor Game** — 5 predictions (winner, toss, total sixes, Player of the Match, first-innings total), saved on-device; after the match, pick the actual outcomes and get an auto-scored /100 scorecard with verdicts
- **The Series Story** — a timeline of all four T20Is so far (Lucknow, Ranchi, Indore, Hyderabad) with verified results
- **India's squad** — horizontal snap-scroll cards for all 16 squad members (captain + injury/cover notes)
- **Decider Quiz** — 8 questions mixing series facts and T20 know-how, with explanations for every answer
- **Conditions Watch** — rain/dew and Chinnaswamy pitch insight from pre-match reports, with plain-language tooltips
- **The Roar Meter** — a tap-to-fill stadium meter that erupts in canvas fireworks at 100
- **First-run onboarding** — a 3-step coach tour; helper text, tooltips, and friendly empty states throughout

## Who it's for

Cricket fans following the West Indies tour of India 2026 — from kids who just want to tap the Roar Meter to adults who want to test their prediction skills. Every screen is written in plain language.

## How to use

1. Open the live demo link above (works on phone and desktop, no install).
2. Tap through (or skip) the intro, then take the 3-step tour.
3. **Before the first ball:** play the Predictor Game — tap one option per question, hit *Save my predictions*. Your picks live only in your browser.
4. Scroll through the series story, squad, quiz, and conditions sections.
5. **After the match:** open the Predictor Game, tap *Score my predictions*, choose the actual outcomes from the dropdowns, and get your score out of 100.
6. Warm up your voice on the Roar Meter anytime.

## Match facts (verified 16 Oct 2026)

- 5th T20I: Sat 17 Oct 2026, 7:00 PM IST (toss ~6:30 PM), M. Chinnaswamy Stadium, Bengaluru — live on JioStar & JioHotstar
- Series 2–2; 4th T20I in Hyderabad: West Indies 247/3 (Shai Hope 102* off 50) beat India 223 by 24 runs (Keemo Paul 5-fer)
- India squad (16, per BCCI/Reuters): Shreyas Iyer (C), Abhishek Sharma, Vaibhav Sooryavanshi, Ishan Kishan, Sanju Samson, Tilak Varma, Shivam Dube, Kuldeep Yadav, Axar Patel, Ravi Bishnoi, Nitish Kumar Reddy, Arshdeep Singh, Prince Yadav, Mayank Yadav, Naman Dhir, Bhuvneshwar Kumar (added as cover)
- Pre-match reports flag rain/thunderstorm risk and heavy evening dew; chasing sides won 7 of the last 10 T20s at this venue

Sources: Reuters, Cricbuzz, CricTracker match coverage, 16 Oct 2026.

## Tech stack

- One self-contained `index.html` — no build step, no backend, no dependencies at runtime
- Canvas animations (intro floodlights, stadium hero, dew/pitch visuals, roar fireworks), CSS keyframe motion
- Fraunces + Inter typography (Google Fonts, with system fallbacks)
- `localStorage` for predictions, quiz best, roar best, and onboarding state — no accounts, no tracking

## Data & privacy

- Everything you enter (predictions, scores, taps) stays in your browser's `localStorage` under the `deciderhq_` key prefix. Nothing is sent anywhere.
- The page calls no APIs at runtime — fonts load from Google Fonts CDN. No analytics, no cookies.
- This is a fan-made hub, not affiliated with the BCCI, Cricket West Indies, or any broadcaster. Match facts are from public match coverage; the playing XI is named at the toss and this page doesn't guess it.
