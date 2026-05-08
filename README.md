# 🔬 Learning Labs — Challenge Sign-up

**Part of the RoboTUM Academy · Summer Semester 2025**

A lightweight web app where RoboTUM Academy participants can browse this semester's challenges, read the full brief, and sign up for the one they want to tackle. All sign-ups are stored in real time to a Google Sheet.

---

## What is Learning Labs?

Learning Labs is a bi-monthly challenge program within the RoboTUM Academy. Beginners take on real, scoped tasks proposed by RoboTUM's advanced project teams — things that are genuinely useful to the projects but accessible without deep prior knowledge.

Each cycle runs for 4–5 weeks and ends with a showcase where participants present their output to the proposing team.

---

## How it works

1. Participant opens the link - https://diemnight.github.io/learning-labs/
2. Enters their name and email
3. Reads through the challenge briefs
4. Clicks **Select** on the one they want
5. Their name is saved instantly to the Google Sheet and the challenge brief is sent to their email

Each person can only sign up for one challenge. Challenges can have a slot limit — once full, they're marked as closed.

---

## Current challenges — Cycle 1

| Challenge | Project | Type | Slots |
|---|---|---|---|
| YOLOv8 vs Classical Detector | PlastiX | Research & Coding | 3 |
| Simulate a pick-and-place arm | PlastiX | Coding & Maths | 2 |
| CAD Design — Frail Alignment Mechanism | Hestia | CAD Design | 2 |
| CAD Design — Robotic Fingers | Creative Robotics | Competitive CAD | Unlimited |

---

## Tech stack

- Pure HTML, CSS, JavaScript — no framework, no build step
- Google Apps Script as the backend API (reads/writes to Google Sheets)
- Hosted on GitHub Pages (free, permanent link)

---

## Coordinator tools

The sign-up page includes a password-protected coordinator panel that lets you:

- Manually add a participant to any challenge
- Remove a participant
- Refresh data from the sheet

Access it by clicking **⚙ Coordinator tools** at the bottom of the page and entering the coordinator password.

---

## Updating challenges

To add, remove, or edit challenges, open `index.html` and find the `CHALLENGES` array near the top of the `<script>` section. Each challenge has these fields:

```js
{
  id: "Challenge name",         // used as the display title and sheet key
  project: "Project name",      // e.g. PlastiX, Hestia
  type: "Type label",           // e.g. Research & Coding, CAD Design
  competitive: false,           // true adds a "competitive" badge
  maxSlots: 3,                  // 0 = unlimited
  time: "4–6 hrs",              // estimated time commitment
  brief: "Description...",      // shown on the card
  deliverable: "Output..."      // shown below the brief
}
```

After editing, commit the change to `main` and GitHub Pages will update automatically within a minute.

---

## Coordinator access

Coordinators can also manage sign-ups directly in the Google Sheet — just open it and add or delete rows manually. The app syncs on every page load and when **↻ Refresh data** is clicked.

---

## Maintained by

Aaron Alexander — RoboTUM Academy, Learning & Community team  
RoboTUM · Technical University of Munich
