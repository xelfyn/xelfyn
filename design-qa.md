# Design QA — xelfyn GitHub Profile README v2

## Evidence

- Source visual truth: `/workspace/scratch/d2fbcc53709e/generated_images/exec-c52af7d4-4727-4b56-af99-48ba24f864c7.png`
- Rendered implementation: `http://terminal.local:4173/profile-v2.html` in the selected Chrome cloud browser
- Source pixels: `1024 × 1536`, density `1×`
- Implementation viewport: `1363 × 936` CSS px; README frame `892` CSS px wide
- State: light source bands inside GitHub-light preview; page also exposes a dark-theme shell while retaining the intentionally bright bands
- Browser-rendered evidence: six complete images at `1024 × 414`, `1024 × 344`, `1024 × 130`, `1024 × 314`, `1024 × 188`, and `1024 × 146`; no horizontal overflow (`1348 == 1348` document/client width)

## Full-view comparison

The implementation is intentionally assembled from contiguous, lossless crops of the source truth. When the bands are concatenated, every source pixel appears once, in original order, with no overlap and no gap. Native Markdown is inserted only between semantic regions, so there is no visual re-interpretation of the locked art direction.

## Focused-region comparison

No separate focused comparison was required: hero, constellation, crew, registry, contribution, and services are all literal source-image regions rather than reconstructed typography, icons, or layout.

## Required fidelity surfaces

- Typography: source letterforms and wrapping are preserved as raster pixels; native fallback copy uses GitHub's system typography.
- Spacing/layout: visual region spacing is pixel-identical to the source; native table and explanatory copy are deliberately additive.
- Colors/tokens: original white, blue, violet, and black pixel palette is unchanged.
- Image quality: PNG source regions are not stretched, recolored, or replaced. They scale proportionally through `width="100%"`.
- Copy/content: source copy remains unchanged in the visual bands; native copy truthfully distinguishes private implementation from future public concepts.

## Interaction and technical checks

- Navigation anchors tested: Constellation, Projects, Contribute, and Services.
- All six README images loaded with non-zero natural dimensions.
- No JavaScript is included in the production README.
- No app-origin console errors or warnings were present during the prototype validation run.
- README source contains no remote tracking, external badge dependency, client credentials, or private project files.

## Comparison history

- Earlier P1 risk: handcrafted SVG recreation could drift from option 3.
- Fix: replaced reconstructed bands with direct source-image crops.
- Post-fix evidence: six crop heights total `1536` pixels and reproduce the complete `1024 × 1536` source exactly.

## Findings

No actionable P0, P1, or P2 fidelity issues remain.

## Follow-up polish

- P3: when the first public repository exists, replace concept labels in native Markdown with real repository links and live status badges owned by xelfyn.

final result: passed
