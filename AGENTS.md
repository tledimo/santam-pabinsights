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
- CMDB lives in src/data/cmdb.ts with one tabbed route /cmdb; Jira Assets objects are pulled by syncJiraAssets (src/lib/jira-assets.functions.ts) and cached as a browser snapshot that replaces the sample CIs/relationships via loadCis/currentRels; why: pages stay source-agnostic.
- Release Management (src/data/release-management.ts, /release-management) and Certificate Management (src/data/certificate-management.ts, /certificate-management) are separate browser-stored modules; future providers plug in via src/lib/integration-adapters.ts; why: no hard-coded vendor integrations and modules stay independent of Change Management.
