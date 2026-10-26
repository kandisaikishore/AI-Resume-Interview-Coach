# Development, AI-Integration, and QA Guide

This is an AI Studio career-preparation starter with a Node.js/npm workflow and Gemini-backed functionality where configured in source. Verify current implementation before describing resume analysis or interview features as complete.

## Setup and secrets

```bash
git clone https://github.com/kandisaikishore/AI-Resume-Interview-Coach.git
cd AI-Resume-Interview-Coach
```

Use the project's declared package scripts and runtime requirements. Configure the Gemini key in an untracked local environment file only if the source expects it. Never commit keys, real resumes, or private interview transcripts.

## Functional QA

For implemented flows, test:
- Missing/invalid credentials and provider-unavailable responses
- Empty, oversized, and malformed resume or prompt input
- Provider timeout, rate limit, and malformed model output
- Repeated submission, cancellation, and stale async responses
- Clear distinction between generated suggestions and verified facts
- Loading, success, and recoverable error states

Mock the AI provider in automated tests so they run without real credentials or quota. Validate structured model output before displaying or persisting it.

## Privacy and responsible output

Resume and interview content may contain personal information. Minimize logging and retention. Do not fabricate resume facts, citations, or guaranteed hiring outcomes. Explain that generated suggestions require human review.

## Pull-request checklist

- [ ] Run the declared lint/test/build commands.
- [ ] Add regression tests for provider failure and invalid input.
- [ ] Verify secrets and user content are not exposed in logs.
- [ ] State which AI behaviors were mocked.
- [ ] Keep implementation and roadmap claims separate.
