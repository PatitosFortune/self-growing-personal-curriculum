# Contributing

Thanks for looking. This is a deliberately small project, so contributions are welcome but selective.

## What fits

- Fixes to the validator, the progress script, the stylesheet or the docs.
- Clearer onboarding, better prompts in `prompts/`, and clearer rules in `AGENTS.md`.
- Accessibility and mobile-layout improvements.
- Reports from real first-run attempts: where you got stuck, what the assistant misunderstood.

## What does not fit

- A framework, build step, database, accounts, a server, analytics, trackers, CDNs or remote fonts. The point is plain static files.
- Features that need a specific AI provider. The rules must stay assistant-neutral.
- Personal or domain-specific course content. Show it in your own copy instead. The example course exists only to show the format.

## How

1. Open an issue first for anything larger than a typo, so we can agree on scope.
2. Branch from `main`. Do not push to `main` directly.
3. Keep the change small and run the validator; it must end with `RESULT: PASS`:

   ```bash
   python3 tools/validate_site.py
   ```

4. Open a pull request explaining what changed and why. If an AI assistant wrote part of it, say so and confirm you reviewed it.

Never include secrets, personal data or a private email address in a contribution. Report security problems privately, as described in [SECURITY.md](SECURITY.md).

By contributing you agree your work is released under the [MIT License](LICENSE).
