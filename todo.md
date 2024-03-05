# 2024W10 - 2024-03-06

- [] $ book dental appointment
- [] $ book other appointment

- [] [!!!] ipSCAPE issue with ph1 vs ph2 fields, investigate and remedy [wait for next release 2024-03-06]
- [] [!!] AXP: complete TSM questionnaire (waiting on IT response)

- [] Dupe stamping - follow up CJ on 2024-03-08

- [] website: finish v1.0 site
- [] rebrand: rebrand website for indebted

- [] metabase: dermot add liquidation placement_level via updated ads report
- [] metabase: kept promise rate information for Rustam to build report
- [] metabase: spin report for ynna, document process

- [] rebrand email template to send to customers (to be sent 2024-03-11)
- [] rebrand sms template to send to customers (to be sent 2024-03-11)

- [] cx: build new report for WISR for reg notices, using cxactivitylog table based on reg notice activity codes (see 99.VC.009)

- [] review templates for harish (respond to email in action folder)

- [] AXP letters of authority, updated with indebted trading name [Let Ravi know!]

- VESTONE reporting - IDEA = Could parse first part of email address and add as a note?

- [] implement automatic sweep of overnight files to client sftp directories
  - [] Vestone
  - [] AB
  - [] Wisr


- [] review non-HTML email templates in Collexus for rebrand

- [] Check placement load profiles - we should be setting `FILODEBTDUE` at initial load, updating only `FILDOD` on subsequent metadata updates
  - [x] VCEA 
  - [] WISR:WREA
  - [] WISR
  - [] MP
  - [] RS

- [] Retention of recordings, AXP want 2y8m years per CHC, we hold for only 2y (Maria, Lex) 
  - Chaser email sent to Lex 2024-02-23

- [] Add ttl to for dynamodb resolve table
- [] Start enforcing ttl for dynamodb campaign table

- [] Daily load process for CXLIVE is flawed because it us batch based, should really compare against last client file rather than against CX info. 
  - Issue: if a single file in a batch does not load, the logic to close files flags open CX files that do not exist in latest client file. If latest client file only contains updated error files, all other open files will incorrectly be flagged to closed.
  - Could we compare record against record in latest client batch, treat each entry as an atomic element? If record is received and existed in last file received prior, then update/reconcile. If no record in previous file, 
  - Would it simply make more sense to receive a closure report? Client tells us that the file is closed and provide a reason for closing?
  - Possible solution: forget metabase, parse client file and make imports directly. Can use API to check data from Collexus (live data). Can still load full client file into a metabase table, however generation of imports happens in deno, not metabase
  - Streaming all the things
  - Check out use of JSON LINES

- [] ~ test new metabase server's slack integration
- [] ~ Review Caro process for generating regulatory notices for WISR
- [] ~ investigate better way to DO payments in Collexus, pending or unconfirmed would be great. Get confirmed when payment is reconciled or verified (by Finance or client file)
- [] ~ relax ID verification for deceased processing (Ravi) Very hard to ID efficiently

- [] ~ merge AWS accounts instances with InDebted

# 2024W10 - 2024-03-05

- [x] add porcode filter to metabase report https://metabase.corp.cfmg.com.au/question/1109
- [x] Add cname for static.indebted.au, same as static.reminda.com (S3 assets)
- [x] [!!] ipSCAPE stamping duplicates, ask CJ to fix with Collexus
- [x] [!] Fix VC PTP website emails sent back, references "WISR" incorrectly (code reminda.com)

# 2024W10 - 2024-03-04

- [x] [!!] review new NBN templates for CJ
- [x] [!!!] Plug dialler stamping gap between 14 Feb PM and 19 Feb
- [x] vestone activities report - add placement date?
- [x] tell finance the netlify is closed down, do not expect bills
- [x] downgrade netlify account to free tier
- [x] create vscode snippet to add date tags for this file!
- [x] generate and send updated VC activities report to DROSE, respond to email
- [x] Check-in with Ravi workload on DC portfolio

# 2024W09 - 2024-03-01

- [x] send list of AXP hardship templates to Dermot to forward to Azra
- [x] send slack note, cancel team day on 4 Mar for the time being
- [x] respond to AXP audit date confirmation email (Val)

# 2024W09 - 2024-02-29

- [x] ask about induction program for indebted, how much time expected?

# 2024-02-28

- !! [x] send weekly DOM to AXP ~ week 8 stats
- [x] requested a report from ipscape to provide missing data between 14 Feb and 21 Feb
- [x] Respond to JM@WISR email, advise happy to test from 4 Mar
- [x] metabase: dermot reporting broken report, recoveries mom

# 2024-02-27

- [x] !!! Reg notice file format for WISR
- [x] VCEA - Create overnight to show OB customer contacts (sms, email, call) `99.VC.009`
- [x] VCEA - run report showing all activities since go-live
- [x] find and send AWS invoice for Jan to finance
- [x] find policy for policy review cycle, send to azra
- [x] investigate fix issue with ABEA files not being closed after customer action
- [x] create overnight closure report for ABEA
- [x] create overnight closure report for VCEA
- [x] chat with LEX about moving AXP liquidation into Legal CX groups, lockdown
- [x] !!! move reminda.com GH repo to indebted
- [-] test out new metabase server (migrated before I could test)

# 2024-02-26

- [x] Email Sian to request moving LPL privacy policy to be a new page on lintonpitt.com.au (currently points to cfmg.com.au)
- $ new desk top received, waiting for desk frame and legs, should be delivered in next few days
- [x] add CNAME entry to point indebted.au to netlify deployment of reminda.com
- [x] Send call recording to customer (Maria) Ref 10045215

# 2024-02-24

- [x] send IT request to add rules for contingent mailbox to sweep reminda.co emails into archive
- [x] request use of `indebted.au` in netlify from pierre and team
- [x] azra request for policies
- [x] $ chase up desk #14740; dispatched today via ARAMAX
- [x] update invite for team day on monday
- [x] approve pending leave in employmenthero
- [x] investigate updating slack channel when new data loaded into metabase
  - Needs slack integration added to metabase. Waiting.
- [x] !!! Confirm team day for Monday COVID etc
- [x] !!! Send inventory file spec to WISR
- [x] process VC daily file and record loom
- [x] handover VC daily process to Caro