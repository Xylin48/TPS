# R2-3PO Git history provenance audit — 2026-11-15

**Reporting organization:** Xylin48 (HydraGames)  
**Filed by:** Z3R0 C001  
**Purpose:** Determine whether an earlier R2 GitHub commit history can be substantiated before the initial October 8, 2026 source uploads.

## Investigation and findings

1. The accessible `Xylin48/R2-3PO` repository's `main` branch returned **96 commits** in the GitHub commit search, ordered by committer date. The oldest returned mainline commit was [714d510](https://github.com/Xylin48/R2-3PO/commit/714d510734514c55300db1cc1ac127e109a46a3d), recorded October 8, 2026 at 07:19:39 UTC.
2. Its next source uploads were [8690e12](https://github.com/Xylin48/R2-3PO/commit/8690e12f1f5f2a84f5344a9c8c5120e1e5e59675), [ebdc11c](https://github.com/Xylin48/R2-3PO/commit/ebdc11c37c12508fa74508bb970e5f232d9a4e5b), and [d74eb4d](https://github.com/Xylin48/R2-3PO/commit/d74eb4d337415d6844a8f8d2fec2c601975af459), all on October 8, followed by [38260b0](https://github.com/Xylin48/R2-3PO/commit/38260b0ddbd51c9b2a6b975cb60c11df3753f46d).
3. GitHub compare between `714d510` and `main` reported `ahead_by=95`, `behind_by=0` and `merge_base_commit=714d510`. This is consistent with the oldest returned commit being the base of the 96-commit mainline.
4. Tested side branches `R2_Home`, `feature/pockets-room-world`, `feature/sensory-journal-alternate-self`, and `tv` also compared ahead of `714d510` with no behind commits; each comparison returned `714d510` as the merge base. The repository has many other branches not individually ancestry-checked.
5. An old repository alias `Xylin-Holstein/R2-3PO` resolved to `Xylin48/R2-3PO`; it was not an independently accessible older repository in this check.
6. [Issue #1](https://github.com/Xylin48/R2-3PO/issues/1), titled `r2`, was created on **October 8, 2026 at 07:14:42 UTC**, earlier than the oldest returned commit. This is an **issue**, not a pull request. Its empty body provides no source implementation evidence.
7. Additional commit searches with date qualifiers for pre-October 8 returned no matching commits. Those negative text searches do not establish the absence of all older objects.

## What this does **not** establish

- October 8 is **not** proven to be the beginning of R2 development. The first uploads already contained a core, shell, diary, Ears, Eyes, and launcher; those files could have existed locally before upload.
- An unrelated private repository, an inaccessible reflog, old device backup, deleted branch, shallow/migrated source, or unconnected Git history would not necessarily appear in these results.
- A complete graph-level ancestry proof for every one of the repository's side branches was not performed.
- No source change, production deployment, physical robot test, or software-completeness claim follows from this provenance audit.

## Next evidence required for dates earlier than October 8

Earlier local Git repositories, commit bundles, export archives, file backups containing timestamps, or an independently accessible predecessor repository are needed to substantiate older development dates. Prefer immutable Git objects where available; distinguish filesystem timestamps from original authoring dates.

**Filing decision:** Do not fabricate TPS reports dated before October 8 based solely on the current accessible repository. Continue the archive once earlier evidence is identified.
