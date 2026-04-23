# Nyree Hinton — Job Search Targets & Bot Filter Configuration

This file defines exactly how to configure the JobHuntr app for Nyree's campus job and staff role search.
Copy these settings into the app's setup fields.

---

## Bot Configuration Settings

### Location
```
City:    Los Angeles, CA
Country: United States
Radius:  20 miles
```

### AI Model (Ollama — Free Plan)
```
Recommended: gemma3:4b  (4GB RAM, fastest)
Alternative:  llama3     (if gemma3 unavailable)
Ollama URL:   http://localhost:11434
```
> Upgrade to Premium ($10/mo) for GPT-4o + Claude 4 Sonnet, ATS resume auto-generation, and 35–45 apps/day.

### Daily Application Limit
```
Free plan:    20 applications/day
Premium plan: 35–45 applications/day
```

### Application Mode
```
Start with: Queue / Review mode (first 10 applications)
Then switch: Auto-apply (free run after 10 reviewed)
```

---

## Job Title Search Filters (Enter in app search bar)

Use these titles one at a time or in rotation across sessions:

```
"Research Data Analyst"
"Graduate Research Assistant"
"Teaching Assistant"
"Instructional Student Assistant"
"Data Analyst"
"Business Data Analyst"
"Program Coordinator"
"Administrative Analyst"
"Information Systems Assistant"
"Resident Advisor"
"Research Assistant"
"Product Analyst"
"Operations Analyst"
"Graduate Assistant"
```

---

## Target Employers (Priority Order)

### Tier 1 — Highest Priority (Housing + Income)
| School | Portal / Career Page |
|--------|---------------------|
| UCLA | jobs.universityofcalifornia.edu |
| USC (University of Southern California) | usccareers.usc.edu |
| Cal State LA | calstatela.edu/hrm/employment-opportunities |
| Loyola Marymount University | lmu.edu (Handshake) |

### Tier 2 — Strong Fit (Data/Research Roles)
| School | Portal |
|--------|--------|
| Claremont Graduate University | cgu.edu |
| Chapman University | chapman.edu |
| Pepperdine University | pepperdine.edu (Workday) |
| California Lutheran University | callutheran.edu |
| Cal Poly Pomona | cpp.edu |
| Cal State Northridge (CSUN) | csun.edu |
| Cal State Long Beach (CSULB) | csulb.edu |

### Tier 3 — Fallback / Accessible Entry
| School | Portal |
|--------|--------|
| Mount Saint Mary's University LA | msmu.edu |
| Glendale University College of Law | glendalelaw.edu |
| Caltech (Pasadena) | hr.caltech.edu |
| Antioch University LA | antioch.edu |
| UCLA Extension | uclaextension.edu |
| USC Price School | priceschool.usc.edu |
| UCLA School of Law | law.ucla.edu |
| USC Gould School of Law | gould.usc.edu |
| Occidental College | oxy.edu |

---

## Company Blacklist (Former Employers — Add to Bot Blacklist)

```
Capital Group
Third Bridge Group
Third Bridge
Bloomberg LP
Bloomberg L.P.
Bloomberg
Reorg Research
Reorg
```

---

## Smart Filters — Jobs to SKIP

Configure these as exclusion keywords in the bot's smart filter:
```
"Unpaid"
"Volunteer"
"Commission only"
"Requires PhD" (unless explicitly research-targeted)
"Requires current enrollment" (for staff roles — not grad assistant)
"Nursing"
"Medical"
"Healthcare clinical"
```

---

## Resume Upload Instructions

1. Upload your latest resume PDF from **nyreehinton.com** or the attached `Nyree-Hinton.pdf`
2. Key sections JobHuntr will use to generate ATS resumes:
   - **Capital Group** → emphasize for data analyst, research, BI roles
   - **Reorg Research** → emphasize for finance, M&A, bankruptcy, activism roles
   - **Bloomberg LP** → emphasize for equity research, data quality, financial data roles
   - **AWS CCP Cert** → emphasize for IT, systems, cloud roles
   - **ESG Cert** → emphasize for sustainability, governance, policy roles
3. Let the bot auto-generate a tailored 1-page ATS resume per application (Premium feature)
   OR manually upload one version for all applications (Free plan)

---

## Outreach Message Template (Post-Application DM)

Use this in the bot's **Outreach to Company** / DM feature after applying:

```
Hi [Name],

I recently submitted an application for the [Role Title] position at [School/Department].

My background in ETF data product management at Capital Group and financial research 
at Bloomberg and Reorg Research gives me a strong foundation in data analytics, 
SQL/Python pipeline work, and cross-functional stakeholder management — skills I'm 
excited to bring to [School]'s team.

I'd welcome the chance to connect briefly if you have a moment.

Best,
Nyree Hinton
nyreehinton.com | 732.979.6264
```

---

## Application Tracker Log (Manual Backup)

Use the bot's built-in **Job Tracker** tab to track status. Also maintain this log:

| Date | School | Role | Status | Notes |
|------|--------|------|--------|-------|
| | | | Applied | |
| | | | Interviewing | |
| | | | Offer | |
| | | | Rejected | |

---

## Weekly Goals

| Week | Target Applications | Focus Schools | Priority Role Type |
|------|--------------------|--------------|-----------------|
| Week 1 | 20 | UCLA, USC, Cal State LA | Research Data Analyst, Grad Assistant |
| Week 2 | 20 | LMU, Chapman, CGU | Teaching Assistant, Program Coordinator |
| Week 3 | 20 | Pepperdine, Cal Lutheran, CSUN | RA / Housing-linked, Admin Analyst |
| Week 4 | 20 | CSULB, Cal Poly, Caltech | Data/IT Analyst, Research Assistant |

**Total Month 1 target: 80 applications across 20 schools**

---

## Notes & Tips

- **RA Roles:** UCLA RA applications open November — enroll first, then apply. Free apartment + stipend.
- **USC TA/RA (50% appointment):** $40K/yr stipend + tuition remission up to 12 units/semester. Requires PhD enrollment.
- **Staff roles (no enrollment required):** UCLA Research Data Analyst ($33–$69/hr), USC Business Data Analyst ($74K–$85K) — apply NOW via job portals above.
- **Free plan limit:** 20 apps/day. Run the bot daily for maximum reach.
- **Premium ($10/mo):** Unlocks ATS resume auto-generation per application + 35–45 apps/day — strongly recommended once you confirm bot is working correctly.
