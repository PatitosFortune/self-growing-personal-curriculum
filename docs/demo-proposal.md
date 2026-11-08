# Demo proposal

Status: proposal for the maintainers. Nothing here is implemented yet.

## The problem with the current demo

The published site shows a two-lesson example course and an empty learning profile. A visitor can see what a finished lesson looks like, but not the thing the project actually claims to do: an assistant that grows a curriculum from a learner's interests. The honest gap is evidence of the workflow, not more features.

## Proposed demo: "one real session, shown in full"

Show a single, real first session end to end, with nothing staged beyond choosing a topic.

1. **Pick a small, neutral subject** that needs no private context, for example "how spaced repetition works" (already the example course's subject) or a second, unrelated one such as basic music theory, so visitors see that the format is not tied to software.
2. **Run the documented flow in a throwaway copy** of the template: the first-run prompt from `docs/starter-prompts.md`, then scouting, a choice, a lesson, the validator.
3. **Record what actually happened**, including the candidates the learner did not pick, any sources the assistant could not verify, and anything that needed human correction.
4. **Publish the record** as a short walkthrough page on the product page: the prompt, the resulting `LEARNING_PROFILE.md`, `CANDIDATES.md` with outcomes, the chosen lesson, and the validator result. Link to the throwaway repository.

What this proves: the workflow is followable by a stranger, candidates are staged before they become lessons, and the validator catches structure mistakes. What it does not prove: that lessons are accurate or that the assistant always behaves; the walkthrough should say so.

## Acceptance criteria

- Every claim on the walkthrough is backed by a file in the demo repository.
- The assistant, its version and the date are named.
- At least one thing that went wrong or needed correction is shown, if anything did.
- No private data; the demo repository contains no personal profile.
- Works without JavaScript apart from the Mark-as-read button, on a phone-width screen, with keyboard navigation.

## Out of scope for the demo

- Any hosted AI feature, account system or "try it live" box. The product has none, and adding one would change what it is.
- Invented testimonials, usage numbers or comparisons.

## Possible later evolution (not commitments)

- A second example course in a different field, to show the format is not software-specific.
- A progress page that is easier to use on mobile.
- Screenshots in the README, generated from the example course.
- An optional, clearly separate export format for flashcards. Only if a real learner asks for it.
