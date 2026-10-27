# Performance and Functional Test Notes

## Test scope

The test checks the browser dashboard's initial rendering and core interactions using the full CSV included with this project. It loads all 27,468 data rows, renders the four charts and regional table, exercises year/region/country filters, and verifies that the filtered CSV export is triggered.

## Result

**Status: PASS**

- Dashboard-ready time in the local test environment: **1.187 seconds**.
- Dashboard JavaScript load metric: **906 ms**.
- Source CSV size: **1,885,113 bytes**.
- HTML size: **29,327 bytes**.
- Source records loaded: **27,468**.
- Verified UI behaviors: year filter updates KPI values; region filter narrows country choices; country selector updates the selected-record summary; filtered CSV download triggers.
- Console/runtime: no JavaScript runtime errors or browser console errors observed in this run.

### Checks passed

- [x] Browser loaded 27,468 CSV records through the test hook
- [x] All four SVG charts rendered
- [x] Regional summary table rendered with all seven regions
- [x] Year filter updates KPI values
- [x] Region filter narrows country options
- [x] Country selector updates selected-record summary
- [x] Filtered CSV download triggers with the expected filename
- [x] No JavaScript runtime errors
- [x] No browser console errors

## How to reproduce

1. Install Python 3.10+ and a compatible browser.
2. From the project root, install the test dependency: `python -m pip install -r requirements-test.txt`.
3. Install the Playwright Chromium browser: `python -m playwright install chromium`.
4. Run `python tests/test_dashboard.py`.
5. The script saves `performance-test-results.json` and refreshes `assets/dashboard-preview.png`.

## Important measurement limits

This test used Playwright's local HTML document and injected the repository CSV through a test-only hook. It did process the full dataset and verify the real dashboard JavaScript, but **the reported timings do not include an HTTP download of the CSV**. They are a local rendering/interaction baseline, not a Lighthouse score, hosted GitHub Pages benchmark or production SLA. Browser, machine, cache and network conditions change timing.

After enabling GitHub Pages, open the hosted site in Chrome DevTools or run Lighthouse against the hosted URL. Save the report/screenshot and append the real hosted results here. Do not report the local timing as an internet-access performance result.
