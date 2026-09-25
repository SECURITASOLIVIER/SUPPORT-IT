# IT Pocket / Super Support IT — Agent Working Contract

This repository is migrated to a gstack-style workflow without replacing the existing product.

## Golden rule
Preserve working behavior. Do not rewrite, reorganize, remove, rename, or simplify unrelated features unless the user explicitly asks for it.

## Baseline
- Frozen pre-migration branch: `archive/pre-gstack-2026-09-25`
- Baseline commit: `75f775c1e7c5e3cde94bc322b78231b9ec0f02f9`
- Migration work branch: `migration/gstack`
- The frozen branch is a rollback reference and must not be modified.

## Change workflow
For every change:
1. Inspect the current implementation before editing.
2. State the exact requested scope internally.
3. Identify affected functions/UI areas and regression risks.
4. Make the smallest targeted patch possible.
5. Do not refactor unrelated code.
6. Compare changed behavior with the frozen baseline when relevant.
7. Verify navigation, mobile layout, existing menus, templates, scripts, buttons, links, favorites/recent state and language behavior when touched.
8. Treat a previously validated feature as frozen unless it is directly part of the request.
9. Do not merge to `main` until the change is verified.

## Product DNA
- Mobile-first IT technician companion.
- Simple, fast navigation and immediate identification of actions.
- Existing content and functions are more important than cosmetic refactors.
- Communications, scripts/commands, portals, browser/Office/Windows/Intune/Entra support content must remain usable.
- Templates must remain copyable/editable where supported.
- Avoid duplicate labels, duplicate subjects and unnecessary previews.
- Use official technology logos when appropriate; use Fluent/Windows-style icons for system actions.
- Keep visual hierarchy clean and professional, not overly flashy.
- FR/EN must be coherent across the whole interface when language switching is enabled.
- Mobile usage must never attempt to execute Windows PowerShell locally; scripts are reference/copy content only.
- Do not introduce company-specific names into generic product branding.

## Security principles
- Never store Microsoft/Office passwords in the site.
- Never persist access tokens unnecessarily.
- Prefer short-lived, least-privilege sessions for any future Microsoft Graph integration.
- Do not expose secrets in HTML/JavaScript/GitHub.
- Separate read-only information access from privileged actions.
- Any authentication/security change requires a dedicated security review.

## Definition of done
A change is complete only when the requested behavior works and unrelated validated behavior remains intact.
