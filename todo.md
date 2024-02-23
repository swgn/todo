# 2024-02-24


- [] metabase - kept promise rate information for Rustam to build report
- [] metabase - spin report for ynna

- [] request use of `indebted.au` in netlify from pierre and team
  - [] add CNAME entry to point indebted.au to netlify deployment

- [] Check placement load profiles - we should be setting `FILODEBTDUE` at initial load, updating only `FILDOD` on subsequent metadata updates
  - [x] VCEA 
  - [] WISR:WREA
  - [] WISR
  - [] MP
  - [] RS
- [] Delegate ipscape stamp duplications to CJ
- [] Retention of recordings, AXP want 2y8m years per CHC, we hold for only 2y (Maria, Lex) 
  - Chaser email sent to Lex 2024-02-23
- [] Send call recording to customer (Maria)

- [] Add ttl to for dynamodb resolve table
- [] Start enforcing ttl for dynamodb campaign table

- [] Daily load process for CXLIVE is flawed because it us batch based, should really compare against last client file rather than against CX info. 
  - Issue: if a single file in a batch does not load, the logic to close files flags open CX files that do not exist in latest client file. If latest client file only contains updated error files, all other open files will incorrectly be flagged to closed.
- [] ~ investigate better way to DO payments, pending or unconfirmed would be great. Get confirmed when payment is reconciled or verified (by Finance or client file)
- [] ~ relax ID verification for deceased processing (Ravi)

- [x] chase up desk #14740; dispatched today via ARAMAX
- [x] update invite for team day on monday
- [x] approve pending leave in employmenthero
- [x] investigate updating slack channel when new data loaded into metabase
  - Needs slack integration added to metabase. Waiting.
- [x] !!! Confirm team day for Monday COVID etc
- [x] !!! Send inventory file spec to WISR
- [x] process VC daily file and record loom
- [x] handover VC daily process to Caro