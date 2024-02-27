# 2024-02-27

- [] $ book dental appointment

- [] !!! Plug dialler stamping gap between 14 Feb PM and 19 Feb
- [] !!! ipSCAPE issue with ph1 vs ph2 fields, investigate and remedy
- [] !! ipSCAPE stamping duplicates, ask CJ to fix with Collexus

- [] review templates for harish, email in action folder

- [] Check-in with Ravi workload on DC portfolio

- [] AXP letters of authority, updated with indebted trading name [Let Ravi know!]

- VESTONE reporting - IDEA = Could parse first part of email address and add as a note?

- [] implement automatic sweep of overnight files to client sftp directories
  - [] Vestone
  - [] AB
  - [] Wisr? needed?

- [] close down netlify account
- [] tell finance the netlify is closed down, do not expect bills

- [] ask about induction program for indebted, how much time expected?

- [] metabase - kept promise rate information for Rustam to build report
- [] metabase - spin report for ynna, document process

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
- [] ~ Review caro process for generating regulatory notices for WISR
- [] ~ investigate better way to DO payments in Collexus, pending or unconfirmed would be great. Get confirmed when payment is reconciled or verified (by Finance or client file)
- [] ~ relax ID verification for deceased processing (Ravi) Very hard to ID efficiently

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