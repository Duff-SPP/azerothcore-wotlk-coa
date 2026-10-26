---
area: game
type: changed
audience: players
title: Direct recruiter and recruit pairs can grant earned levels in either direction
---
Level grants now work in both directions for directly linked RaF accounts. Recruiters earn grant
credits with the same existing one-per-two-levels progression rule as recruits. Existing balances
are preserved; no retroactive credits are added.

The donor still needs available credit and a higher level. Group, faction, proximity, level caps,
consent, expiry and acceptance-time validation remain enforced. Same-account characters, sibling
recruits and unrelated recruiters cannot exchange levels. Native summon/teleport and XP rules remain
unchanged. No SQL migration is required.

Characters actively leveling through Prestige cannot receive RaF-granted levels. The shared
proposal/acceptance validator checks persisted in-memory Prestige state in both directions;
a blocked acceptance does not spend the donor's credit. Completed Prestige history alone
is not a restriction, and eligible non-Prestige recipients retain reciprocal grants.
