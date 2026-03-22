# PULSE DASH — Game Design Document

## 1. Elevator Pitch
**Tap to dash through an endless neon corridor of rhythmic obstacles, chaining combos and collecting light orbs in 15-second bursts that feel like swiping through the best TikTok feed.**

## 2. Core Fantasy / Theme / Target Audience
- **Theme:** Neon synthwave runner — the player is a pulse of light dashing through a digital corridor
- **Fantasy:** You ARE the beat. Every tap syncs with the rhythm of the world
- **Target Audience:** 13-35, casual mobile gamers, TikTok/Instagram users, anyone with 5 minutes to kill
- **Art Style:** Dark background, vibrant neon gradients (cyan, magenta, gold), particle trails, screen shake

## 3. Core Loop (7 Steps)

1. **SEE** — An obstacle pattern slides toward you (walls with gaps, moving barriers)
2. **TAP** — Player taps to dash/switch lanes (left side = go left, right side = go right)
3. **FEEDBACK** — Neon trail burst, satisfying "whoosh" sound, screen pulses
4. **COLLECT** — Orbs in the path are auto-collected (coins + XP)
5. **COMBO** — Consecutive near-misses and orb chains build a combo multiplier (x2, x3... x10)
6. **VARIABLE REWARD** — 5% chance of golden orb (10x value), 2% chance of "SUPER DASH" mode (invincible + magnet for 3 seconds, screen goes wild with particles)
7. **NEXT** — The next obstacle is already visible and approaching. Zero pause. The corridor never ends.

**Format:** Player taps to dodge → instantly sees neon burst + hears whoosh → may trigger SUPER DASH or golden orb → next obstacle already incoming, tap again.

## 4. Example Round (20 seconds)

> **0s:** Round starts. You're a cyan light pulse. A wall with a right gap approaches.
> **2s:** Tap right side. SWOOSH. You dash through, collecting 3 orbs. "+15" floats up. Combo: x1.
> **4s:** Two walls in sequence — gap left, then gap right. Tap-tap. "Nice!" text. Combo: x2.
> **7s:** A moving barrier oscillates. You time the tap perfectly — NEAR MISS! Screen shakes. "+50 CLOSE CALL!" Combo: x3.
> **10s:** Golden orb appears in the next gap. Tap through. "GOLDEN!" — 150 points. Combo: x4. The corridor shifts to magenta.
> **13s:** Three rapid walls. Tap-tap-tap. "INCREDIBLE x5!" Particles everywhere.
> **16s:** A narrow double-barrier. You tap... slightly off. CRASH. Your light pulse shatters into particles. "Nice run! 485 pts" Score floats up. The corridor reassembles in 0.5 seconds. You're already playing again.

## 5. Progression & Rewards

### Short-term (per action / per round, every 5-20 seconds)
- Orbs: 5-15 per dodge (multiplied by combo)
- Score counter climbing
- Near-miss bonuses: +50 points
- Combo text: "Good!" "Great!" "Incredible!" "LEGENDARY!"
- Visual: trail color intensifies with combo

### Medium-term (per 5-10 minutes)
- XP bar fills → Level up (every ~3-5 minutes of play)
- Level-up screen: quick flash "LEVEL 7!" with new particle effect
- Every 5 levels: unlock a new color theme (Synthwave, Ocean, Sunset, Toxic, Ice, Lava, Galaxy)
- High score notifications: "NEW BEST! 2,340"
- Milestone orb counts: every 500 orbs = bonus animation

### Long-term (per day / per week)
- Daily streak counter (just a number, no punishment for missing)
- "Welcome back" bonus: +100 orbs if you were away 4+ hours
- Collection: 12 themes to unlock, each with unique particle colors
- Mastery meter: tracks total distance traveled (endless, always growing)
- Weekly challenge: "Reach combo x8 this week" → bonus theme unlock

## 6. Session Design

### Friction Removal
- NO title screen on repeat plays — tap anywhere = instant start
- Death → 0.5s particle explosion → corridor reforms → you're playing. No "retry" button
- No loading screens. Everything is procedurally generated
- Score/level always visible, never interrupts gameplay

### Soft Failure
- Death animation is SATISFYING — your light pulse explodes into beautiful particles
- Funny/encouraging death messages rotate: "So close!" "Almost had it!" "The corridor respects you"
- Your score and combo are shown briefly, then gone — no dwelling on failure

### "One More Round" Hooks
- After death, the next round's first obstacle is already sliding in — you're playing before you decide to
- "Your best: 2,340. This run: 2,280" — so close, gotta beat it
- Combo near-misses: "You hit x7 that run, x8 unlocks a bonus!"
- New theme preview: "3 more levels to unlock GALAXY theme"

### Adaptive Difficulty
- Tracks your success rate over last 20 obstacles
- Above 85% success → speeds up, adds complexity (moving barriers, narrower gaps)
- Below 60% success → slows down, widens gaps
- Target: keep player at 70-80% success rate (flow state)

## 7. Ethical Guardrails

- **Break reminders:** After 15 minutes of continuous play, a gentle message: "You've been dashing for 15 min. Take a stretch?" (dismissible, non-blocking, shown once per 15-min block)
- **No pay-to-win:** All themes are earnable through play. No premium currency
- **No gambling:** No lootboxes, no gacha, no random purchases. SUPER DASH is a free in-game event
- **Welcome back bonus:** 4+ hours away = +100 orbs. Rewards breaks, doesn't punish them
- **No streak punishment:** Daily streak counter goes up but missing a day just pauses it, doesn't reset
- **Session stats:** Optional "your stats" showing time played today (informational, not shaming)
- **No ads in this version:** Pure gameplay. Monetization (if any) would be cosmetic-only theme packs
