📘 Application Security Goal – DevNest Tech

*Course:** Application Security Foundations Level 1 (Semgrep)  
*Author:** Mansi Mahamuni  
*Scenario:** Security Integration in a Remote-first Startup  
*Company:** DevNest Tech  
*Team Size:** 25–30  
*Security Team:** Sole AppSec Engineer (me)

---

🎯 Goal 1: Integrate Security in CI/CD Pipelines Across All Projects

Objective:  
Ensure every software project at DevNest Tech integrates automated security scans in its CI/CD pipeline within 3 months.  
This includes:

- ✅ Static Application Security Testing (SAST)  
- 🔐 Secret Scanning  
- 📦 Open-source Dependency Analysis  

---

🧩 Step 1: Understand the Development Environment (1 Week)

Action:
- Initiated 1:1 coffee chats with team leads (Frontend, Backend, DevOps).
- Asked questions about:
  - CI/CD pipeline setup
  - Sprint durations
  - Deployment pain points
  - Tools currently in use (e.g., GitHub Actions, GitLab CI)
  - Manual vs automated processes

Reason: 
Understanding current workflows helps me design integrations that don’t disrupt velocity. For instance, if frontend teams push directly to S3 without a pipeline, I’ll need a custom approach.

---

🔧 Step 2: Select Tools & Customize for Dev Workflow (2 Weeks)

Tools Chosen:
- 🛡️ Semgrep — Customizable SAST  
- 🔑 Gitleaks — Secrets detection  
- 📚 OWASP Dependency-Check — Open-source vuln scanning (language dependent)

Action:
- Built reusable GitHub Actions YAML templates
- Tuned rule severity levels to avoid noise
- Configured builds to fail only on critical/blocker-level issues

Reason:  
Out-of-the-box tools are helpful but noisy. Custom rules + fail thresholds keep developers engaged instead of frustrated.

---

🤝 Step 3: Developer Enablement & Training (2 Weeks)

Action:
- Recorded a 30-min async session: _"Why CI Security Matters"_ and shared via Slack.
- Created `#secure-pipelines` Slack channel for:
  - Pipeline alerts
  - Feedback loop
  - Rule cheat sheets & config help
- Published internal Confluence docs with:
  - Sample alerts & fixes
  - How to handle false positives
  - Copy-paste CI config snippets

Reason:  
Security only scales when developers feel ownership. My goal isn’t to gatekeep, but to **empower**.

---

🧪 Step 4: Pilot, Feedback, & Rollout (2 Weeks)

Action:
- Ran pilots on 2 selected projects (frontend + backend)
- Paired with devs for “PR review parties” to integrate scans
- Monitored build issues, offered support quickly

Reason:  
Building trust and minimizing friction leads to higher adoption and better code hygiene across teams.

---

📊 Step 5: Dashboarding & Measurement (Ongoing)

Action:
Created a dashboard using **Grafana + Prometheus + webhook logs** to track:

- of projects with scans enabled
- of high/critical issues detected weekly
- False positive vs true positive ratio

Reason:  
You can't improve what you can't measure. This helps prioritize fixes and show value to leadership.

---

✅ Outcome

With this structured approach:
- DevNest now has full CI security integration across active projects
- Developers are informed and involved
- I have metrics to measure effectiveness and plan improvements

---


