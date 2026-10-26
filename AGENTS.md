# AGENTS.md

Guidance for AI coding agents working in this repository.

## What this repository is

A prose framework, not software. It argues that **specification literacy** — describing a problem precisely enough that any interpreter, human or machine, produces the same result — is a foundational literacy, and shows how to teach it from kindergarten through adult professional life. There is no build, no test suite, and no code to run. Every change is an edit to Markdown.

The framework applies to its own documents: write so that a careful reader can't take a sentence two ways.

## Layout

| Path | Role |
|------|------|
| `index.md` | The main framework document. Numbered sections (§1–§14) and footnotes. Other files cite it by section number. |
| `docs/continuing-ed-course-outline.md` | Adult anchor course (Band 5), a community-college continuing-education class. |
| `docs/pilot-plan.md` | Pilot and evaluation plan for that course. |
| `docs/explicit-instruction.md` | How the framework maps onto Explicit Instruction (Rosenshine; Archer & Hughes; Engelmann). |
| `docs/specs/`, `docs/plans/` | Dated design documents and their implementation plans. These are **historical records**: don't revise them to match later changes. |
| `README.md` | Overview and file table. Add a row when you add a document. |

## Writing conventions

- **No date or version stamps in documents.** Don't add headers like "Draft v3 · April 2026". Git history is the record of when things changed; dates in the text drift out of date. (Dated filenames under `docs/specs/` and `docs/plans/` are the exception.)
- **Cross-references cite `index.md` by section.** From `docs/`, link the file and give the section: ``[`../index.md`](../index.md) §10.3``. Within `index.md`, use the bare `§` form (`§12.1`). If you renumber sections, update every cross-reference in every file.
- **Use the framework's own terms, and use them consistently.** These have fixed meanings; don't paraphrase them into near-synonyms:
  - *underspecification* (§2)
  - *the Verification Principle*: specify, evaluate, explain, identify limits (§4)
  - *the Assumption Audit*, with its four questions: Types, Boundaries, Defaults, Context (`docs/continuing-ed-course-outline.md`, Session 2)
  - *the expert's curse* (§10.5)
  - the five developmental *bands* (§10)
- **Footnotes for sources.** Use Markdown footnotes (`[^1]` in `index.md`; named footnotes such as `[^archer]` are fine in `docs/`), collected under a `## Notes` heading at the end of the file. Give the author, title, venue, year, and a URL where there is one.
- **Keep quotations short and few.** Paraphrase sources. Quote only a short phrase when the exact wording matters.
- Separate major sections with `---`, as the existing files do.

## Sources and accuracy

Factual and citation accuracy matter more here than anywhere else: the documents argue for precision, and a wrong citation undercuts the argument.

- Check a claim against its source before citing it. If you can't reach the source (paywall, 403, no transcript), say so in your summary and in the PR description, and cite the claim through a source you *could* read where possible.
- Never invent a page number, timestamp, episode title, or quotation. If one is needed and you can't verify it, ask the author.
- Flag citations written from memory so a human can check them before merge.

## Git workflow

- Branch from `main` and open a pull request; don't commit to `main` directly.
- Commit messages use a `docs:` prefix and a short imperative summary, followed by a body that explains why.
- Group a coherent change (for example, a new document plus its README row and `index.md` cross-reference) into a single commit.

## License

The repository is dedicated to the public domain under [CC0 1.0](LICENSE). Contributions are made under the same terms. Don't add material that can't be released that way, such as long excerpts from copyrighted sources.
