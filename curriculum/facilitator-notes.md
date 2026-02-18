# Shipyard: Caleb's Cheat Sheet

Keep this on your phone or second monitor. The seminar guide has the actual script. This is for when things go sideways or you need a quick reminder.

## Pre-Session Checklist

- [ ] Test Zoom audio, screen share, camera
- [ ] Demo site open in a tab, ready to share
- [ ] Demo app open in another tab
- [ ] Student handout link copied to clipboard
- [ ] Backup screencast of a working GitHub Pages deploy (for when deploys break live)
- [ ] Pin your video so they see your face when you talk, your screen when you share
- [ ] Send pre-session email 24 hrs out (template in `curriculum/pre-session-email.md`)
- [ ] Confirm students made GitHub + Claude accounts (check replies to pre-session email)

## Claude Free Tier Warning

The free tier of Claude has message limits. Students who iterate a lot can hit the cap mid-session. Mitigation:
- Pre-session email tells students to sign up for Claude Pro free trial (no charge for first use)
- If someone hits the limit during the session, have them open an incognito/private browser window and create a new free account with a different email. This is a last resort but it works.
- Don't mention this proactively during the session — only address it if someone hits the wall

## Timing

| Time | Section | What's happening | You |
|------|---------|------------------|-----|
| 0:00 | Open | You talk, they listen | Screen share the comparison. Be direct, not hype-y. |
| 5:00 | Setup | They log into Claude, you explain the save rule | Paste claude.ai link. Watch for confused faces. |
| 10:00 | Build site | They build, you build alongside on your screen | Step by step. Pause a lot. Paste prompts in chat. |
| 35:00 | Build app | They build something harder, you float around | Check in. Encourage weird ideas. |
| 65:00 | Close | You talk, connect the dots | Keep it to ~15 min. Concrete. Point them forward. |

## Running Behind

Do a group deploy instead of individual GitHub setup. Saves about 5 min.

Skip the portfolio linking step ("Connect them") entirely. Students can do it after the session.

Shorten the Close section — skip the "What you actually learned" display and weave those points into your wrap instead.

## Running Ahead

Let them customize longer. The ones who are into it will surprise you.

Do a quick show-and-tell. Ask 2 or 3 students to share their screens on Zoom. This gets the quiet ones interested.

Spend more time on prompt iteration. Show how changing one sentence changes everything.

## The Comparison

Coding bootcamp: $15K, 3 months. Shipyard: $300, 90 minutes. Both produce working, deployed projects. The difference is we teach building with AI from the start, which is how more and more real software gets made now.

This is not a replacement for anything. Not college, not trade school, not a CS degree. It's a practical skill that layers on top of whatever they decide to do. Like knowing how to use a spreadsheet. It just makes everything else easier. Don't oversell it.

## Troubleshooting: What They Say

**"This is too hard."**
"That's normal. Let's look at it together. Tell me what part isn't working and we'll fix it right now."

**"AI did all the work."**
"You chose what to build. You decided how it should look. You told it what to fix. You deployed it. AI was the tool. You were the builder."

**"Why not just use Wix?"**
"You could. But then you'd learn Wix. Here, you're learning how to use AI to build anything. Not just websites. That skill transfers to apps, automations, tools, whatever you want to make next."

**"I don't want to build a portfolio site."**
"Then don't. The portfolio is the starting point, but build whatever you want. If you have an idea for something cooler, go for it. That's the whole point."

**"This is too easy."**
"Good. Add more features. Dark mode. Animations. Export to PDF. Push it until it breaks, then fix it."

## Troubleshooting: Zoom Stuff

**They can't see your screen.**
Ask if they're in gallery view. They need to switch to the shared screen view. On a phone or tablet, they have to tap the screen and select it. If nothing works, paste the current step into chat as plain text and keep going.

**Audio cutting out or they can't hear you.**
Have them leave and rejoin the call. If it keeps happening, switch from computer audio to phone dial-in. Post instructions in chat as backup either way.

**Someone falls way behind.**
Paste the current prompt or code snippet into the Zoom chat so they can copy it. If they're more than a few steps behind, tell them to jump to wherever you are now and finish the earlier parts after the session. Don't slow the group down for one person.

**A deploy fails and you can't debug it live.**
Share the backup screencast of a working deploy. Tell the student you'll troubleshoot with them in the last 5 min or after the session. Keep the group moving. This happens more often than you'd think.

**Student can't figure out TextEdit plain text mode.**
"On Mac, open TextEdit, then go to the Format menu at the top and click 'Make Plain Text.' Then paste and save as index.html." You will say this at least once per session.

**Student closes their tab and loses everything.**
"This is why we said save your work. If you saved to GitHub, it's still there. If not, you get to practice building it again. You'll be faster this time." Don't dwell on it. They'll remember next time.

## Parent FAQ

Parents ask these during or after sessions. Keep answers short and factual.

**"Is this just playing with ChatGPT?"**
"No. Students leave with live, deployed projects on the internet. Real portfolio pieces they can link on applications and resumes. They learn prompt engineering, deployment, and iterative development. These are practical skills that complement whatever path your student takes."

**"Is this a replacement for learning to code or going to college?"**
"Not at all. This complements any path. Students who go on to study CS will have a head start. Students who don't will still know how to use AI to build working software. It's a practical skill that makes everything else easier."

## Returning Students

| Session | Focus | What they build |
|---------|-------|----------------|
| 1 (this one) | Portfolio + micro-app | Website + first app |
| 2 | Level up | More complex app (multi-page, uses an API) |
| 3 | Automate your life | Personal tool (daily planner, habit tracker, budget thing) |
| 4 | Build for someone else | Tool for a club, a team, a family member |

The best sessions happen when a returning student pitches their own idea. Let them run with it. Your job shifts from guiding to unblocking.
