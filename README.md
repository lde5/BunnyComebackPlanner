🐰 Bunny Comeback Planner
A NewJeans-inspired daily to-do app built in Python. Every day is a
"comeback," every task is a "track," and clearing your list earns you
Hype Points, Cookies, streaks, trophies, and new color "concepts" —
all designed to make finishing your list feel as satisfying as possible.
This is a fan-made project inspired by NewJeans and the Bunnies fandom.
It is not affiliated with, endorsed by, or sponsored by ADOR, HYBE, or
the group's members.
---
What's inside
⚠️ If you tried alarms before and they didn't work: the time picker had
a bug where it defaulted to 9:00 AM regardless of what time it actually
was — so creating an alarm any time after ~9:30am meant its deadline had
already passed the instant you saved it, which also meant the ringing
pop-up (and its sound) never got a chance to fire at all. That's fixed:
you now type the exact time, it's pre-filled to a sensible near-future
default, you get live feedback as you type, and saving an alarm whose
time has already passed is now a hard error with a clear explanation
instead of a silent trap. There's also a one-click Test alarm sound
button in Settings and in the alarm editor so you can confirm audio
works on your machine before trusting it.
Core to-do features
Tasks with priority (Low/Medium/High/ASAP), categories, due dates, notes
Subtasks/checklists for breaking big tasks into smaller steps
Recurring tasks (Daily / Weekdays / Weekly / Monthly) that regenerate
automatically when completed
"Quick win" flag for anything that takes 2 minutes or less
Search and filter (Active / Completed / All) in the Full Album view
Motivation & anti-procrastination systems
Alarm tasks — real stakes ⏰ — turn any task into a scheduled alarm.
Type the exact time (or use the +15min/+30min/+1hr/+2hr quick-set
buttons), with live feedback confirming exactly when it'll ring. When
it hits, the app rings — sound plus a topmost pop-up, and it flashes
your taskbar icon too — until you hit Start, which begins a
countdown you also set (up to 3 hours). Hit Finish before it runs
out and you get a bonus on top of the normal reward; let it expire —
or never start it at all — and you lose Hype Points, Cookies, and
your streak. Dismissing the pop-up doesn't cancel the deadline, and if
you keep dismissing it, it comes back faster and rings more
insistently each time.
Locked-In Focus Sessions 🔒 — an optional toggle on the Studio
Session page. With it on, starting a Studio Sprint is a real
commitment: bailing out early (hitting Reset, or switching modes)
before the timer finishes costs you Hype Points and Cookies. Pausing
doesn't count against you — only actually abandoning it does. Off by
default; turn it on when you want the extra pressure.
Daily/Weekdays tasks have teeth — leave a Daily or Weekdays
recurring task unfinished and you lose Hype Points, Cookies, and your
streak for it too, checked automatically while the app is open. Weekly
and Monthly recurring tasks, and regular one-off tasks, are
deliberately exempt — those still get the gentle, no-punishment
stuck-task check-in below.
The bunny actually talks to you 🐰 — a speech bubble by the mascot
that rotates through contextual nudges: calling out overdue tasks by
name and count, celebrating a hot streak, or just nagging you to start
something when the list is sitting untouched. Tune how often in
Settings (Off / Gentle / Persistent).
Today's Brief — once a day, the first time you open the app, a
quick pop-up greets you with what's on deck, your streak, your rank,
and your comeback countdown if you've set one — a deliberate "here's
the plan" moment to kick the day off.
Hype Points & Bunny Levels — every completed track earns XP and
levels you up through rank titles like Trainee Bunny → Certified
Bunny → Comeback Icon → Legendary Bunny
Cookies — a currency earned alongside XP, spendable on streak
freezes and bonus color concepts
Streaks with Streak Insurance — keep a daily streak alive; a
streak freeze (buyable with Cookies) automatically protects it if you
miss exactly one day. A penalty (from a missed alarm, an abandoned
locked-in sprint, or a missed daily/weekday task) always breaks the
streak regardless, even if a freeze is available — insurance covers
forgetting, not an active miss.
Trophy Case — 12 unlockable achievements, from Debut Stage
(your first task) to Legendary Bunny (a 30-day streak)
Comeback Countdown — set a big goal (finals week, a launch, a
deadline) and get a D-day style countdown (D-7, D-1, D-DAY)
Studio Session focus timer — Pomodoro-style Studio Sprints and
Green Room / Tour Bus breaks that earn extra Hype Points, with an
"always on top" option and optional Locked-In stakes (above)
Gentle stuck-task check-ins — for regular and Weekly/Monthly
tasks, when the app opens with overdue ones it offers to reschedule,
break the task down, or drop it — no penalty, just a nudge
Celebration pop-ups with confetti for level-ups, new trophies, and
unlocked concepts; a lighter toast for everyday completions; and an
honest (not harsh) notice when something gets missed, showing exactly
what was lost
End-of-Day Recap — a one-click summary of what you cleared today
Make it yours
Five unlockable color "concepts," each loosely inspired by a different
era/comeback: Attention, OMG, Super Shy, Get Up, How Sweet
Custom background — pick any photo from your PC in Settings and
it becomes the backdrop behind your tracklist, automatically tinted
for legibility. Swap it or remove it any time.
A tracklist-style layout (today's tasks are numbered like an EP), a
Chart Performance page with a weekly bar chart, and an evolving bunny
mascot that gains accessories as you level up
Fandom-flavored language throughout (Bunnies, Hype Points, Trophy
Case, Studio Sessions) without using any official artwork, logos, or
lyrics
---
Notes
Alarm tasks and the Daily/Weekdays penalty need the app to be open
to fire — this is a desktop app, not a background service, so it can
only ring or apply a penalty while it's running. Leave it open
(minimizing is fine) if you're relying on an alarm going off. This
version checks every 5 seconds, so it should catch a due alarm almost
immediately rather than making you wait.
Sound effects and the taskbar-flash attention-getter use Windows-only
APIs (`winsound` and `FlashWindowEx`) and only work on Windows; on
other platforms they're silently skipped rather than erroring.
We deliberately didn't add real Windows toast/Action Center
notifications. It's possible in principle, but the reliable ways to do
it need either a new dependency or fragile PowerShell/COM tricks that
are known to silently fail without proper app registration — exactly
the kind of "looks like it should work but doesn't" problem you just
ran into with the alarm, and we didn't want to risk shipping another
one. The in-app pop-up (sound + topmost + taskbar flash) is the
reliable version of that same idea.
The custom background is tinted toward your current color concept so
text stays readable — very bright or busy photos will look muted by
design, not broken.
You can back up or wipe your data any time from Settings.
Everything runs 100% locally — no account, no internet connection
required after the one-time package install.
