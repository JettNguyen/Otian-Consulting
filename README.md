# Otian AI Consulting

The consulting site for Otian AI LLC: Jack and Jett helping small businesses use AI, with Archie
(otianai.com) as the proof. One static page, no build step, served by GitHub Pages.

## Before it goes live

- Jett and Jack confirm three offers the page makes: visits around Dallas-Fort Worth, setting up an
  AI the owner already uses, and checking what they pay for software.
- Price the monthly "someone to call" plan. The page shows `[Price to set]` in two places (the
  services card and the price card), and otianai.com's FACTS.md gets a row for the figure first.
- On otianai.com, merge `consulting-site-links` the day this site answers. It points every Services
  and Work With Us link here and turns `services/`, `consulting/` and `guided-setup/` into redirects.
  The same day, because the Terms' guided-sessions link changed: set the Terms' `data-terms-version`
  and "Last updated" to that day, run `python3 scripts/archive-terms.py`, and bump `TERMS_VERSION`
  in Archie's next release.

## Publishing

1. Create a GitHub repository for this folder and push it.
2. In the repository's Settings, Pages: deploy from the `main` branch, root folder.
3. Where otianai.com's DNS is managed, add a CNAME record: `consulting` pointing to
   `jettnguyen.github.io`.
4. Back in Pages, set the custom domain to `consulting.otianai.com` (the `CNAME` file already says
   so) and turn on Enforce HTTPS once the certificate is issued.

A different address later means changing `CNAME`, the canonical link in `index.html`,
`robots.txt` and `sitemap.xml`, and the links on otianai.com.
