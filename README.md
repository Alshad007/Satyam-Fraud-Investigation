# Satyam Fraud Investigation & Forensic Financial Analysis

An independent forensic reconstruction of India's largest corporate fraud (₹7,136 Cr, FY2005–FY2008), built entirely in Excel from public annual reports, the Raju confession letter, and CID findings.

---

## Why I built this

My first projects (an Air India vs. IndiGo diagnostic) were about reading numbers that were *true*  messy, but true. I wanted to try the opposite problem: can you tell, from the outside, when the numbers are lying?

Satyam is the natural case study for this in India; there's a public confession letter that tells you exactly what was faked, which means you can actually check your own analysis against the answer key. So the goal here wasn't just to summarize "what happened at Satyam" (that's been written a hundred times). It was to build a **repeatable red-flag framework**, the kind of scoring model a forensics analyst would actually use  and then prove it works by running it against Satyam and a clean peer (Infosys) side by side.

## What's in the workbook

`Satyam_Fraud_Investigation.xlsx` has five sheets, each one layer of the investigation:

| Sheet | What it does |
|---|---|
| **Raw Data** | Satyam's reported P&L and balance sheet (FY2005–08), Raju's confession-letter figures, and Infosys as a clean benchmark |
| **Analysis** | Ratio analysis (cash/assets, receivables/revenue, interest yield, revenue-per-employee)  Satyam vs. Infosys, side by side |
| **Red Flag Scoring** | A ten-indicator fraud risk model, weighted by diagnostic strength and scored against a clean industry peer, with each flag traced back to the exact audit or governance control that failed to catch it.|
| **Scenario Analysis** | Reported vs. restated financials, plus a year-by-year escalation timeline showing how a ₹20 Cr gap in FY2002 became ₹7,136 Cr by FY2008 |
| **Dashboard** | Executive summary headline metrics, two charts, key findings, and five recommendations |

## The fraud, in numbers

| Metric | Value |
|---|---|
| Total fraud quantum | ₹7,136 Cr (~US$1.6 Bn) |
| Fake cash on the books (FY2008) | ₹5,040 Cr = 94% of reported cash balance |
| Ghost employees | ~13,000, siphoning ~₹20 Cr/month |
| Years undetected | 7+ |
| Composite fraud risk score (my model) | Satyam 8.44/10 vs. Infosys 1.63/10 |
| PwC's fine at the time | US$200 (India Companies Act max) / US$33M (SEC + class action total) |

## How the red flag model works

This is the part I actually care about, because it's the part that generalizes beyond Satyam. Instead of just listing "things that were wrong," I scored ten indicators, each weighted by how diagnostic it is of financial statement fraud for *both* Satyam and Infosys. I mapped every one to the specific audit or governance control that should have caught it:

| # | Indicator | Weight | Satyam | Infosys | Control that failed |
|---|---|---|---|---|---|
| 1 | Cash balance inconsistency | 20% | 9.5 | 1.0 | Bank confirmation procedure bypassed |
| 2 | Revenue vs. receivables mismatch | 15% | 8.0 | 2.0 | No independent debtor confirmation |
| 3 | Interest income anomaly | 15% | 9.0 | 1.5 | Interest income never reconciled to bank statements |
| 4 | Headcount vs. revenue mismatch | 10% | 8.0 | 2.0 | HR payroll never reconciled to actual headcount |
| 5 | Promoter share pledge | 10% | 9.0 | 1.0 | SEBI disclosure norms didn't mandate pledge reporting |
| 6 | Related-party transactions | 10% | 8.0 | 2.0 | Maytas deal approved with no independent valuation |
| 7 | Auditor fee vs. complexity | 8% | 7.0 | 2.0 | No fee-to-complexity benchmarking |
| 8 | Board independence quality | 7% | 8.0 | 2.5 | Independent directors resigned only *after* the fraud broke |
| 9 | Accrued interest manipulation | 3% | 9.0 | 1.0 | Third-party bank confirmation circumvented |
| 10 | Operating margin compression | 2% | 5.0 | 2.0 | No alert on margin decline vs. revenue growth |

**Composite score: Satyam 8.44/10 (high risk) vs. Infosys 1.63/10 (normal)** — a 5x gap that would have flagged Satyam years before the confession, if anyone had been running this kind of check.

The single most damning number in the whole workbook: a 74.3% cash-to-total-assets ratio in FY2008. No operating IT services company holds three-quarters of its balance sheet in cash — that ratio alone should have triggered scrutiny before anyone even opened the confession letter.

## Key findings

1. **Cash fraud** — ₹5,040 Cr (94%) of reported FY2008 cash was non-existent
2. **Revenue inflation** — Q2 FY2009 revenue overstated by ₹588 Cr in a single quarter; real operating margin was 3%, not the reported 24%
3. **Ghost employees** — ~13,000 fictitious names on payroll, masking a declining revenue-per-employee trend
4. **Interest income anomaly** — reported interest implied a 4.8% yield on cash, well below prevailing FD rates — a number that shouldn't have survived a basic reconciliation
5. **Control failure** — PwC never independently confirmed cash balances directly with the banks
6. **Governance breakdown** — Raju had pledged 100% of his personal shareholding; the four independent directors resigned only after the fraud became public, not before

## What this project is (and isn't)

This is a portfolio exercise built from public sources annual reports, Raju's confession letter, and CID findings not a primary audit. I don't have access to underlying transaction level data, so the model works at the level a forensic *analyst* would work at before an engagement gets underway: spotting the ratios and patterns that justify digging deeper, not proving fraud beyond doubt. Treat the recommendations section as "what a fresher forensics analyst would flag for a senior to investigate," not a finished regulatory response.

## Recommendations (if I were advising SEBI post-mortem)

1. Mandatory independent bank confirmation for any cash balance above ₹100 Cr
2. Compulsory auditor rotation every 5 years + joint audit above ₹1,000 Cr revenue
3. Real-time SEBI reporting for promoter share pledges above 10% of holding
4. Whistleblower protection with financial incentives
5. Independent, physical HR headcount audits for companies above 10,000 employees

## Tools

Built entirely in Microsoft Excel, no external libraries. Formulas, conditional formatting, and native charts only, so the whole audit trail is inspectable in one file.

## Files

- `Satyam_Fraud_Investigation.xlsx` — the full model (5 sheets)
- `Satyam_Fraud_Investigation.pptx` — a 9-slide summary deck for anyone who wants the findings without opening Excel

---

**Md Alshad Ansari** 
[LinkedIn](http://www.linkedin.com/in/alshad) | alshad936@gmail.com
