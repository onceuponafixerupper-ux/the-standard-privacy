# Gameplan — Phone-Down App (working title: **"Off"** / **"Locked In"** / **"Hold"**)

> Turn your phone off, prove it, and let your brain heal. The flex isn't your screen time — it's how little of it you have.

_Draft v1 · 2026-06-07_

---

## 1. The one-liner

A dead-simple app that puts your phone into a real, locked "do-not-disturb / focus"
state, tracks how your phone habits change over time, and turns *being off your phone*
into a social flex. People know they *should* do this manually — they won't. We make it
one tap, make it provable, and reward it (hit your daily goal consistently → the app
becomes **free**).

---

## 2. Why this works — the science (this IS the marketing)

Every claim below is backed by a real study. These are the lines we put on the landing
page and App Store screenshots, because "why should I download this" is answered by
*what it does to your brain*.

### a) Your phone drains your brain just by being *near* you
The landmark **"Brain Drain"** study (UT Austin, ~800 people, _Journal of the Association
for Consumer Research_, 2017) found that the *mere presence* of your own smartphone —
face-down, silent, untouched — measurably **reduces available working memory and fluid
intelligence**. The effect is **largest for the most phone-dependent people**. The act of
*not* checking it consumes cognitive bandwidth.
→ **Pitch line:** "It's not the scrolling. Just having it on the desk makes you dumber. We get it out of reach."

### b) Notifications wreck attention even when you don't touch them
Multiple studies show notifications harm attention and cognitive control *without you
even picking up the phone*. People respond slower and show measurable changes in brain
activity (N2/P2 ERP) on tasks paired with notification sounds. Task-switching from a
single buzz fragments focus.
→ **Pitch line:** "One buzz and you're gone. We silence the buzz at the source."

### c) It takes ~23 minutes to refocus after one interruption
Classic attention research: after an interruption it takes about **23 minutes** to return
to full focus. A handful of notifications can mean you never actually reach deep focus all
day.
→ **Pitch line:** "A 5-second glance costs you 23 minutes. Do the math on your day."

### d) Blocking your phone measurably improves attention & mental health
A 2025 **PNAS Nexus** randomized study: blocking mobile internet on phones for two weeks
**improved sustained attention, mental health, and subjective well-being** — the
attention gain was equivalent to reversing several years of age-related decline.
→ **Pitch line:** "Two weeks. Measurably sharper. Clinically, not vibes."

### e) Phones at night destroy sleep; cutting them back rebuilds it
A randomized trial found restricting phone use before bed for 4 weeks **reduced time to
fall asleep, increased sleep duration, improved sleep quality, and improved working
memory and mood**. Blue light suppresses melatonin.
→ **Pitch line:** "Your worst sleep starts with 'just one more video.'"

### f) A short detox starts rewiring the dopamine system
Reporting on recent neuroscience: even a ~72-hour break begins shifting dopamine
responses, so deep concentration stops feeling impossible. Constant rapid-fire phone
stimulation raises the bar for what feels rewarding; stepping back resets it.
→ **Pitch line:** "Your attention span isn't broken. It's overstimulated. This resets it."

**Sources (put these in an in-app "The Science" page for credibility):**
- Brain Drain — mere presence reduces cognitive capacity: https://www.journals.uchicago.edu/doi/full/10.1086/691462 · summary: https://news.utexas.edu/2017/06/26/the-mere-presence-of-your-smartphone-reduces-brain-power/
- Notifications harm cognitive control (PLOS One): https://journals.plos.org/plosone/article?id=10.1371/journal.pone.0277220
- Notifications harm attention (EU-JER): https://www.eu-jer.com/articles/EU-JER_11_3_1487.pdf
- Blocking mobile internet improves attention & well-being (PNAS Nexus, 2025): https://academic.oup.com/pnasnexus/article/4/2/pgaf017/8016017
- Restricting bedtime phone use improves sleep & working memory: https://www.ncbi.nlm.nih.gov/pmc/articles/PMC7010281/
- Digital detox / brain rewiring overview (Georgetown): https://www.georgetown.edu/news/digital-detox-reduce-screen-time-benefits/

> **Honesty rule:** we cite real studies and don't overclaim. "Associated with / shown to
> improve" — never "cures." Trust is the brand.

---

## 3. What the app actually does (core loop)

1. **Onboarding (60 sec):** pick a daily goal ("≤ 2h screen time" or "3 locked focus
   sessions"). See your *current* baseline so the before/after is visceral.
2. **One-tap Lock:** big button → phone enters a real focus/blocked state. Distracting
   apps are shielded; notifications go quiet. A timer runs.
3. **Don't cheat:** if you bail early or disable it, the session fails (and you don't earn
   the reward). Optional "hardcore" mode makes leaving cost you the streak.
4. **Track the change:** daily/weekly view of pickups, screen time, notifications, and
   locked-focus minutes — **then vs. now**. The hero metric is the *downward trend*.
5. **Earn it:** hit your goal consistently (e.g. 7 days) → **app goes free** (see §4).
6. **Flex it:** share a clean "I was off my phone X hours this week" card; climb a
   friends leaderboard. Proof-of-absence is the status symbol.

---

## 4. The "earn it free" mechanic (the hook) — design + cautions

**Concept:** consistently hit your daily limit *with the phone genuinely locked* (timer
can't be turned off / tampered with) → subscription becomes **free**. You literally pay
with your attention, not your wallet.

**Proposed rule (tunable):**
- Define a "qualifying day": ≥ N locked-focus minutes **OR** under your screen-time cap,
  verified by the OS, with no tamper/disable events.
- Hit qualifying days **X of last 7** (e.g. 6/7) → next week is **free**.
- Miss the streak → revert to paid until you re-earn it. Keeps people engaged.

**Why it's powerful:** flips the usual incentive. Most apps profit when you use your phone
*more*. We profit (in goodwill + virality) when you use it *less*. That's the story.

**⚠️ Things to design around before we ship this:**
- **App Store guideline risk:** Apple/Google scrutinize subscription mechanics and
  anything that conditions price on behavior. Likely cleanest implementation: a normal
  subscription + an automatic, fully-disclosed **"focus credit"** that discounts/comps the
  next period. Get this reviewed early.
- **Anti-cheat:** "locked + can't turn off timer" is the integrity core. iOS can shield
  apps and detect when shielding is removed; we log tamper events. We can't make iOS
  literally un-exitable, so the rule must be "tamper = day doesn't qualify," not "app
  physically traps you."
- **Unit economics:** if power users go free forever, what funds it? Options: paid tier
  for people who *don't* hit goals (the ones who need it), one-time unlock, team/【B2B】
  (schools, employers) wellness licenses, or sponsorship. **Decide before launch.**
- **Ethics/safety:** never punish in a way that strands someone in an emergency. Locking is
  *app-shielding*, never blocking calls/SOS/maps. Make that loud in the UI.

---

## 5. Social / community — "proof is the flex"

- **Friends & streaks:** add friends, see who's most off-phone this week. Compete on
  *absence*, not presence.
- **Shareable proof cards:** auto-generated image — "🔒 11h 20m off my phone this week,
  pickups down 38%." Built for stories/group chats. This is the growth engine.
- **Verified, not self-reported:** numbers come from the OS, so the flex is real. A "✓
  verified by device" badge.
- **Groups/challenges:** "Dorm vs dorm," "team no-phone Sunday," friend pacts. Group goals
  → referral loop → free for everyone who hits it.
- **Privacy by default:** sharing is opt-in; you choose what's visible. (Mirrors the
  existing privacy-first DNA in this repo's policy.)

---

## 6. Technical reality (this shapes everything — read before building)

### iOS (recommended starting platform — reuses the existing Apple/Swift/Supabase stack)
- **Frameworks:** `FamilyControls` (ask permission + pick apps), `ManagedSettings` (shield
  apps/web), `DeviceActivity` (schedule restrictions + threshold monitoring),
  `DeviceActivityReport` (display usage). Reference:
  https://developer.apple.com/documentation/screentimeapidocumentation
- **The big constraint:** for privacy, **your app never learns *which* apps the user
  selected** — selections are opaque tokens, and usage data can only be *rendered* inside
  a sandboxed report extension, not read as raw numbers by your main app. So "track
  exactly what they do now" is **limited on iOS** — we get aggregate trends and
  thresholds, not "you spent 47 min on TikTok" pulled into our DB.
- **Entitlement:** the Family Controls "distribution" entitlement must be **requested from
  Apple** and approved — apply for this **on day one**, it can gate launch.
- **DND/Focus:** we can't silently flip the system Focus, but **shielding apps +
  scheduled DeviceActivity is effectively stronger** (the distracting apps literally won't
  open). Frame this as the feature, not a limitation.

### Android (phase 2 — more open, better for "track what they do now")
- `UsageStatsManager` gives **per-app time, unlocks, and notification counts** (with user
  permission) — richer baseline data than iOS. App-blocking via accessibility/overlay
  services. Note: third-party access is typically limited to ~recent weeks of history.

### Backend
- Reuse **Supabase** (already in this ecosystem): Apple/Google sign-in, Row-Level
  Security, sync, friends/leaderboard tables, streak + reward state.
- **Local-first** like the existing app: works offline, syncs when signed in.

### Cross-platform later
- SwiftUI native for iOS v1 (best Screen Time integration). Consider Flutter/RN only if/when
  Android demands shared code — but the OS integrations are platform-specific regardless.

---

## 7. UX principles (the user asked for clean + simple)

- **One job per screen.** Home = one giant Lock button + today's streak. That's it.
- **The number that matters is the trend, going down.** Big, calm, obvious.
- **Calm, not gamified-casino.** Muted palette, lots of whitespace, one accent color.
  (The existing privacy page already has a nice warm palette — terracotta/cream/sage — we
  can carry that brand language.)
- **Reward feels earned, not bought.** When the app goes free: a quiet, classy moment.
- **No dark patterns.** We're the *anti*-attention-economy app; the UI must prove it.

**Screen list (v1):**
1. Onboarding + baseline reveal
2. Home (Lock button + streak + today)
3. Active focus session (timer, "you're off, nice")
4. Insights (then vs now: pickups, screen time, focus minutes, trend)
5. Friends / leaderboard + share card
6. Reward / streak status ("3 more days → free")
7. The Science (credibility page with citations)
8. Settings (goals, hardcore mode, what's shared, SOS always-allowed notice)

---

## 8. Data model (first cut)

- `user` (id, auth, display name, created_at)
- `goal` (user_id, type [screen_cap | focus_sessions | focus_minutes], target, active)
- `session` (user_id, started_at, ended_at, planned_minutes, completed bool, tamper_events int, qualified bool)
- `daily_summary` (user_id, date, screen_time_min, pickups, notifications, focus_min, qualified_day bool)
- `streak` (user_id, current_len, best_len, last_qualified_date, reward_state [paid | earned_free | grace])
- `friendship` (user_id, friend_id, status)
- `share_card` (user_id, period, stats_json, created_at)

(iOS aggregate metrics that can't leave the report extension are stored as *user-confirmed
summaries* / derived qualifying flags, not raw per-app rows.)

---

## 9. Roadmap

**Today (a runnable, demoable slice):**
- [ ] Repo scaffold (SwiftUI app or a clickable web/Expo prototype to validate UX fast)
- [ ] Onboarding → goal → home screen with the big Lock button
- [ ] Local focus-session timer + "don't leave" logic (logical lock first)
- [ ] Insights screen with mock then-vs-now data
- [ ] "The Science" page with the citations above
- [ ] Reward/streak logic (local), share-card generator
- [ ] **File the Apple Family Controls entitlement request** (long lead time)

**Week 1–2:**
- [ ] Real Screen Time integration (FamilyControls/ManagedSettings/DeviceActivity)
- [ ] Supabase auth + sync + friends/leaderboard
- [ ] Tamper detection → qualifying-day logic → real reward gating

**Later:**
- [ ] Android (UsageStatsManager + blocker)
- [ ] Groups/challenges, B2B/school licensing, polish

---

## 10. Open decisions (need your call before/while we build)

1. **Platform for v1:** iOS-first (recommended — matches your existing Apple/Swift/Supabase
   stack and has real app-blocking) vs. cross-platform vs. fastest-possible web prototype
   to nail the UX today.
2. **Name + brand.** Candidates: *Off*, *Locked In*, *Hold* (ties to "Hold the Standard"),
   *Unplug*, *Away*. Pick one so we can scaffold.
3. **Reward economics:** what funds "free for the disciplined"? (paid-for-strugglers /
   one-time unlock / B2B / sponsor)
4. **"Locked" strictness:** logical lock (tamper = doesn't count) vs. hardcore. iOS can't
   physically trap a user — confirm we're OK with "tamper-detected, not tamper-proof."
5. **Reuse this repo or start a fresh one?** This repo currently only hosts a privacy
   policy page; the app likely wants its own repo.

---

## 11. Risk register (quick)

| Risk | Mitigation |
|---|---|
| Apple rejects behavior-conditioned pricing | Model it as subscription + disclosed auto-credit; pre-check with App Review |
| Family Controls entitlement delay | Apply day one; build UX with mock data meanwhile |
| iOS hides per-app data → weaker "what you do now" | Lean on aggregate trends + Android for detail; honest framing |
| "Free forever" kills revenue | Decide monetization (§4) before launch |
| Safety (locking during emergency) | Never block calls/SOS/maps; loud disclosure |
| Looks like every other screen-time app | Differentiator = *earn-it-free* + *proof-is-the-flex* social layer |
