<!-- LOVABLE:BEGIN -->
> [!IMPORTANT]
> This project is connected to [Lovable](https://lovable.dev). Avoid rewriting
> published git history — force pushing, or rebasing/amending/squashing commits
> that are already pushed — as it rewrites history on Lovable's side and the
> user will likely lose their project history.
>
> Commits you push to the connected branch sync back to Lovable and show up in
> the editor, so keep the branch in a working state.
<!-- LOVABLE:END -->

## Portfolio architecture
- Keep the main portfolio on the index route with native section anchors; case studies use the dynamic /work/$slug route for shareable detail pages.
- Keep visual roles and motion in the global semantic design system; this preserves consistent styling across sections.
- Import uploaded media through Lovable asset pointers, preserving original images; missing client media must remain explicitly labeled rather than fabricated.
- Keep all editable case study content in src/data/caseStudies.ts; shared views render this data to prevent content duplication.
- Render optional screenshot comparisons inside the existing Screens section with native range controls; this preserves page order and keyboard/touch accessibility.
- Mask sensitive screenshot contents before CDN upload; portfolio previews must not expose private operational records.
- Keep call-booking destinations in src/lib/booking.ts and track case-study links by slug; all booking buttons must use the same appointment destination.
