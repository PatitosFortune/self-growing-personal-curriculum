# Security policy

## What this project is

Self-Growing Personal Curriculum is a template: static HTML and CSS, one small browser script (`assets/js/progress.js`), Markdown instructions for AI coding assistants, and two Python standard-library tools (`tools/validate_site.py`, `tools/rebrand.py`). The site has no server, accounts, database, analytics or API, and it never calls an AI model.

That keeps the attack surface small, but it is not zero. In scope for a report:

- Cross-site scripting or other script injection through the progress import/export feature or any page.
- The validator or rebrand tool doing something other than reading and rewriting files in the repository (for example executing code, or writing outside the repository).
- The Pages workflow (`.github/workflows/pages.yml`) being usable to leak secrets, publish unintended files or run untrusted code with write access.
- Instructions in `AGENTS.md` or `prompts/` that would steer an AI assistant into exposing private data or running untrusted code.

Out of scope: vulnerabilities in GitHub Pages, GitHub Actions, your browser, or an AI assistant you chose to use; sites other people built from this template (report those to their owners).

## How to report

Please do not open a public issue for a vulnerability.

1. Preferred: use **Security → Report a vulnerability** on the repository page (GitHub private vulnerability reporting).
2. If that option is not available, contact the maintainers through the contact address on the [Patitos Fortune organization profile](https://github.com/PatitosFortune).

Include what you found, how to reproduce it, and the affected file or page. This is a small, volunteer-maintained project: expect an acknowledgement within about a week and a fix or a clear decision after that, but there is no service-level guarantee and there is no bug bounty.

## Supported versions

Only the current `main` branch is maintained. There are no versioned releases yet.

## If you build a site from this template

- **Everything in the repository root is published** when you use the included Pages workflow, including `curriculum/LEARNING_PROFILE.md`, `curriculum/CANDIDATES.md`, `curriculum/PROGRESS.json` and `AGENTS.md`. They are not linked from the site, but anyone who guesses the URL can read them. Keep sensitive details out of those files, or do not publish. See [docs/publishing.md](docs/publishing.md).
- **Git history is public too.** The author email on your commits is visible to everyone. Turn on **Keep my email addresses private** and **Block command line pushes that expose my email** in your GitHub email settings before your first commit, or set a `users.noreply.github.com` address in your Git configuration.
- **Do not put secrets in the repository**, including API keys and tokens for the assistant you use. The template does not need any.
- **Review what your AI assistant changes** before merging, especially workflow files, scripts and links.
