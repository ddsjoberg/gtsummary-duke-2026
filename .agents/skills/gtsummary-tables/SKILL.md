---
name: gtsummary-tables
description: Build summary tables in R with gtsummary and cards. Use
  whenever the user asks for a summary / demographics / AE table or a
  "Table 1".
---

# Summary tables

Setup: load tidyverse, gtsummary, cards; prep data with tidyverse.

## Priority order
1. set the group's theme right after loading packages, e.g.
   theme_gtsummary_journal("jama")
2. {gtsummary} tbl_*() (tbl_summary(), tbl_hierarchical())
3. complex/custom -> ARD-first: cards::ard_stack() / cardx::ard_*()
   -> tbl_ard_*()
4. last resort -> build the ARD, then as_gtsummary()

Never use gtsummary::tbl_custom_summary(): it is not ARD-based.

Always gather_ard() the result for QC.
