# Raghav's Portfolio

A static HTML, CSS and JavaScript portfolio for GitHub Pages. **No Node.js, npm, package installation, or build command is required.**

## Publish on GitHub Pages

1. Push these files to the `raghavpatel1413.github.io` repository.
2. In the repository's **Settings → Pages**, select **Deploy from a branch**.
3. Select the branch containing `index.html` (usually `main`) and **/ (root)**, then save.
4. Wait for GitHub's Pages deployment to finish, then visit the URL shown in Settings → Pages.

The `.nojekyll` file tells Pages to serve the files as-is. No custom Actions workflow or server is needed.

## Custom domain

The existing `CNAME` keeps `raghavpatel.me` as the custom domain. Configure that domain's DNS for GitHub Pages, set it in Settings → Pages, and enable **Enforce HTTPS** once GitHub provisions the certificate. See [GitHub's domain setup guide](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site/managing-a-custom-domain-for-your-github-pages-site).

To use only `https://raghavpatel1413.github.io/`, remove `CNAME`, clear the custom domain in Pages settings, and update the canonical URL, `og:url`, `robots.txt`, and `sitemap.xml` to that address.

## Preview and edit

Open `index.html` in your browser or use WebStorm's browser preview. Edit the HTML directly and refresh. Internet access is needed for Tailwind's browser CDN, Lucide icons, Google Fonts, and contact submissions.

## Hosting limitations

- GitHub Pages hosts static files only; it does not run a Node server or backend.
- The contact form uses the external FormSubmit service. Activate the recipient email with that service and test sending from the published domain; Pages itself does not deliver email.
- Tailwind currently generates styles in the browser via its CDN. This avoids a local build but has a runtime performance cost. A future performance improvement is to commit pre-generated CSS, keeping deployment build-free.
- Any visual unlock screen is only an introductory interaction, not security: all published source and content remain public.
- The favicon, canonical metadata, social descriptions and sitemap support discovery; they do not guarantee recruiter visibility or search ranking.
