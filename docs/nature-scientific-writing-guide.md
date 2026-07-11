# Nature-Style Scientific Writing Guide

This guide combines the drafting workflow in `nature-writing` with the diagnostic and polishing workflow in `nature-polishing`. Use it to build an argument from research materials, complete a first draft, revise an English manuscript, and perform a pre-submission check. The goal is not to imitate a “Nature voice”, but to help readers quickly understand why the work matters, what is new, whether the evidence is credible, whether the work can be reused, and where the conclusions stop.

## 1. Identify the task before writing

| Task | First step | Main deliverable |
| --- | --- | --- |
| Draft from results, figures, notes, or Chinese materials | Build the argument and section structure | Draft sections, outline, and evidence map |
| Restructure an existing draft | Diagnose article type, section roles, and paragraph logic | Reorganised draft and structural rationale |
| Polish existing English | Resolve structural and evidential issues before language | Polished text and revision notes |
| Translate Chinese into English | Translate the intended argument, not Chinese word order | Natural, accurate English matched to the evidence |

Do not limit revision to sentence polishing while any of these issues remains unresolved: the article type is wrong; the research gap is unclear; claims lack evidence; evidence lacks a claim; conclusion boundaries are missing; results and discussion are conflated; or terminology is inconsistent.

The revision order is always:

> Article type → section role → paragraph logic → claim–evidence–boundary → sentence expression

## 2. Minimum preparation before writing

### 2.1 Write a one-sentence argument

Summarise the paper using this form:

> In [system or problem], we achieve or discover [advance] through [method], supported by [key evidence]; its scope is limited by [boundary].

If this sentence cannot be written, complete the research argument before drafting. Every section and paragraph should serve it.

### 2.2 Create a terminology ledger

When first processing the materials, fix the standard forms of key terms, abbreviations, symbols, model names, dataset names, metrics, units, and proper nouns. Use the same form throughout the manuscript, captions, supplementary material, and later revisions; do not reintroduce variants while editing.

### 2.3 Specify the article type

| Type | Core reader question | Writing focus |
| --- | --- | --- |
| Research article | What was found, and what does it mean? | Phenomenon or mechanism, evidence, and significance |
| Methods article | Does the method work, outperform alternatives, and remain reproducible? | Validation, advantages, and conditions of use |
| Hypothesis/mechanism article | Is the causal explanation justified? | Targeted evidence and alternative explanations |
| Algorithm, system, or device article | Is performance reliable, comparison fair, and failure understood? | Benchmarks, fair comparisons, robustness, and failures |
| Review | What is known, disputed, and still open? | Problem-centred synthesis rather than paper-by-paper listing |

#### Argument chains and drafting order by type

- **Research article:** Use an hourglass structure: broad context → precise gap → finding and evidence → broad significance. Start with the results narrative and normally proceed as results → introduction/conclusion → title → discussion → methods → abstract, so an overdeveloped introduction does not constrain the results narrative.
- **Methods article:** Fix the method definition, inputs and outputs, assumptions, and evaluation protocol before writing validation. Results must state whether the method is more reliable, faster, less resource-intensive, or easier to reproduce, and whether comparisons use the same data split, preprocessing, and budget.
- **Hypothesis/mechanism article:** State the hypothesis explicitly in the introduction and specify in advance what observation would falsify it. Distinguish evidence supporting the hypothesis from evidence consistent with it but unable to rule out alternatives; correlation alone does not justify causal verbs such as `causes` or `drives`.
- **Algorithm, system, or device article:** Separate what the system is, why it works, and how well it performs. Every performance claim should identify the dataset, metric, baseline, and experimental conditions; the discussion must identify experimentally revealed failure modes.
- **Review:** Define the subfield, time window, and inclusion criteria first. Organise around disputes, evidence, and questions rather than papers. Judgements are acceptable when their basis is shown, and the conclusion should leave readers with a usable map of the field.

### 2.4 Define the readers and submission context

Readers usually ask, in order:

1. **Relevance:** Why does this matter to me?
2. **Novelty:** What is new?
3. **Credibility:** Is the evidence sufficient?
4. **Reusability:** Can I use, test, or extend it?
5. **Significance and boundary:** What does it mean, and when does it not hold?

For a broad audience, establish relevance and novelty before technical detail. Identify the target journal, primary audience, word limit, and results that need emphasis.

## 3. Workflow from materials to first draft

1. **Collect facts:** Organise claims, figures, results, controls, ablations, statistics, limitations, and literature. Distinguish established facts, reasonable inferences, and missing information.
2. **Set the argument:** Complete the one-sentence argument, identifying the results that best support it and its non-negotiable boundaries.
3. **Plan sections and paragraphs:** Each paragraph has one role only: background, gap, method, result, comparison, mechanism, significance, or limitation. Split paragraphs that serve two roles.
4. **Align at a confirmation gate:** Before a full section or major restructuring, confirm the one-sentence argument; article type, sections, journal, and length; paragraph map; terminology ledger; primary readers; inferred key assumptions; and at most two or three high-impact questions. When claims, evidence, and boundaries are clear, confirm only the one-sentence argument. When the issue is solely stylistic, request a short sample written by the author and calibrate sentence length, tone, hedging, person, and connectives without reusing factual content.
5. **Build the evidence ladder first:** For each major claim, identify direct evidence, controls or baselines, necessary ablations or stress tests, and evidence still missing.
6. **Draft outwards from evidence:** Place claims close to their supporting data; do not pile conclusions at the start of a section and leave evidence to its end.
7. **Calibrate evidential strength:** Direct, sufficient evidence supports `show` or `demonstrate`; trends or indirect evidence call for `suggest` or `indicate`; unverified mechanisms require `may` or `could`.
8. **Check paragraph flow:** The first sentence gives a topic or claim; later sentences must relate clearly through causation, comparison, limitation, or example.
9. **Deliver with notes:** Preserve assumptions, missing inputs, and locations requiring more evidence. Do not conceal evidential gaps with fluent prose.
10. **Revise selectively:** After feedback, change only the identified claim or paragraph. If structural reordering is necessary, explain why. Return to step 2 when underlying premises are wrong.

## 4. Responsibilities of each section

### Title

- State the research object, central advance, or key relation in the fewest words.
- Avoid generic promotional terms such as `novel`, `first`, and `unprecedented` unless they can be rigorously supported.
- Use terminology consistent with the abstract, figures, and main conclusion.
- Choose a noun phrase (often methods), declarative statement (findings), “system name: function” form, or gerund/question form (often benchmarks or perspective pieces) according to the paper’s selling point. Usually reserve numbers and full conclusions for the abstract and results.

### Abstract

Organise as background → gap → method/strategy → key result → significance → boundary. Retain only background needed to understand the problem; key results must trace to specific data; significance must not exceed the evidence. Finalise the title and abstract after the main argument and results narrative are stable.

Before drafting, answer four questions: What technical problem remains unsolved? What is the technical contribution? Why is it feasible? What technical advantage or insight does it provide? Then choose a suitable framework:

- **Challenge → contribution:** task → technical challenge in existing methods → one or two contribution sentences → advantages → experimental summary.
- **Challenge → insight → contribution:** task → challenge → core insight → contribution implementing that insight → advantages → experiments.
- **Multiple contributions:** task → optional comparison → each contribution and its advantage → experimental summary.

Afterward, check whether readers can identify the task, challenge, contribution, and result in one pass; whether every major claim has experimental support; whether technical names are internally consistent; and whether every sentence carries only necessary information.

#### Broad-audience summary paragraph for Nature journals

For a summary paragraph aimed especially at interdisciplinary readers, use a seven-step funnel:

1. Broad field introduction (one or two sentences);
2. Minimum necessary background (two or three sentences);
3. One explicit unknown;
4. The main result using `Here we show/demonstrate`;
5. The direct implication of that result;
6. Broad significance anchored in evidence;
7. A high-level outlook, when needed.

Without an outlook this is usually about 190 words; with one, about 250 words. Avoid opening with dense proper nouns, omitting a clear gap, revealing the main result too early or too late, listing data without interpretation, or overstating impact at the end.

### Introduction

Narrow progressively from the field scale:

1. Why the problem matters;
2. The current bottleneck;
3. What existing approaches achieve and still lack;
4. The specific gap addressed here;
5. This paper’s approach, main results, and contribution boundary.

Do not let method detail obscure novelty, and do not create novelty by disparaging previous work.

First reason **backwards**: identify the technical challenge, contribution, and advantage, then decide how to lead readers to the challenge. Draft forwards as task → technical challenge → contribution → advantage/insight → evidence.

For an unfamiliar task, define it before giving applications; for a known task, begin with an application; for a specific scenario, narrow from the general task. If failures are the main selling point, begin directly with the challenge.

Do not introduce a naïve approach only to say that the present work performs better, because that weakens the necessity of the problem. Do not offer an abstract insight without a concrete workflow, which creates an illusion of innovation.

### Methods

Explain each module’s motivation, design, forward process, and technical advantage so readers can judge reproducibility and scope. Methods articles must also clearly present validation, conditions for comparison with alternatives, and failure modes.

Recommended sequence: draw the complete workflow → plan subsections from it → state motivation, design, and advantage for each subsection → write the concrete design first → add motivation and advantage. Every module must answer:

1. **Motivation:** Why is it needed, and why is the obvious alternative inadequate?
2. **Design/mechanism:** What are the inputs, processing steps, and outputs?
3. **Technical advantage:** What specifically improves over alternatives, preferably in observable or measurable behaviour?

An opening overview can follow task setting → core contribution → framework-figure pointer → subsection contents. Check three levels: can readers restate the overall logic; does each paragraph’s first sentence state its task; and does every sentence make clear why it exists?

### Results and experiments

Results are an evidence ladder, not an experimental log. Each subsection answers one question: What is the main result? What is it compared with? How are alternative explanations excluded? Under what conditions does it hold? Algorithmic or systems work must report baselines, data splits, metrics, fair comparisons, ablations, robustness, and failure cases.

Experiments should answer at least:

1. Does the approach outperform strong baselines under identical data splits, preprocessing, and evaluation protocols?
2. Which modules or design choices produce the gains? Use removal, replacement, or disabling ablations for every key module.
3. How far does it generalise under harder conditions? Stress-test it with complex scenarios, out-of-distribution inputs, or stricter constraints, reporting both gains and failures.

An ablation package should include one core table spanning the main contributions, small ablations for design choices, and qualitative visualisations for important ablations. Follow one table, one message: place the title above the table; avoid vertical rules, double rules, and dense horizontal rules; specify metric directions and units; use consistent precision; left-align text columns; group headers when needed; and mark best and second-best values sparingly.

### Discussion and conclusion

The discussion explains the meaning of results, relation to prior work, limitations, and testable next steps; it does not repeat results. The conclusion consolidates contributions, strongest evidence, potential impact, and boundaries, without leaping from local results to universal conclusions.

### Related work and reviews

Organise around themes, disputes, evidence types, and open questions rather than paper-by-paper summaries. Clearly identify what belongs to prior work, the present work, and competing interpretations.

List direct competitors and the latest strong baselines first, then group work into two to four technical themes: mainstream task approaches, approaches closest to the central idea, and necessary supporting technologies. Each paragraph should define the theme, summarise representative paradigms, identify limitations relevant to the present challenge, and lead naturally to the present difference. Do not turn related work into a chronological bibliography.

After section drafts are complete, confirm that each fulfils its distinct responsibility before revising paragraphs and sentences.

## 5. Revising paragraphs and sentences

### 5.1 Paragraph checks

Ask of each paragraph:

- What is its single task?
- Does the first sentence state the topic or claim directly?
- Does every later sentence advance it through causation, comparison, qualification, or example?
- Is relevant evidence placed immediately after the claim?
- Does it include content that belongs in another paragraph or section?

When needed, make a reverse outline: write one sentence explaining what each paragraph does, then reorder where adjacent sentences or paragraphs repeat, jump, or leave a gap.

A complete reverse outline:

1. State the section argument;
2. State every paragraph’s topic sentence;
3. List evidence or explanation under each paragraph;
4. Check whether the topic sentences jointly support the section argument;
5. Check whether the evidence supports each topic sentence;
6. Rewrite, move, or remove content that cannot be mapped.

Also test whether terminology is understandable without hidden context and whether every sentence connects to the preceding one through cause, contrast, consequence, elaboration, or illustration.

### 5.2 Language checks

- Keep sentences short, explicit, and readable; remove stock phrases and redundant qualifiers that add no information.
- Prefer precise nouns and verbs to abstract, inflated, or generic wording.
- Keep terminology, abbreviations, tense, units, symbols, and figure numbers consistent.
- In English translation, preserve logical relations and evidential strength rather than copying Chinese word order.
- Avoid absolute terms such as `always`, `never`, `complete`, `comprehensive`, `unique`, and `first`. Remove them or qualify their scope when they cannot be demonstrated.

More detailed Nature-oriented rules:

- Usually keep sentences to 10–30 words and avoid placing multiple claims in one sentence; inspect long sentence endings especially carefully.
- Avoid em dashes, contractions (such as `don't`), and rhetorical questions; do not join two independent clauses with a comma.
- Use British spelling by default. Use `a/an` for a singular countable noun on first mention, `the` for a subsequent specific mention, and usually no article for generic plurals.
- Use Arabic numerals for measurements, with a space between number and unit (for example, `25 cm`); use en dashes for ranges.
- Figure legends are usually no longer than 300 words and titles no longer than 75 characters; journal instructions take precedence.

#### Five steps for translating Chinese materials into English

1. List the core propositions in English first;
2. Reconstruct contrasts, causation, inferences, and limitations explicitly;
3. Verify terminology and causal and hedging strength;
4. Lock model names, dataset names, and technical terms rather than varying them for style;
5. Apply English sentence and paragraph conventions only at the end.

Common repairs include selecting past or present tense from factual status; correcting countable-noun number; turning nested modifiers into relative clauses or separate sentences; changing “about X” topic sentences into subject–verb–object sentences; varying repetitive “this paper/we” openings; supplying a baseline for “significantly improved”; and splitting comma-spliced short sentences.

#### Evidential strength and linking expressions

| Purpose | Suitable expressions |
| --- | --- |
| Strong direct evidence | `show`, `demonstrate`, `establish`, `reveal`, `identify` |
| Limited or indirect evidence | `suggest`, `indicate`, `are consistent with`, `point to` |
| Speculative explanation | `may reflect`, `could arise from`, `appears to`, `might be explained by` |
| Contrast | `however`, `by contrast`, `nevertheless`, `whereas` |
| Causation or result | `therefore`, `thus`, `consequently`, `as a result` |
| Qualification | `notably`, `in part`, `approximately`, `at least in this cohort` |

Avoid repeating `This suggests`. Instead, use a restated noun (`Such heterogeneity ...`), a definite noun phrase (`The resulting gradient ...`), a summarising participial construction (`Taken together, ...`), or no connective when the logic is already clear. A useful convention for *Nature Communications* is to make result sentences affirmative and numerical, while concentrating hedging in significance sentences; do not use `significantly` as generic emphasis without statistical support.

## 6. Claim–evidence–boundary map

For every major claim during drafting and before submission, complete:

| Claim | Supporting evidence | Status | Boundary/limitation |
| --- | --- | --- | --- |
| Main finding or performance gain | Relevant figure, statistic, comparison, or replication experiment | Supported / evidence needed / inference | Sample, condition, comparison scope, or unverified mechanism |

Any item marked “evidence needed” or “inference” must be downgraded, explicitly qualified, or marked as pending. Never disguise it as an established conclusion through coherent prose.

## 7. Ethics, citations, and boundaries of AI use

- Acknowledge the prior ideas, data, methods, and explanations on which the research builds, with clear attribution.
- Cite original sources that you have actually read and verified: cite the original paper for its data, methods, and conclusions, and cite the relevant commentary for others’ interpretations or comments.
- Properly cite others’ ideas, data, methods, wording, structure, images, and distinctive explanations; public availability online does not automatically place material in the public domain.
- AI may improve grammar, clarity, concision, tone, outlines, translation, and title options, but authors must verify every item.
- Do not include unverified AI-generated citations, data, claims, or images in a manuscript, and do not upload unpublished manuscripts, sensitive data, or peer-review materials to public models.
- AI cannot replace authors’ responsibility for the central argument, evidence, methodological explanation, and final work.

Citations also position work: use **support** for premises, **borrow** for adopted methods, frameworks, or protocols, **contrast** for differing results, settings, or interpretations, and **reuse/adaptation** for materials, data, code, or images used. Position prior work fairly with a structure such as “previous work has established X, but Y remains unclear under Z,” rather than implying that it has no value.

## 8. Pre-submission checklist

- [ ] The one-sentence argument includes problem, advance, method, evidence, and boundary.
- [ ] The article type matches the section architecture.
- [ ] Readers can find relevance, novelty, credibility, reusability, significance, and boundaries in sequence.
- [ ] Every paragraph has one task, and its first sentence states a topic or claim.
- [ ] Every major claim has adjacent, sufficient evidence.
- [ ] Verb strength matches evidential strength.
- [ ] Results and discussion are distinct, and discussion does not list results again.
- [ ] There are no unsupported claims of being first, unique, comprehensive, or universal.
- [ ] Terminology, abbreviations, symbols, units, figure and table numbers, and citations are consistent and correct.
- [ ] Citations attribute accurately, and sources for figures, data, and wording have been checked.
- [ ] Grammar, spelling, formatting, and readability have been checked.

### Adversarial self-review

From a reviewer’s perspective, examine five rejection risks: whether the contribution is merely a common failure case or an already well-explored technique; whether method and motivation enable reproduction; whether improvement is substantively meaningful rather than merely statistically significant; whether ablations, strong baselines, and difficult data are complete; and whether the experimental setting is realistic, the method has hidden flaws, and net benefit is positive. Turn every risk into an answerable question and point each answer to evidence in the manuscript. Where no answer exists, prioritise more experiments, clearer limitations, or weaker claims.

## 9. Journal and submission specifications

Before submission, follow the target journal’s current author instructions. The information below supports early planning and does not replace official requirements.

| Context | Planning focus |
| --- | --- |
| Nature journals | Prefer cutting content to compressing sentences into unreadability; make the first sentence meaningful to non-specialists; use an unstructured abstract where customary; place methods near the end; avoid em dashes; and expect strict reference limits. |
| *Nature Communications* | Main text and methods are commonly about 5,000 words; reserve roughly 700 words for the introduction, 2,000 for results, 800 for discussion, and 1,500 for methods early on; use an approximately 150-word, citation-free abstract focused on findings; normally keep figures and tables to 10 in total and move extras to supplementary information; prepare data and code availability statements, the Reporting Summary, and cover letter early. |
| General journals | Before drafting, confirm formatting, word limits, citation style, audience scope, and whether a significance/author summary, graphical abstract, highlights, or keywords are required. |

## 10. LaTeX layout diagnosis and repair (optional)

Address layout problems through modify → compile → read logs → render page images → inspect visually → iterate; do not inspect only the `.tex` source. In logs, prioritise `Float too large`, `Overfull \vbox`, and unresolved citations. Render the PDF to page images and make a contact sheet to find blank pages, orphaned headings, and unbalanced figures quickly.

- When float pages are too loose, adjust the top, spacing, and bottom glue so content aligns to the top.
- When wide, short figures cannot fill a page, redraw them from source with a taller aspect ratio (commonly about 1.9:1–2.2:1) instead of rotating the page.
- Avoid landscape main-text figures that force readers to turn the page; stack wide multi-panel figures vertically where possible.
- When float congestion isolates a section heading, use `\clearpage` and `[H]` to treat the heading and figure as a unit, but use `[H]` only when sufficient space is available.
- `placeins` affects global float behaviour; test it with figure dimensions and placement instead of treating it as a universal fix.

## 11. Recommended delivery format

### Drafting or restructuring

1. **Draft:** The requested English draft.
2. **Section outline:** Three to seven paragraph-level bullets for a complete section.
3. **Assumptions or missing inputs:** Only assumptions or missing information affecting the argument.
4. **Claim–evidence map:** Major claims and their evidential status.
5. **Why this structure:** A brief explanation of the structural choice.

### Polishing

1. **Polished text:** Provide the polished text directly.
2. **Revision notes:** Explain major structural and expression changes, including issues that cannot be fixed without inventing content.
3. When sentence-by-sentence comparison is needed, present **Original / Polished / Why changed**.

This guide is intended to improve clarity, argument, and expression. It must not be used to fabricate scientific content, minimise uncertainty, or evade author responsibility.
