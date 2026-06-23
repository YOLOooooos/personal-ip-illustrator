# Article Visual Planning

Use this reference to decide where an article deserves illustrations and what each illustration should do.

## Visual Value Score

Score each paragraph or section from 1-5:

- **5**: must visualize. The section contains the main idea, a hard abstraction, a key method, a decisive contrast, or a highly shareable conclusion.
- **4**: strong candidate. The section introduces an important concept, sequence, example, risk, or memorable scene.
- **3**: optional. The section can support an illustration, but the article still works without it.
- **2**: low value. The section is transitional, explanatory filler, or repeats a previous point.
- **1**: do not illustrate. The section is housekeeping, setup, citation, or already visually obvious.

## High-Value Signals

Prioritize sections that contain:

- The first appearance of the article's core concept.
- A counterintuitive claim or reversal.
- A process, framework, or multi-step method.
- A comparison between wrong and right approaches.
- A concrete case or scenario.
- A risk, trap, failure mode, or misunderstanding.
- A sentence that could become a shareable card.
- The final synthesis or action recommendation.

## Illustration Types

- **Cover**: compress the article's main tension into one scene.
- **Concept metaphor**: turn an abstract idea into a visible object or environment.
- **Process illustration**: show a sequence, pipeline, decision tree, or workflow.
- **Contrast**: compare two approaches, states, or mental models.
- **Scenario**: dramatize a concrete user, creator, team, or product moment.
- **Risk warning**: show a trap, failure mode, hidden cost, or wrong assumption.
- **Summary card**: turn the conclusion into a visual memory anchor.
- **Slide visual**: make a clean presentation-ready diagram or scene.

## IP Roles

Choose the IP's role per image:

- **Guide**: leads the reader through a complex map or system.
- **Operator**: performs the method or manipulates the workflow.
- **Observer**: notices a hidden pattern or anomaly.
- **Diagnostician**: points to a failure mode or cause.
- **Recorder**: organizes complexity on a board, notebook, or interface.
- **Challenger**: confronts a false assumption or weak idea.
- **Narrator**: frames a story moment or transition.
- **Witness**: shows the consequence or result.

## Density Rules

- Default to 2-5 illustrations for a long article.
- Do not illustrate every heading.
- Avoid placing two illustrations next to each other unless the article is a visual essay.
- Prefer fewer stronger images over many decorative images.

## Selection Output

For every selected position, output:

- `position`
- `section_summary`
- `reason`
- `visual_value_score`
- `illustration_type`
- `ip_role`
- `scene_brief`
- `expected_reader_effect`
