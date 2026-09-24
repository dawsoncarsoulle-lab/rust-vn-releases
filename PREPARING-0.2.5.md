# 0.2.5 preparation — 24 September 2026

Not a published release. Version 0.2.4 and its download hashes are unchanged.

Completed:
- Public issue tracker enabled and linked from the English README.
- French overview and bilingual installation/integrity instructions.
- New real Linux captures: launcher, simplified story graph, menu designer.
- Engine README rewritten without obsolete roadmap or unsupported comparative claims.
- Proposed editor terms separated from engine, media and prior license grants.
- Corvo bridge CC0 entry rechecked against the distributor's per-asset manifest.
- Linux and Windows release editor builds successful; 93 editor tests and five packaging-gate tests passed.
- Historical secret scan with Gitleaks 8.30.1 across all local refs after fetching: no findings. This is not a guarantee that no sensitive information exists.

Publication hold:
- The owner approved a separate public engine repository (`rust-vn-engine`); the old development repository remains private, including its historical pull-request references. Legacy test media and media-bearing archives are excluded from the public history. The public CLI starter is text-only. The full editor example is unchanged.
- Release packages must be rebuilt from the public engine source so their embedded CLI starter does not reintroduce old test assets. Existing 0.2.4 downloads are not retroactively changed by source cleanup.
- Complete dependency/font license inventory and export-notice coverage still need verification before claiming a full licensing audit.
- New editor terms preserve prior MIT grants. They cannot turn already licensed historical code into exclusive proprietary property. No independent legal review has been completed.
- Final package builds, package-level tests, upload and download verification remain pending.

Native Windows, clean Ubuntu and the other qualification gaps recorded in 0.2.4 are not marked as passed by this documentation update.
