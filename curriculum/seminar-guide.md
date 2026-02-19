# Shipyard: Read-Aloud Script (Zoom Workshop)

> **Everything in "quotes" is exactly what Caleb says out loud.**
> **Everything in [brackets] is a stage direction. What to do, not say.**
> **No improvisation needed. Just read the quotes and follow the brackets.**

---

## BEFORE STUDENTS JOIN THE CALL

[Checklist. Do these 5 min before the scheduled start. Pre-session email should have gone out 24 hrs ago (see `curriculum/pre-session-email.md`).]

- [ ] Your screen shared in Zoom, showing claude.ai
- [ ] Demo portfolio site open in a browser tab (your example)
- [ ] Demo micro-app open in another tab (your example)
- [ ] Student handout link ready to paste into Zoom chat
- [ ] Zoom chat open so you can paste links and prompts as you go

---

## 0:00 - OPEN (5 min)

[Unmute. Camera on. No slides. Just talk.]

"Hey everyone, welcome. I'm Caleb. Let's get right into it."

"So right now, a coding bootcamp costs about fifteen thousand dollars. Three months, full time. You learn HTML, CSS, JavaScript, Git, deployment. Real skills, real price tag."

"Here's what changed. The AI we're using today, Claude, can build a working app in minutes. The same app a bootcamp student would spend weeks writing by hand. Line by line. The skill that actually matters now isn't typing code. It's knowing how to tell AI exactly what to build."

"That's useful no matter what you end up doing. And honestly, you're in a better position to learn it than most adults, because you don't have ten years of doing it the old way that you need to forget first."

"So here's what's happening in the next 90 minutes. You're building two things. A portfolio website and a working app. Both live on the internet. Both yours. By the time this call ends, you'll have a URL you can text to someone and say, I made this."

"No lectures. We build. Let's go."

---

## 5:00 - SETUP + SAVE WARNING (5 min)

[Share your screen showing claude.ai. Paste the link into Zoom chat.]

"Everyone go to claude.ai and log in. You should have an account from the setup email. If you don't, make one now — link's in the chat."

[Give them 60 seconds. Watch the Zoom grid for confused faces. Ask "Does everyone have Claude open?" before moving on.]

"Okay. Before we build anything, one rule."

[Pause for a beat.]

"Your AI chat does not save automatically. If you close the tab, if your laptop dies, if you accidentally refresh, your work is gone. Just gone. So the rule is simple: every time Claude gives you something good, you save it. Copy it. Paste it somewhere — a notes app, a Google Doc, anywhere. Do not trust the browser tab."

"We good? Good. Let's build."

---

## 10:00 - BUILD YOUR WEBSITE (25 min)

### Prompt it (4 min)

[Show this prompt on your shared screen. Paste it into Zoom chat so students can copy it easily.]

"Here's what you're going to type into Claude. I'm putting it in the chat right now so you can copy and paste. Fill in the blanks with your actual info."

[Display on screen and paste into chat:]

```
I'm a high school student and I want to create a personal portfolio website.
Here's some info about me:

- Name: [YOUR NAME]
- Grade: [YOUR GRADE]
- Interests: [2-3 THINGS YOU CARE ABOUT]
- One thing I'm proud of: [ANYTHING - a project, a sport, a hobby]

Please create a complete, single-page HTML website for me with:
- A clean, modern design (dark mode optional)
- A hero section with my name and a one-line tagline
- An "About Me" section
- A "Projects" section (leave placeholder cards for now)
- A "Contact" section with a mailto link
- Smooth scroll navigation
- Mobile responsive
- Use only HTML and CSS (no external dependencies)

Make it look professional but have personality.
```

"Fill in your details. Hit enter. Claude's going to write you an entire website."

[Watch the Zoom grid while they type. Say "If you're stuck on interests, just put what you actually spend time on. Video games, cooking, robotics. Whatever's true." After about 90 seconds:]

"While it generates. What you just did has a name in the industry. Prompt engineering. You gave an AI context about who you are and constraints for what you want. That's a job title at real companies right now. People get paid to do exactly that."

### Customize it (5 min)

[Once most students seem to have output, based on the Zoom grid:]

"Alright. You should all have a website. But it probably doesn't look exactly right yet. So let's fix that. Type any of these follow-ups into the same conversation."

[Display on screen and paste into chat:]

```
Change the color scheme to [blue and gold / earth tones / neon / whatever you want]
```
```
Add an animated gradient background to the hero section
```
```
Make it more minimal / more creative / more fun
```
```
Add a section for my extracurriculars and activities
```

"Go for it. Make it yours. You've got five minutes. Those prompts are starting points. You'll probably come up with better ones. Most people end up building something cooler than the demo I showed you at the start."

[If someone seems to have a good one, ask them to share their screen briefly: "Hey [name], want to share your screen for a sec? That looks really clean." This motivates others.]

[At the 4-minute mark:]

"One more minute on customization, then we're putting these on the internet."

### Deploy it (5 min)

"Time to make this live. Go to github.com. Link's in the chat."

[Paste github.com into Zoom chat. Walk through every step on your shared screen so students can follow along visually.]

"Everyone should have a GitHub account from the setup email. If you don't have one yet, make one now — but it'll eat into your build time."

[Give them 30 seconds for this.]

"On GitHub, click the plus icon in the top right corner. Click 'New repository.' For the name, type your GitHub username, then a dot, then github.io. Like this."

[Type it on screen: yourusername.github.io]

"Has to match your username exactly. Set it to Public. Check the box that says 'Add a README file.' Click 'Create repository.'"

[Do this on your screen. Pause. Say "Drop a message in chat when you've got the repo created." The README checkbox is important — it initializes the repo so the 'Add file' button appears immediately.]

"Now go back to your Claude tab. Select all the code Claude gave you. Copy it. Then go back to GitHub. Click 'Add file' and then 'Create new file.' In the filename field at the top, type index.html. Paste your code into the big editor box. Scroll down and click 'Commit changes.'"

[Do this on your screen so they can watch. Everything stays in the browser — no TextEdit, no file downloads.]

[Pause. Say "How's everyone doing? Thumbs up in Zoom reactions when you've committed the file."]

"Now click 'Settings' in the top menu of your repo. Left sidebar, click 'Pages.' Under 'Branch,' change the dropdown from 'None' to 'main.' Click Save."

[Do this on your screen.]

"Give it thirty to sixty seconds. Then open a new tab and go to your username dot github dot io."

[Pause. Watch for reactions.]

"If your site is showing up, that's a live website. You built that. If it's not loading yet, give it another minute. GitHub Pages can be slow to publish."

"If you're stuck on any step, drop your question in the chat and I'll walk you through it."

### Quick reminder (30 sec)

"And save your code. Your GitHub repo has a copy, but also copy the code from Claude and paste it somewhere safe as a backup — a notes app, a Google Doc, whatever. Don't rely on only one place."

---

## 35:00 - BUILD YOUR APP (30 min)

### Pick your project (3 min)

"Now we build something more interesting. A working app. Something you can actually use. Pick one of these, or come up with your own."

[Display on screen and paste into chat:]

```
STUDY BUDDY      Paste your notes, get flashcards and quiz questions
DEBATE PREP      Enter a topic, get arguments for both sides
WORKOUT PLANNER  Enter your goals + equipment, get a custom plan
ESSAY HELPER     Answer 5 questions, get 3 unique essay angles
YOUR OWN IDEA    Go for it
```

"If nothing jumps out, go with Study Buddy. Everyone needs flashcards. But if you have your own idea, those usually turn out best. The list is just there to get you started."

[Give them 30 seconds to decide.]

"Got one? Good."

### Build it (12 min)

"Open a new conversation in Claude. Not the same one. New conversation. Type this in, fill in your app name and what it does."

[Display on screen and paste into chat:]

```
I want to build a simple web app called [APP NAME].

What it does: [DESCRIPTION]

Requirements:
- Single HTML file with embedded CSS and JavaScript
- Clean, modern UI
- Works entirely in the browser (no backend needed)
- Use localStorage to save data between sessions
- Mobile-friendly
- Add a small footer that says "Built with AI by [YOUR NAME]"

Build the complete app.
```

"Hit enter. This one takes a bit longer to generate."

[While students wait for Claude to generate, drop this in the chat:]

"While we wait — someone built a script that automatically opens TikTok and Instagram Reels whenever Claude is thinking, so they wouldn't get bored staring at the screen. That's a real project someone shipped. You could literally build that after this session."

[Link in chat: https://www.instagram.com/reels/DR5E5f4gbYl/ — gets a laugh and subtly shows them what's possible.]

[Watch the Zoom grid. This is the core of the session. After about 2 minutes:]

"If Claude gives you something and it doesn't work, that's normal. Actually, that's useful. Copy the error message, paste it back into Claude, and say 'I'm getting this error, fix it.' That back and forth is called iterative development. It's not a sign something went wrong. It is the process."

[If someone finishes early:]

"Done already? Add features. Ask Claude for a dark mode toggle. Animations. Data export. Keep pushing it until something breaks, then fix it. That's where you actually learn."

[At the 10-minute mark:]

"Two more minutes of building, then we deploy."

### Deploy it (4 min)

"Same process as your portfolio. GitHub. New repository. This time name it whatever your app is called. study-buddy, workout-planner, whatever. Add file, create new file, name it index.html, paste your code, commit. Settings, Pages, branch to main, save."

[Walk through this on your shared screen.]

"Your app will be live at your-username dot github dot io slash your-app-name. So if your username is janedoe and your app is study-buddy, the URL is janedoe.github.io/study-buddy."

[Pause for them to deploy. Say "Drop your live URL in the chat when it's working."]

### Connect them (3 min, optional)

"If you've got time, let's connect your app to your portfolio. If you're still finishing your deploy, skip this and do it after the session. Go back to your portfolio conversation in Claude. Or start a new one and paste your portfolio code in. Then type this."

[Display on screen and paste into chat:]

```
Here's my portfolio website code:
[PASTE YOUR PORTFOLIO CODE]

Add a new project card for [APP NAME].
Link: https://[username].github.io/[app-name]
Description: [ONE SENTENCE ABOUT WHAT IT DOES]

Keep the same design. Give me the updated code.
```

"Copy the updated code. Go to your portfolio repo on GitHub, click on index.html, then click the pencil icon to edit. Select all, paste the new code over it, and commit. It'll replace the old version."

"Now your portfolio links to your app. Your app says 'Built with AI by your name.' Everything connects."

---

## 65:00 - CLOSE (15 min)

### What you actually learned (4 min)

"Okay. Let's talk about what just happened. You built a website and an app, yes. But here's what you actually practiced."

[Display on screen:]

```
WHAT YOU DID                        REAL-WORLD NAME
─────────────                       ──────────────
Told AI about yourself              Prompt engineering
Told it what format to use          Writing specifications
Asked it to change things           Iterative development
Fixed errors by pasting them back   Debugging
Put it on the internet              Deployment
Connected your projects together    Portfolio architecture
```

"Those aren't buzzwords. Those are job descriptions. And the proof isn't a grade or a certificate. It's a URL. Anyone can click it. Anyone can see what you built."

### The real skill (3 min)

"The specific tools we used today. Claude, GitHub, HTML. Those might be different in six months. New AI models come out constantly. New platforms replace old ones. That's fine."

"Because the skill you practiced isn't 'how to use Claude.' The skill is this: pick up a new tool, figure it out, build something real, ship it, move on to the next one."

"That works everywhere. College, a job, a side project, a startup. The tools change. That process doesn't."

### Wrap + what's next (3 min)

"The handout with all the prompts is in the chat so you can keep building after this. Here's your homework."

[Display on screen and paste into chat:]

```
TONIGHT      Text your portfolio link to one person
THIS WEEK    Build one more app and add it to your site
THIS MONTH   Find a real problem you have and build a tool that solves it
ALWAYS       Every new project goes on your portfolio
```

"Your portfolio is alive now. Every project you add makes it stronger. An admissions officer clicking a link to a working app they can actually use is worth more than a line on a resume."

"If you get stuck, reach out through the contact form on our site. Go build stuff. Thanks for showing up."

[Paste the student handout link and website URL into Zoom chat one more time before ending the call.]

---

## CHEAT SHEET - IF THINGS GO WRONG

[Keep this open on your phone or a second monitor during the session.]

| Problem | What to say |
|---------|------------|
| Student's code doesn't work | "Copy the error, paste it into Claude, tell it to fix it. That's literally the skill." |
| Student doesn't know what to build | "Go with Study Buddy. Everyone needs flashcards." |
| GitHub is confusing someone | Share your screen and walk through it step by step. If multiple people are stuck, do a group walkthrough. |
| Student says "AI did all the work" | "You decided what to build, how it should look, what to change, and then you shipped it. AI was the tool. You were the one making decisions." |
| Student says "This is too easy" | "Good. Add features. Dark mode. Animations. PDF export. Push it until it breaks and then fix it." |
| Student closes their tab and loses everything | "This is why we talked about saving. If you committed to GitHub, it's still there. If not, rebuild it. You'll be faster this time." |
| Student hits Claude free tier limit | "Go to Settings, start the free Pro trial. Takes 30 seconds. If that doesn't work, open an incognito window and make a new account." |
| You're running 5+ min behind | Skip "Connect them" and "What you actually learned." Weave key points into your wrap. Deploy apps as a group. |
| You're running 5+ min ahead | Let students customize more. Have 2-3 students share their screen and show what they built. |
| Parent asks "Is this just ChatGPT?" | "Students leave with live, deployed projects on the internet. They learn prompt engineering, debugging, and deployment. The output is a portfolio, not a conversation." |
| Zoom audio/video issues | "If you can't hear me, try leaving and rejoining. I'll put the current step in the chat so you don't miss anything." |

---

## REPEATABLE VARIATIONS

[For students who come back for another session:]

| Session | Focus | What they build |
|---------|-------|----------------|
| 1 (this one) | Portfolio + micro-app | Website + first app |
| 2 | Level up | More complex app (multi-page, uses an API) |
| 3 | Automate your life | Personal tool (daily planner, habit tracker, budget tool) |
| 4 | Build for someone else | Tool for a club, a team, a family member, or a small business |
