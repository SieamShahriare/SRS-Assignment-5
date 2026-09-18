# Ilm — Student Information System Redesign

An interactive, wireframe-style redesign of the IUT Student Information System (SIS), built as a usability case study for a Software Requirements Specification (SRS) course.

The original SIS repeats the same student profile block on every screen, buries functionality like results and admit cards behind mostly-empty pages, and loses navigation consistency between screens. This redesign keeps the same core data and purpose but restructures the information architecture, groups related features, and adds screens the original was missing entirely (a course routine, a CGPA trend view, and a fees overview).

**Live demo:** `https://<your-username>.github.io/<your-repo-name>/`
*(replace with your actual GitHub Pages URL once deployed)*

## What's inside

A single self-contained `index.html` — no build step, no dependencies to install, no backend — with eight connected, navigable screens:

| Screen | Purpose |
|---|---|
| Dashboard | At-a-glance overview: CGPA trend, attendance, today's classes, quick actions, pending dues and feedback status |
| My Courses | Registered courses for the current semester, with credit load, schedule and past-semester course history |
| Course Feedback | Filterable evaluation list (All / Pending / Evaluated) with an in-page star-rating submission flow |
| Results | Semester-wise SGPA/CGPA with an expandable, per-course grade breakdown for each completed semester |
| Admit Card & Exams | Admit card preview and eligibility checklist, plus the semester final exam schedule |
| Fees & Payments | View-only fee summary with an itemized pending-dues breakdown by fee head (no in-app payment) |
| My Profile | Personal, family/guardian, and contact information grouped into tabs |
| Settings | Password change with live strength meter, notification preferences, and a light/dark/system theme switch |

## Why it's designed this way

- **One persistent identity block** (top bar) instead of repeating the student's ID, name and photo on every page.
- **Grouped, labeled navigation** (Overview / Academics / Examinations / Finance / Account) instead of a flat, ungrouped menu.
- **Wireframe treatment** — grayscale palette, flat cards, plain typography, image placeholders instead of real photos — to keep the review focused on structure and flow rather than visual polish, which is appropriate at this stage of an SRS/usability review.
- **Fees are view-only.** The portal shows what's paid, what's pending, and an itemized breakdown by fee head, but does not process payments in-app — matching how many institutional systems separate information display from the actual payment channel (bank/bursar's office).
- **Genuinely interactive**, not a static image: sidebar navigation, tabs, an accordion, filters, a feedback modal, a password-strength meter, and a theme toggle all work, so the flow can actually be clicked through during review.

## Tech stack

Plain HTML, CSS and JavaScript — no frameworks, no build tooling. The only external resource is a Google Fonts stylesheet (Public Sans + IBM Plex Mono); everything else is inlined in the single file.

## Running locally

Clone the repo and open `index.html` directly in a browser:

```bash
git clone https://github.com/<your-username>/<your-repo-name>.git
cd <your-repo-name>
open index.html   # or just double-click the file
```

No server or install step is required.

## Deployment

This repo deploys automatically to GitHub Pages via the included workflow at `.github/workflows/`, using the official `actions/deploy-pages` action. Every push to `main` rebuilds and republishes the site; no manual deploy step is needed. In **Settings → Pages**, the source is set to **GitHub Actions**.

## Data disclaimer

All student, course, faculty, grade and fee figures shown are illustrative placeholder data used to demonstrate the redesigned flows. They do not represent real records.

## Project context

Built as a redesign exercise for a Software Requirements Specification (SRS) course assignment, focused on usability, information architecture and navigation rather than backend implementation.