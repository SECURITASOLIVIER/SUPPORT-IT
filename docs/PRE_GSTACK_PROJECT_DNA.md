# Pre-gstack baseline and project DNA

## Purpose
This document preserves the intent accumulated before the gstack-style migration so future work can improve the product without losing validated behavior or design decisions.

## Rollback point
- Repository: `SECURITASOLIVIER/SUPPORT-IT`
- Frozen branch: `archive/pre-gstack-2026-09-25`
- Baseline commit: `75f775c1e7c5e3cde94bc322b78231b9ec0f02f9`
- Baseline title: `Add files via upload`
- Baseline visible version: `Mobile 1.18.0`

The frozen branch is the exact GitHub state before the migration and is the source of truth for rollback.

## Important context preserved from pre-migration work
Recent iterations and decisions were not all committed as HTML after September 22. They must therefore be treated as product requirements, not discarded merely because the baseline file is older.

### Interface and navigation
- Keep navigation simple and quick for technicians.
- Preserve existing working menus and functions before adding or changing anything.
- Home cards must stay aligned and visually balanced.
- Communication cards must remain readable and must not show unnecessary content previews.
- Avoid duplicated subject/object text.
- Use a clear "see more"/detail interaction when full content would overload a card.
- Official product logos should be used for Microsoft 365/Word/Excel/PowerPoint/Outlook/Teams/OneDrive/Edge/Chrome/Firefox/Intune/Entra when appropriate.
- Use Windows/Fluent-style icons for local/system functions instead of repeating generic icons.
- Avoid excessive padlock/ticket emoji repetition.

### Content
- Preserve all existing communication templates, scripts, commands, portals and diagnostic themes unless an explicit cleanup is requested.
- New content must be additive by default.
- Review templates for wording errors before publishing.
- Maintain copy/edit/share/Open-in-Outlook style actions where implemented.
- The mobile site is a consultation/copy companion; it does not execute PowerShell on the phone.

### Language
- When FR/EN switching is enabled, the whole interface and its menus/options should switch coherently; partial translation is not acceptable.

### Microsoft/Graph direction
- Future Microsoft 365 recent-files/sites/activity views should be read-only by default.
- Support simple filters such as recent 10/30/100, date and alphabetical order when that feature is implemented.
- Avoid permanent Microsoft sessions.
- Use least privilege and short-lived tokens; never store Office passwords or secrets in the front end.
- After inactivity, sensitive authenticated views should expire/close rather than remain indefinitely connected.

### Development behavior
- Do not rebuild a large section to fix a small layout problem.
- Do not regress previously validated functionality.
- Every change should be a targeted patch unless the user explicitly requests a redesign.
- When in doubt, compare against the frozen branch and preserve behavior.

## Migration principle
The gstack-style workflow is an engineering process improvement, not a product rewrite. The product DNA above has priority over automated refactoring or stylistic cleanup.
