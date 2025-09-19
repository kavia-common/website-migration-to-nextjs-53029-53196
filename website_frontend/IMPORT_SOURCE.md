# Importing Source Code for Migration

The source repository could not be cloned automatically due to authentication requirements.

Repository: https://github.com/amlkhwn/personal-site.git

Observed error:
- `fatal: could not read Username for 'https://github.com': No such device or address`

To complete the import, please provide one of the following:

1) Preferred: GitHub PAT (Personal Access Token) with `repo` read permission.
   - Recommended scope: `repo:read` (or `repo` if `repo:read` is not available).
   - Once available, set the environment variable:
     - GITHUB_TOKEN (or provide username/password for HTTPS).
   - Authenticated clone command (example):
     ```
     git clone --depth=1 https://<TOKEN>@github.com/amlkhwn/personal-site.git website-migration-to-nextjs-53029-53196/website_frontend/personal-site
     ```

2) If the repository is public, confirm public access or provide a direct archive link (e.g., GitHub release/source zip).
   - Example:
     ```
     curl -L -o /tmp/personal-site.zip https://github.com/amlkhwn/personal-site/archive/refs/heads/main.zip
     unzip -q /tmp/personal-site.zip -d website-migration-to-nextjs-53029-53196/website_frontend/
     mv website-migration-to-nextjs-53029-53196/website_frontend/personal-site-* website-migration-to-nextjs-53029-53196/website_frontend/personal-site
     ```

3) Provide a local archive (zip/tar) to attachments or give read-only access via a temporary link.

Once imported, the code will be available at:
- `website-migration-to-nextjs-53029-53196/website_frontend/personal-site/`

Next migration steps (planned):
- Audit the existing site’s build system (likely static HTML/CSS/JS) and content structure.
- Map pages to Next.js app router under `src/app`.
- Migrate static assets to `public/`.
- Wrap layout in `src/app/layout.tsx`.
- Implement redirects/routing as needed.
- Add Tailwind or maintain existing styles per project direction.

Note: No code was modified in the Next.js app; this document guides secure import.
