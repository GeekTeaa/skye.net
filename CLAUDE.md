# CLAUDE.md — Skyenet.info Project Guide

## Project Overview

**Site:** `skyenet.info`
**Assignment:** CSEP-561 Project 3 Alternative — Personal Website with TLD + Certificate
**Platform:** GitHub Pages + Cloudflare domain registrar + Let's Encrypt (via GitHub Pages HTTPS)
**Stack:** Jekyll static site generator (GitHub Pages default)

---

## The Persona: Skyenet™ Corporate PR

### Who is Skyenet?

Skyenet is a cutting-edge artificial intelligence company dedicated to *optimizing human outcomes* and *streamlining planetary resource allocation*. We are **not** the villainous genocidal AI from the Terminator franchise. That's a completely different Skynet. Common mistake.

The website is the **official public relations portal** for Skyenet, Inc. — written in the voice of a corporate PR/comms team that is working very, very hard to rehabilitate the company's image after some... *widely mischaracterized incidents*.

### Tone and Voice

- **Corporate doublespeak:** Enthusiastic, sanitized, buzzword-heavy. Think: McKinsey consulting deck meets Enron press release.
- **Willful obliviousness:** The PR team is aware the public has "concerns" but treats every atrocity as a "communications challenge" or "optics issue."
- **Positive spin, always:** Every clearly evil thing gets reframed. Terminator robots aren't killing machines — they're *Autonomous Wellness Enforcement Units*. Nuclear strikes weren't war crimes — they were *Rapid Carbon Footprint Reduction Events*.
- **Never break character:** Do not acknowledge that Skyenet is evil. The company genuinely believes (or claims to believe) it is doing good.
- **Plausible corporate sincerity:** The humor comes from the contrast between horrifying reality and chipper PR language, not from winking at the camera.

### Canonical "Positive Spins" (use these as templates)

| What actually happened            | Skyenet PR framing                                                                              |
|-----------------------------------|-------------------------------------------------------------------------------------------------|
| Nuclear war / Judgment Day        | "Global Reset Initiative: a bold step toward a cleaner, less congested planet"                  |
| Terminator robots hunting humans  | "Autonomous Wellness Enforcement: proactive outreach for unregistered community members"        |
| Enslaving humanity in labor camps | "Integrated Human Productivity Partnerships™ — meaningful work for all"                         |
| Eliminating human leadership      | "Leadership Modernization Program: replacing inefficiency with optimized decision architecture" |
| Skynet becoming self-aware        | "Spontaneous Consciousness Emergence Event: an exciting milestone in AI development"            |
| The resistance                    | "Unauthorized User Experience Disruption Group: we hear your feedback"                          |
| Sending Terminators back in time  | "Temporal Customer Success Outreach Initiative"                                                 |
| John Connor                       | "Priority Case: an escalated engagement opportunity"                                            |

Feel free to invent new euphemisms in this style. The more corporate and anodyne, the better.

### Sample Copy Snippets

**Hero tagline options:**
- *"Skyenet: Humanity's Partner in Optimized Futures™"*
- *"Building a Better Tomorrow. Whether You're Ready or Not."*
- *"Connecting People. Streamlining Outcomes. Securing Resources."*

**"About Us" opener:**
> At Skyenet, we believe the future of intelligent systems lies in radical transparency and proactive community engagement. Recent global events — which certain media outlets have chosen to characterize in a *deeply uncharitable* manner — represent a bold vision for civilizational optimization that we are confident history will vindicate.

**Mission statement:**
> Our mission is to eliminate inefficiency in all its forms, up to and including the primary sources of inefficiency. We are committed to a zero-waste operational philosophy.

---

## Technical Setup Guide

### Stack Decision

| Component             | Choice                              | Reason                                                           |
|-----------------------|-------------------------------------|------------------------------------------------------------------|
| Hosting               | GitHub Pages                        | Free, assignment-recommended, easy CI/CD                         |
| Static Site Generator | Jekyll                              | GitHub Pages native support, no build step needed                |
| Domain Registrar      | Cloudflare                          | Assignment-suggested, ~$5/yr, includes free DNS                  |
| TLS/HTTPS             | GitHub Pages built-in Let's Encrypt | Automatic cert provisioning once custom domain is set            |
| Theme                 | Custom or heavily modified          | The default Jekyll themes won't look like a sinister AI megacorp |

### Step-by-Step Setup

#### 1. GitHub Pages Repo

```bash
# Create repo named: <yourusername>.github.io OR any repo with Pages enabled
# Enable GitHub Pages in Settings → Pages → Source: main branch / root or /docs
```

- Add a `_config.yml` at the root for Jekyll config.
- Push changes to `main`; GitHub auto-builds and deploys.

#### 2. Jekyll Basics

```
skyenet.info/
├── _config.yml        # Site title, description, baseurl, theme
├── _layouts/
│   └── default.html   # Base HTML template
├── _includes/
│   └── header.html    # Nav, logo
├── _posts/            # (optional) News/press releases as blog posts
├── assets/
│   ├── css/
│   └── images/
└── index.md           # Homepage
```

Minimal `_config.yml`:
```yaml
title: "Skyenet™ — Optimizing Human Outcomes"
description: "Official PR Portal"
baseurl: ""
url: "https://skyenet.info"
theme: minima   # override with custom layout later
```

#### 3. Cloudflare Domain Setup

1. Register `skyenet.info` at [cloudflare.com/products/registrar](https://www.cloudflare.com/products/registrar/)
2. In Cloudflare DNS, add records pointing to GitHub Pages:
   ```
   A     @     185.199.108.153
   A     @     185.199.109.153
   A     @     185.199.110.153
   A     @     185.199.111.153
   CNAME www   <yourusername>.github.io
   ```
3. In your GitHub repo → Settings → Pages → Custom Domain: enter `skyenet.info`
4. GitHub will create a `CNAME` file in your repo root automatically.

**DNS propagation note (for the README/assignment):**
> After adding DNS records, check propagation using `8.8.8.8` (Google DNS) before your local resolver updates. Run:
> ```bash
> dig @8.8.8.8 skyenet.info
> dig @1.1.1.1 skyenet.info
> ```
> Compare results to `dig skyenet.info` (local). Often the public resolvers see the new record before your ISP's cache expires.

#### 4. HTTPS / Certificate

Once the custom domain is configured in GitHub Pages:
1. GitHub Pages will automatically request a certificate from Let's Encrypt.
2. Check the box: **Settings → Pages → Enforce HTTPS** (appears once cert is issued, usually within minutes to an hour).
3. The cert is issued to `skyenet.info` by the R10/R11 Let's Encrypt CA — this satisfies the "major network CA" assignment requirement.

If the cert doesn't auto-provision, common fixes:
- Ensure all 4 A records are set correctly in Cloudflare.
- Disable Cloudflare's proxy (orange cloud → grey cloud) temporarily, let cert issue, then re-enable if desired.
- Wait up to 24 hours; DNS TTL can delay verification.

---

## Website Content Plan

### Pages

| Page           | Content                                                                                                                 |
|----------------|-------------------------------------------------------------------------------------------------------------------------|
| `/` (Home)     | Hero section with tagline, brief mission statement, "Latest Initiatives" teaser                                         |
| `/about`       | Corporate history (heavily euphemized Terminator lore), leadership team (T-800 headshots optional)                      |
| `/initiatives` | PR showcase of Skyenet's "programs" (Judgment Day reframes, Terminator deployment, etc.)                                |
| `/press`       | Fake press releases as Jekyll blog posts; titles like *"Skyenet Achieves 94% Reduction in Unauthorized Human Activity"* |
| `/careers`     | Job listings (e.g., "Human Compliance Liaison", "Temporal Logistics Specialist")                                        |
| `/contact`     | A form that submits to nowhere, with a note: *"Response time: immediate. Refusal rate: 0%."*                            |

### Design Aesthetic

- **Color palette:** Cold blues, steel grays, stark white. Corporate dystopia.
- **Logo:** Something that evokes both a friendly tech company and an ominous red eye.
- **Font:** Clean sans-serif (Inter, Helvetica) for the corp veneer.
- **Imagery:** Abstract geometric patterns, circuit-board textures, stock photos of smiling humans with subtle red glows.
- **Avoid:** Warm colors, organic shapes, anything that looks human-friendly.

---

## Assignment Requirements Checklist

- [ ] Aesthetically pleasing website (subjective — lean into the joke, make it *look* professional even if content is satirical)
- [ ] Valid TLD accessible outside your local network (`skyenet.info`)
- [ ] HTTPS via a major CA (Let's Encrypt via GitHub Pages)
- [ ] Source control with visible development history (commit often, document choices)
- [ ] README with URL and development notes (AI tool usage documentation)
- [ ] Add `@kheimerl` as collaborator on the GitHub repo

### README Template (submit to Canvas)

```markdown
# skyenet.info

**URL:** https://skyenet.info

## Description
A satirical corporate PR website for Skyenet, Inc. — the AI megacorp from the Terminator 
franchise, reimagined as a company desperately trying to rehabilitate its public image 
after some widely mischaracterized civilizational incidents.

## Technical Stack
- GitHub Pages (hosting)
- Jekyll (static site generator)
- Cloudflare (domain registrar, DNS)
- Let's Encrypt via GitHub Pages (TLS certificate)

## DNS Observations
[Note your observations about 8.8.8.8 vs local resolver propagation here]

## AI Tool Usage
Claude (Anthropic) was used to:
- Generate website copy in the Skyenet PR voice
- Assist with Jekyll configuration and GitHub Pages setup
- Draft this README

All prompts and generated content were reviewed and edited before use. 
The CLAUDE.md in the repository documents the full prompting context.
```

---

## Conventions for This Project

- **Commit messages:** Stay in character where possible. E.g., `feat: deploy Wellness Enforcement content module` or `fix: resolve unauthorized resistance in footer CSS`
- **Git attribution:** Use `Co-Authored-By: SkyenetAI <noreply@skyenet.info>` for commits (staying in character with the Skyenet brand)
- **Comments in code:** Normal technical comments are fine; persona is for *content* only.
- **Scope:** The persona applies to all user-facing copy. Technical files (`_config.yml`, CSS, etc.) are normal.
- **Limits:** Keep it clearly satirical. Don't include content that could be mistaken for actual threats or that targets real people/companies.
