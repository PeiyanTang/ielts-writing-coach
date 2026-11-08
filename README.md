# IELTS Writing Coach

An open-source Codex skill for rigorous IELTS Academic Writing assessment with multilingual explanations and English Band 8+ model answers.

It assesses either Task 1 or Task 2 independently, gives conservative criterion-level band estimates, diagnoses task and language problems, corrects sentences in context, supplies a realistic Band 8+ model response, and assigns a focused revision instead of automatically demanding a full rewrite.

## What it does

- Scores Task Achievement/Task Response, Coherence and Cohesion, Lexical Resource, and Grammatical Range and Accuracy.
- Accepts a prompt image with a `.txt` response or text pasted directly into chat.
- Handles Academic Task 1 and Task 2 as separate scripts.
- Checks task interpretation and idea development before language polishing.
- Distinguishes actual errors, awkward or imprecise wording, and optional refinements.
- Explains scores and corrections in the learner's preferred language while keeping corrections, IELTS criterion names, and model answers in English.
- Preserves a viable Task 2 stance while allowing stronger supporting arguments.
- Produces one original, exam-realistic Band 8+ model answer.
- Optionally maintains a private learner profile at a location chosen by the user.

## Install

Clone this repository into your Codex skills directory:

```powershell
git clone https://github.com/PeiyanTang/ielts-writing-coach.git "$env:USERPROFILE\.codex\skills\ielts-writing-coach"
```

On macOS or Linux:

```bash
git clone https://github.com/PeiyanTang/ielts-writing-coach.git ~/.codex/skills/ielts-writing-coach
```

Start a new Codex conversation if the skill list does not refresh immediately, then invoke `$ielts-writing-coach` and attach one IELTS Academic prompt and response.

## Language behavior

The coach uses a feedback language explicitly chosen by the learner. If no preference is stated, it follows the primary language of the learner's current request and asks only when the choice is genuinely unclear. It never guesses a mother tongue from a name, location, or background. Submitted writing, proposed corrections, IELTS criterion names, and Band 8+ model answers remain in English.

## Repository structure

```text
ielts-writing-coach/
|-- SKILL.md
|-- agents/openai.yaml
`-- references/
    |-- learner-profile.md
    |-- response-format.md
    |-- scoring.md
    |-- task-1.md
    `-- task-2.md
```

## Scoring basis

The skill is calibrated to the public IELTS Writing Band Descriptors and official sample scripts linked in `references/scoring.md`. Its scores are informed estimates, not official IELTS results.

## Privacy

The repository contains no learner history. Progress tracking is optional, stored only at a location selected by the user, and should not be committed to a public repository.

## Disclaimer

This independent project is not affiliated with, endorsed by, or sponsored by IELTS, the British Council, IDP Education, or Cambridge University Press & Assessment. IELTS is a registered trademark of its respective owners.

## License

MIT License. See [LICENSE](LICENSE).
