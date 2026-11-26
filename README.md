# Resume Work campaign — live dashboard

Public page for the CSP "Resume Work" campaign (PN 1795673193, in-app 1795673011, 169 CSPs, launched 26 Nov 2026).

- Page: `index.html` (static, no build). Loads numbers on open and every 60 s via JSONP from the tracking Apps Script `?action=campaign` (counts only — no CSP ids; digits in typed reasons masked).
- Backend: `campaignStats_()` / `campaignCompute_()` in the tracking sheet's Apps Script (`Code.gs`), reading tab `ResumeWork`. Cached 60 s.
- CleverTap numbers (PN sent/delivered/clicked, in-app shown) are typed into `CAMPAIGN.clevertap` in that script, then redeploy (Manage deployments → Edit → New version).
