# Capture Baseline Screenshots

Your first task is to capture baseline screenshots of all key pages before any audits or changes are made.

## Instructions

1. **Start Local Server**
   ```bash
   python3 -m http.server 8000 &
   ```

2. **Run Screenshot Script**
   ```bash
   node scripts/capture-screenshots.js --output=audit-results/baseline-screenshots
   ```

3. **Verify Capture**
   - Confirm all 42 screenshots were captured (7 pages × 3 breakpoints × 2 themes)
   - Check file sizes are reasonable (not blank screens)
   - Ensure screenshots saved to correct directory

4. **Stop Server**
   ```bash
   # Find and kill the Python server process
   pkill -f "python3 -m http.server 8000"
   ```

## Expected Output

You should see:
- 42 total screenshots
- Desktop (1920×1080): light + dark mode
- Tablet (768×1024): light + dark mode
- Mobile (375×667): light + dark mode

## Pages to Capture

1. index.html (Homepage)
2. about-me.html
3. ux-bites.html
4. casestudy/pages/bhava.html
5. casestudy/pages/pushowl.html
6. casestudy/pages/pushowl-bfcm.html
7. casestudy/pages/branch.html

## Success Criteria

✅ All 42 screenshots captured successfully
✅ Files saved to audit-results/baseline-screenshots/
✅ Server started and stopped cleanly
✅ Ready to proceed with parallel audits
