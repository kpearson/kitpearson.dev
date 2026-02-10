# Consulting Site

Single-page consulting site. Two offerings:

1. **AI Infrastructure Cost Optimization** � Fixed-fee engagements to audit and
   reduce LLM/AI compute costs (proven 95%+ reduction in production).
2. **Fractional VP of Engineering / AI Transformation** � Embedded leadership
   for teams adopting AI-native workflows.

## Stack

- **Framework:** SvelteKit w/ `adapter-static`
- **Styling:** Tailwind CSS
- **Hosting:** AWS S3 + CloudFront
- **DNS:** Route 53
- **SSL:** ACM (CloudFront handles TLS termination)
- **Deploy:** GitHub Actions ? `aws s3 sync` + CloudFront invalidation

## Setup

```bash
npx sv create consulting-site
cd consulting-site
npx svelte-add tailwindcss
npm install -D @sveltejs/adapter-static
npm install
```

In `svelte.config.js`:

```js
import adapter from "@sveltejs/adapter-static";

export default {
  kit: {
    adapter: adapter({
      pages: "build",
      assets: "build",
      fallback: null,
      precompress: false,
      strict: true,
    }),
  },
};
```

## AWS Infrastructure

```bash
# S3 bucket (static hosting)
aws s3 mb s3://YOUR_DOMAIN

# CloudFront distribution
# - Origin: S3 bucket
# - Default root object: index.html
# - ACM cert for HTTPS

# Route 53
# - A record ? CloudFront alias

# Deploy
npm run build
aws s3 sync build/ s3://YOUR_DOMAIN --delete
aws cloudfront create-invalidation --distribution-id DIST_ID --paths "/*"
```

## Project Structure

```
src/
  routes/
    +page.svelte
    +layout.svelte
  lib/
    components/
      Hero.svelte
      Offerings.svelte
      CaseStudy.svelte
      Background.svelte
      BookCall.svelte
  app.html
```

## Tasks

See [.epics/tasks.md](.epics/tasks.md) for project task list and planning.
