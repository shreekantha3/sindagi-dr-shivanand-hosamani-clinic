# TEST_REPORT — sindagi-dr-shivanand-hosamani-clinic

- `npm install`: PASS (87 packages)
- `npm run build`: PASS — `dist/index.html` 16.45 kB (gzip 4.03 kB), CSS 12.05 kB (gzip 3.27 kB), JS 1.20 kB (gzip 0.63 kB). Total `dist/` ≈ 40K.
- Base path: `/sindagi-dr-shivanand-hosamani-clinic/` ✓
- No-phone compliance: `grep -ci 'tel:\|wa.me'` on `index.html` = **0** — no `tel:`/`wa.me` links, no invented number. CTAs are Directions/Maps only; "Call for OPD timings" is plain text.
- SEO: title + meta description + OG tags ✓; JSON-LD `MedicalClinic` (no `telephone`) ✓
- A11y/perf: skip link ✓; async Google Fonts (`media="print" onload`) + `<noscript>` fallback ✓; `prefers-reduced-motion` in CSS ✓; dark slate text only ✓
- Contrast spot-check: body ink #0F172A on white; brand-700 #084F4F on white — dark, passes.

## Flags
- `data-missing=phone` — CSV phone empty; owner must supply number before any call/appointment CTA is added.
