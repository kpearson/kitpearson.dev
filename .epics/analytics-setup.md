# Google Analytics Setup (via Google Tag Manager)

## Tasks

### 1. Set up Google Tag Manager
- [x] Create GTM account (tagmanager.google.com)
  - Create new account for kitpearson.dev
  - Create web container
  - Get Container ID (format: GTM-XXXXXXX)

- [x] Add GTM to SvelteKit app
  - Add GTM script to `src/app.html` (head and body snippets)
  - Deploy and verify GTM is loading (use GTM Preview mode)

### 2. Set up Google Analytics 4
- [x] Create GA4 property
  - Sign in to Google Analytics (analytics.google.com)
  - Create new property for kitpearson.dev
  - Get Measurement ID (G-M6YQVWWXN7)

- [x] Configure GA4 tag in GTM
  - Add new Google Tag in GTM
  - Set Measurement ID
  - Add trigger: All Pages
  - Test in GTM Preview mode

- [x] Publish GTM container
  - Review changes
  - Publish container
  - Verify in GA4 Realtime view ✅

### 3. Configure events (optional)
- [ ] Track "Book a call" CTA clicks
- [ ] Track case study scroll depth
- [ ] Track external link clicks
- [ ] Custom conversion events

### 4. Verify tracking
- [ ] Check GA4 Realtime reports
- [ ] Verify pageviews are recording
- [ ] Test from multiple devices/browsers
- [ ] Verify events are firing correctly

### 5. Documentation
- [ ] Note GTM Container ID in secure location
- [ ] Note GA4 Measurement ID
- [ ] Document custom events and triggers

## Benefits of GTM Approach

- **No code deployments** for tag changes - manage in GTM UI
- **Multiple tags** - easily add Facebook Pixel, LinkedIn Insight, etc.
- **Advanced tracking** - scroll depth, video tracking, form submissions
- **Testing** - Preview mode to verify tags before publishing
- **Version control** - GTM maintains version history

## Notes

- Using GA4 (not Universal Analytics - deprecated July 2023)
- SvelteKit is client-side rendered, GTM works well with CSR after hydration
- GTM Preview mode helps debug tracking issues
- Consider privacy: May want cookie consent banner for EU traffic
