# KeepUp — Your AI Fitness Referee 📱

<p align="center">
  <b>Set up your phone, aim the camera, and let KeepUp do the rest.</b><br>
  No smartwatch. No fitness band. Just your phone, counting every rep.
</p>

<p align="center">
  <a href="README_zh.md">中文</a>
  &nbsp;·&nbsp;
  <a href="http://123.56.229.196:18443/keepup"><b>👉 Download KeepUp 👈</b></a>
  &nbsp;·&nbsp;
  <a href="https://github.com/jumppppp/KeepUP">GitHub</a>
</p>

---

## 🆕 v1.1.0 — Motion Engine v2.2

**14 expression functions** + ternary operator + config system. [Full changelog](https://github.com/jumppppp/KeepUP/releases)

| Category | Functions |
|----------|-----------|
| Math | `abs` `sqrt` `pow` `min` `max` |
| Trig | `sin` `cos` *(degrees, `sin(90)=1.0`)* |
| Distance | `distance` `distance3d` |
| Angle | `angle` `angle3d` |
| Midpoint | `centerX` `centerY` |
| Conditional | `? :` |

> AI Smart Detect now with 3-layer softmax noise filter — no more false positives when idle.

---

## 🤖 How It Tracks You

Just train with your camera on. KeepUp's AI pose estimation engine tracks **33 skeletal keypoints** in real time, accurately judging every rep.

- Did you squat deep enough? It knows.
- Did your chin clear the bar? It's tracking.
- Are you sagging during that plank? It sees everything.

**🧠 AI Smart Detect (new!)**: No need to pick an exercise — just start moving and KeepUp recognizes what you're doing. Batch-detects multiple exercises in a single session, each with its own skeleton replay video.

> More strict than a gym trainer. Sharper than your significant other. More obsessed with your form than your mom.

<p align="center"><img src="img/detection.png" width="320" alt="AI counter"> &nbsp; <img src="img/record.png" width="320" alt="Workout records"></p>

---

## 🎯 39 Exercises, No Two Days Alike

Whether you're a gym beast, a Pilates enthusiast, or someone who "just needs to stretch because sitting hurts":

| Category | Exercises |
|----------|-----------|
| 🔨 Strength (12) | Pull-up, Push-up, Squat, Lunge, Handstand Push-up, Shoulder Press, Bicep Curl, Tricep Dip, Glute Bridge, Lateral Raise, Punch, Dynamic Archery |
| 🔥 Cardio (5) | Burpee, Jumping Jack, High Knees, Mountain Climber, Tuck Jump |
| 🧊 Static (5) | Plank, Wall Sit, Hollow Hold, Handstand Hold, Archery Hold |
| 🏋️ Core (3) | Crunch, Russian Twist, Leg Raise |
| 🧘 Stretch (13) | Cat-Cow, Child's Pose, Cobra Stretch, Wall Angels, Neck Side Stretch, Cross-Body Shoulder Stretch, Overhead Tricep Stretch, Behind-Back Chest Stretch, Doorway Chest Stretch, Standing Hamstring Stretch, Wall Calf Stretch, Lunge Psoas Stretch, Reverse Nordic Curl |
| ✏️ Custom (1) | Custom Workout — track whatever you want |

> 39 exercises across 6 categories. Monday pull-ups, Tuesday squats, Wednesday burpees until you question life, Thursday stretch therapy. KeepUp doesn't force you — but your friends will "check in" if you ghost for 3 days.

---

## 🧠 Expression Engine: Write Your Own Exercise Rules

KeepUp's motion detection engine uses a **custom expression language** for defining exercise phases. Templates are JSON — change them without recompiling the app.

```json
// Squat DOWN phase: both knees bent to ~90°
"expr": "min(leftKneeAngle, rightKneeAngle) < 100"

// Body alignment (plank): shoulder-hip-ankle in a straight line
"expr": "abs(angle(shoulderMid, hipMid, ankleMid) - 180) < 10"

// Self-calibrating threshold
"expr": "wristDistance < shoulderWidth * 1.5"
```

**14 functions**: `abs` `sqrt` `pow` `min` `max` `sin` `cos` `distance` `distance3d` `angle` `angle3d` `centerX` `centerY` + ternary `? :`

---

## 🪙 Train Harder, Earn More

A full virtual economy:

```
🥉 Bronze → 🥈 Silver → 🥇 Gold → 💎 Platinum
  100 bronze = 1 silver = 10,000 bronze = 1 gold = 1,000,000 bronze = 1 platinum
```

How to earn? Just train:

- 1 pull-up = **10 bronze** (hardest, top reward)
- 1 burpee = **7 bronze** (heart-rate nightmare, well earned)
- Plank 10s = **5 bronze** (endurance game, slow grind)
- Stretch 10s = **1 bronze** (recovery mode, don't expect to get rich)

> Fair principle: harder = more reward. Want to plank your way to platinum? See you in the next life.

<p align="center"><img src="img/reward.png" width="320" alt="Training reward"></p>

---

## 👀 Check on Your Friends

KeepUp's soul — **social pressure**:

- **🏟️ Feed**: Post workouts with photos. "100 push-ups ✅" — showing off is the #1 gym motivator.
- **🏆 Leaderboard**: Global wealth ranking + per-exercise leaderboards. Filter by gender. "She did more pull-ups than me? Time for an extra set."
- **👤 Profile**: Tap a friend's avatar. Their reps, bio, feed, all exposed. "You said we'd train together. Where's your post?"
- **💬 DMs**: Nudge friends: "👀 3 days no activity..."

> Skip one day, you know. Skip two, KeepUp friends know. Skip three — your inbox explodes.

<p align="center"><img src="img/leaderboard.png" width="320" alt="Leaderboard"> &nbsp; <img src="img/wealth.png" width="320" alt="Wealth ranking"></p>

---

## 📊 Summary: Your Annual Fitness Report

Day / Week / Month / Quarter / Year — dig up the past anytime:

- 🗓 **Streak**: Consecutive training days. Breaks reset to zero — stricter than any game login bonus.
- 📈 **Bar Charts**: Which day you slacked off = instantly visible.
- 🏅 **Top Exercises**: Are you truly devoted to pull-ups, or just flirting?
- 💪 **Body Part Distribution**: Skipping leg day? The chart snitches.
- 🥇 **Personal Records**: On some date, you did 15 pull-ups. History remembers.
- 💰 **Wealth Curve**: Earned coins over time (earning only, spending TBD).

> Look back at year's end: "Oh, I actually trained on March 12." That's an achievement too.

<p align="center"><img src="img/summary.png" width="320" alt="Summary"></p>

---

## 🎬 Skeleton Animation Replay

For camera-based exercises, KeepUp auto-records a **stick-figure animation video**.

Not regular screen recording — it's a motion-traced skeleton showing every joint's path. Where your form broke, where you cheated — replay reveals all.

> Post it on social media with "✓ Done" — one dimension above bathroom mirror selfies.

---

## 💰 My Assets: Your Fitness Bank

<p align="center"><img src="img/profile.png" width="320" alt="Profile page"></p>

Asset dashboard at a glance:
- 💎🥇🥈🥉 Four-tier currency display
- Total workout count (numbers don't lie)
- Consecutive training days (treasure them)
- Quick access: training records / summary / messages

---

## 🔐 Your Data, Your Rules

- Full-chain AES-256 encryption — intercepted? Gibberish.
- Private workouts? Set them private — your eyes only.
- Even admins can't read your messages (not that you're gossiping much).

---

## 🚀 Changelog — No BS

Every update shows what actually changed:

> ❌ "Bug fixes and improvements"
> ✅ "Jumping jacks no longer count twice per jump"
> ✅ "Expression engine: 14 new functions for custom exercise templates"
> ✅ "AI Smart Detect: 3-layer filter eliminates false positives when idle"

We promise: never "fixed some known issues" you.

---

<p align="center">
  <b>KeepUp — Train or admit you didn't. 🏋️</b><br><br>
  <a href="http://123.56.229.196:18443/keepup">📥 Download KeepUp</a>
  &nbsp;·&nbsp;
  <a href="https://github.com/jumppppp/KeepUP">⭐ Star on GitHub</a>
</p>
