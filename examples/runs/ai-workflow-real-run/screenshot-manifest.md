# Screenshot manifest

These screenshots are captured from the real run result pages in this folder.

They are not standalone generated marketing diagrams. Each screenshot maps back to `run-output.md`.

| Screenshot | Source page | Captured section |
| --- | --- | --- |
| `docs/assets/real-run-01-candidate-sheet.png` | `screenshot-01-candidate-sheet.html` | Visual Candidate Sheet |
| `docs/assets/real-run-02-ip-card.png` | `screenshot-02-ip-card.html` | User-facing IP Card |
| `docs/assets/real-run-03-visual-plan.png` | `screenshot-03-visual-plan.html` | Article Visual Plan |
| `docs/assets/real-run-04-exported-skill.png` | `screenshot-04-exported-skill.html` | Exported personal skill |

Capture command pattern:

```bash
perl -e 'alarm shift; exec @ARGV' 60 \
  '/Applications/Google Chrome.app/Contents/MacOS/Google Chrome' \
  --headless=new \
  --disable-gpu \
  --no-first-run \
  --no-default-browser-check \
  --hide-scrollbars \
  --window-size=1440,960 \
  --screenshot=docs/assets/{screenshot}.png \
  file:///.../examples/runs/ai-workflow-real-run/{source}.html
```
