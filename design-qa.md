# Future Savings Design QA

## Evidence

- Selected design source: `/Users/takashi/.codex/generated_images/019f18e8-ae1c-7b90-b001-da3f1326b3d1/exec-193cc4e2-1a82-42fd-96d9-a008291dace1.png`
- Desktop implementation: `/private/tmp/future-savings-v5-desktop-final.png` (1440 x 1024)
- Side-by-side comparison: `/private/tmp/future-savings-design-comparison.png`
- Mobile implementation: `/private/tmp/future-savings-v5-mobile.png` (390 x 844)
- Narrow mobile implementation: `/private/tmp/future-savings-v6-mobile-320.png` (320 x 844)
- Compared in the same default dark-theme state.

## Fidelity Review

- Typography: The large Japanese editorial headline, compact technical labels, and high-contrast numeric displays preserve the selected direction.
- Layout: The desktop split hero, real app screens, dual money/time signals, and numbered feature bands follow the selected composition. Mobile changes to a single-column flow without horizontal page overflow.
- Color: Matte black, cyan structure lines, acid-lime values, and restrained violet accents remain consistent.
- Imagery: Production app screenshots replace conceptual screens while retaining the angled-device hierarchy. The raster cyber-grid texture supplies atmosphere without obscuring content.
- Copy: The experience is framed around both accumulated money and disposable personal time. The former unnatural `円で` wording is not used.

## Iteration History

1. The first mobile hero pushed the next section below 1100 px. Low-priority descriptive copy was hidden on narrow screens and the device stage was clipped, bringing the next-section signal to about 733 px.
2. Automatic line wrapping split key Japanese phrases awkwardly. Explicit semantic line breaks were added to major headings.
3. The 320 px navigation showed a partially clipped item. Secondary privacy and app-list links were removed from the compact header and retained in the footer.

## Remaining Variance

- P3: The real app screens are slightly smaller and more separated than the conceptual source. This preserves screenshot legibility, avoids overlap, and keeps the mobile implementation stable.
- No P0, P1, or P2 visual issues remain in the checked viewports.

## Result

passed

---

# App Index Design QA

## Evidence

- Source visual truth: `/Users/takashi/.codex/generated_images/019f18e8-ae1c-7b90-b001-da3f1326b3d1/exec-d57e5ea4-6ecd-4a6c-9c19-db0272918118.png`
- Desktop implementation: `/private/tmp/apps-portfolio-desktop-final.jpg` (1440 x 1166)
- Tablet implementation: `/private/tmp/apps-portfolio-tablet-viewport-after.jpg` (842 x 673)
- Mobile implementation: `/private/tmp/apps-portfolio-mobile-final.jpg` (390 x 844)
- Side-by-side comparison: `/private/tmp/apps-portfolio-qa-comparison.jpg`
- State: initial app index, no interaction state applied.
- Browser-rendered evidence: Codex in-app browser against `http://127.0.0.1:4173/`.

## Fidelity Review

- Fonts and typography: System Japanese gothic and monospace metadata reproduce the source hierarchy without requiring a network font. Personal-name branding is absent.
- Spacing and layout rhythm: The desktop uses two equal product panels inside one dark portfolio shell. Tablet switches to a single column at 1020 px, and mobile continues the single-column flow with no horizontal overflow.
- Colors and visual tokens: The shared shell stays near-black; Future Savings uses cyan over its supplied grid texture; AssetScope uses a pale surface with cobalt accents.
- Image quality and asset fidelity: The original app icons and production screenshots are used directly. Images preserve aspect ratio and are fully contained in their panels at desktop and mobile sizes.
- Copy and content: Both apps have a short value statement, concise description, release status, and clear detail-page action. No developer name appears.

## Interaction And Browser Checks

- Page identity: passed (`つくったアプリ | Independent Projects`).
- Blank page / framework overlay: passed; semantic content rendered and no overlay appeared.
- Console health: passed; no warnings or errors in the checked desktop and mobile states.
- Interaction: passed; selecting Future Savings navigated to `/future-savings/`, and browser back returned to the index.
- Responsive layout: passed at 1440 px, 842 px, and 390 px. Computed document width matched the viewport in every state.
- CTA clearance: passed at 1440 px, 842 px, and 390 px. The `詳しく見る` controls do not intersect either app screenshot.

## Comparison History

1. P2: The first implementation clipped the lower edge of both product screenshots inside their panels, especially on mobile.
2. Fix: Removed negative mobile margins, reduced desktop image width, and placed both images inside the panel bottom edge.
3. Post-fix evidence: Browser geometry checks report both images contained within their panels at 1440 px and 390 px; the revised mobile capture shows both complete screens.
4. P2: At 842 px, the two-column tablet layout made both `詳しく見る` controls overlap the absolutely positioned iPhone screenshots.
5. Fix: Changed the gallery to one column at 1020 px and constrained the tablet screenshot width to 42% of the full-width panel.
6. Post-fix evidence: At 842 px, both CTA/image intersection checks return false, while 1440 px remains two columns and 390 px retains its static single-column image flow.

## Remaining Variance

- P3: The implementation uses horizontal app names rather than the mock's decorative vertical titles. This is intentional for Japanese readability and future app-card reuse.
- P3: Product screens are slightly smaller than the concept so their full outlines remain visible on mobile and desktop.
- No actionable P0, P1, or P2 findings remain.

## Focused Comparison

A separate focused crop was not required because the supplied production icons and screenshots are used without redraw or replacement, and their complete outlines are visible in the final browser captures.

final result: passed
