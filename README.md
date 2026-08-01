# CyberFoundations Simulators

Standalone, browser-based training simulators for CyberVisionaries Institute's **CyberFoundations** program (Tier I). Each simulator is a single self-contained HTML file — no installs, no accounts, no real infrastructure, and no cost. Students reach these through the CVI Lab Portal.

## Simulators

| Simulator | File | Course use | Live URL (GitHub Pages) |
|---|---|---|---|
| **VM Builder Simulator** | `vm-builder.html` | Week 4, Lab 03 ★ Deliverable 1 | `https://cybervisionariesinstitute.github.io/cyberfoundations-simulators/vm-builder.html` |

## VM Builder Simulator

Students provision, manage, and decommission their first virtual machine through a realistic cloud-style flow — modeled on Microsoft Azure, which the program uses for real lab machines from Week 6 onward.

**The flow:** Basics (name + region) → Guest OS → Size tier → Admin account → Review & Create → lifecycle dashboard (start / stop / snapshot / delete) with a live, time-accelerated billing meter.

**Deliberately realistic, including the friction:** taken names are rejected (`NameNotAvailable`), weak passwords and guessable admin usernames are refused, the largest size always fails provisioning (`QuotaExceeded`), and the high-demand region fails once before succeeding on retry (`AllocationFailed`). All failure behavior is deterministic so instructors can grade against it. Four gated Concept Checks (host vs. guest, the hypervisor, Type 1 vs. Type 2, stopped-VM billing) tie back to the Week 4 lessons.

**Deliverable tie-in:** students capture `vm-config-summary.png` and `vm-dashboard-running.png` at prompted moments — the virtualization half of Deliverable 1.

## Design notes

- **Sequence-safe:** each simulator only uses concepts taught by its course week. The VM Builder has no inbound-port/firewall step (Week 7 territory) and no SSH/connect flow (Weeks 5–6) — by design, not omission.
- **Living files:** simulators expand as the curriculum does. The VM Builder's roadmap: a network info panel (Week 5), a Bastion-style browser connect flow (Week 6), a security-group rules step (Week 7), and SSH key auth (Week 8).
- **No data leaves the browser:** state is in-memory only; refreshing resets the simulation.
- **Accessibility:** halation-safe terminal colors (soft white on indigo — never pure white on black) per the program's ND-engagement standards.

## Editing / hosting

Serve via GitHub Pages (Settings → Pages → Deploy from branch → `main`). Each simulator is one file — edit it directly; version history in this repo is the changelog.

---

© CyberVisionaries Institute · CyberFoundations · Tier I
