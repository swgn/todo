# 2024W20 - 2024-05-17 - final day with CFMG

- [ ] handover FATHOM analytics (Jason)

- [ ] ipscape JANUS files, data from ipscape reporting, emailed each morning for previous day activities - handover!

- [ ] Package up AXP comms template change control process.

- [ ] Add logging local to operations/janus or direct to database for load issues/errors

- [ ] CPE process for WISR daily new debts
- [ ] Review WISR reconciliation process, fix!

- [ ] WISR trust payment flags
- [ ] WISR trust payments are being included in adjustx in error!

- [ ] Fix sms for digital operating metrics
- [ ] Fix sms for maria - compliance reporting

- [ ] AXP letters of authority, updated with indebted trading name [Let Ravi know!] +rebrand

- [-] Retention of recordings, AXP want 2y8m years per CHC, we hold for only 2y (Maria, Lex)

  - Chaser email sent to Lex 2024-02-23

---

<details>
<summary>Completed items</summary>

# 2024W20 - 2024-05-16

- [x] ipscape emailed report each day - handover
- [x] Process for raising client data load issues

# 2024W20 - 2024-05-14

- [-] Convert AB file to ZOD
- Date fix to zero seconds & milliseconds `new Date(new Date().setSeconds(0,0)).toISOString()`
- [-] (#wontdo) XML generator for Harish/LPL for garnishees (2024W13)
- [x] Screen recording for adding a new page (shortlink) to website
- [-] (use cxnote instead) Add `cxactivitylog` table to janus
- [-] !! Consolidate file adjustment profiles in CX. Use the ADJUST payment load profile as used for VC.

  - [x] AB adjustment profile updated
  - [-] MP adjustments in janus
    - [-] Move from ETL to janus
  - [x] updated for MADJUST for WISR
  - [-] update for DEBTADJUST_RS

- [-] (delegated) AXP audit - initial request - offboarding - waiting on Lex

- [-] Check placement load profiles - we should be setting `FILODEBTDUE` at initial load, updating only `FILDOD` on subsequent metadata updates
  - [x] VCEA
  - [x] WISR
  - [-] MP
  - [-] RS

# 2024W20 - 2024-05-13

- [-] janus: update AXP ads report, adding liquidation portfolios (email from AI)
- [x] Add secrets into deno-janus, aws and ezidebit
- [-] (delegated) Ravi future of deceased portfolio actioning, Suzie was to discuss .
- [x] Load missing dialler webhooks from 5 May
- [-] (delegated) !!! ipSCAPE issue with ph1 vs ph2 fields, investigate and remedy [wait for next release 2024-03-06]

# 2024W19 - 2024-05-10

- [x] WISR closure process
- [x] Start enforcing ttl for dynamodb campaign table
- [x] Add `deno task pay` to main func for deno, run often/daily
- [x] Add `deno task web` to main func for deno, run often/daily
- [>] (delegated) cx: build new report for WISR for reg notices, using cxactivitylog table based on reg notice activity codes (see 99.VC.009)
- [>] (delegated) Dupe stamping - follow up CJ on 2024-03-08
- [>] (delegated) janus: kept promise rate information for Rustam to build report
- [>] (delegated) janus: spin report for ynna, document process
- [>] (delegated) ipSCAPE - refactor so abandoned calls are not stamped! see filcode 62595, campaign id 65jrf7727noc / leadId 91207 2024-03-11
- [x] WISR - overnight reporting, post-change only need DD reschedule report. Cancel others.
- [-] Deceased email templates, better method for drafting... Review emails sent.
- [-] Add arr_con_au template to mercury (see ref 10041057 as example of send 2024-03-13)
- [x] Add ttl to for dynamodb resolve table
- [-] ~ test out metabase rest API for running reports or accessing data
- [-] ~ client reporting via SFTP automated via either CX run OR metabase API calls?
- [-] ~ settlement tracker spreadsheet by admin should be moved to metabase
- [-] ~ Set own OKRs: review company kpis and set own krs to break down. start scoring progress
- [-] ~ test new metabase server's slack integration (it security issues potentially)
- [-] ~ investigate better way to DO payments in Collexus, pending or unconfirmed would be great. Get confirmed when payment is reconciled or verified (by Finance or client file)
- [x] WISR closure process
- [>] (delegated) relax ID verification for deceased processing (Ravi) Very hard to ID efficiently
- [>] (deletated) merge AWS accounts instances with InDebted
- [-] janus - better handling of duplicate files, log and prevent re/review each load
- [-] janus - create load files in a specific directory (source settings? or output?), bypass metabase
- Daily load process for CXLIVE is flawed because it us batch based, should really compare against last client file rather than against CX info.

  - Issue: if a single file in a batch does not load, the logic to close files flags open CX files that do not exist in latest client file. If latest client file only contains updated error files, all other open files will incorrectly be flagged to closed.
  - Could we compare record against record in latest client batch, treat each entry as an atomic element? If record is received and existed in last file received prior, then update/reconcile. If no record in previous file,
  - Would it simply make more sense to receive a closure report? Client tells us that the file is closed and provide a reason for closing?
  - Possible solution: forget metabase, parse client file and make imports directly. Can use API to check data from Collexus (live data). Can still load full client file into a metabase table, however generation of imports happens in deno, not metabase

- [x] Streaming all the things (implemented in deno-janus)
  - Check out use of JSON LINES
- [-] ISO 27001 programme - merge with InDebted?
- [-] ISO 9001 programme - merge with InDebted?

# 2024W19 - 2024-05-09

- [x] Update LH permissions in GRC, allow access to press Reassess button (Request raised, RSD-893)

# 2024W19 - 2024-05-08

- [x] Add TTL to resolve table in DynamoDB (resolve)
- [x] AXP audit, outlook retention period
- [x] AXP audit, redaction wording - explain delay with collexus redaction

# 2024W18 - 2024-05-03

- [x] Re-enable RESOLVE / event on website..

# 2024W18 - 2024-04-30

- [x] New data spec for Vestone Capital (due 01 May 2024)
- [x] MERC account loading for AXP - raised with Alex

# 2024W18 - 2024-04-29

- [x] AXP audit - initial request - change management tab
- [x] AXP audit - initial request - approval letters tab
- [x] AWS update credit card info - billing failure!!!

# 2024W17 - 2024-04-26

- [x] WISR RECALL file process..

# 2024W17 - 2024-04-23

- [x] WISR reg notice process, finalise today

# 2024W16 - 2024-04-19

- [x] BMS rebrand PDF export..
- [x] AXP Auditors catering for when in office

# 2024W16 - 2024-04-15

- WISR reg notices, process near complete.. added UDF logic to existing queries

# 2024W15 - 2024-04-12

- [x] Load UDF content into Metabase to use in WISR reg notice processing
- [x] Investigate MP load issues...

# 2024W15 - 2024-04-11

- [x] WISR reg notices, reengineer process

# 2024W15 - 2024-04-10

- [x] AXP audit - initial request - attorney involvement - waiting on Lex
- [x] WISR regulatory notices process, work with CM

# 2024W15 - 2024-04-09

- [x] WISR email to JM about business rules for fees, client tacking onto next Direct Debit. How should we collect?
- [-] Get LH access to github to manage email templates? (Azure is where it's at)

# 2024W15 - 2024-04-08

- [x] website: finish v1.0 site +rebrand :tada:

- [-] overlap of policies on indebted.co website (not me) +rebrand
- [x] email template to send to customers (to be sent ?) +rebrand
- [x] sms template to send to customers (to be sent ?) +rebrand
- [x] review non-HTML email templates in Collexus for rebrand +rebrand
- [x] rebrand website for indebted +rebrand

# 2024W14 - 2024-04-05

- don't panic

# 2024W14 - 2024-04-04

- [x] WISR report to show CX files missing from INV (Closure Report)
- [x] Process to close files on WISR Closure Report, CJ to provide cmd to use AWCR

# 2024W14 - 2024-04-03

- [x] WISR reg notice process, understand better!
- [x] Add all email templates to mercury

# 2024W14 - 2024-04-02

- [x] !!! Add enhanced filcode regex to prod website +rebrand
- [x] !!! respond to Ann @ MP re: Reg notices

# 2024W13 - 2024-03-28

- [x] Load daily WISR files...
- [x] [!!!] generic web links for indebted.co redirect
- [x] [!!!] regex for indebted.co website redirect

# 2024W13 - 2024-03-27

- [x] add cname for AWS CF static.indebted.au
- [x] WISR - reconcile balances after FINTXN entries

# 2024W13 - 2024-03-26

- [x] WISR - load new FINTXN entries? +wisr +janus

# 2024W13 - 2024-03-25

- [x] Add LH to service desk on reminda.atlassian.net

# 2024W12 - 2024-03-22

- [x] [!!!] WISR overnight reporting
- [x] WISR - load metadata changes

# 2024W12 - 2024-03-21

- [x] [!!!] WISR inventory load into Collexus (Upload)
  - [x] portfolio code logic
- [x] [!!!] WISR fintxn load into Collexus

# 2024W12 - 2024-03-20

- [x] reminda/indebted letterhead template
- [x] WISR - new resolve page(s): [webpay, eft, bpay] to reminda
- [x] [!!!] WISR resolve pages

# 2024W12 - 2024-03-19

# 2024W12 - 2024-03-18

- [x] janus - delete existing err file if found
- [x] [!!] WISR new financial transactions file - implement load process for janus [2024-03-25]
- [x] [!!] WISR new daily file - implement load process for janus [2024-03-25]
- [x] send WISR load errors to James
- [x] [!!!] WISR email templates, build is broken

# 2024W11 - 2024-03-15

- [x] Work out Github work vs private
- [x] [!!!] Send digital operating metrics for 2024W10

# 2024W11 - 2024-03-14

- [x] cxfile - change format of fillastpayrevdateent to date
- [x] Find hardship templates to send to Dermot

# 2024W11 - 2024-03-11

- [x] [!!!] Fix AB closure report, you amended VC by mistake, should be AB! stupid
- [-] VESTONE reporting - IDEA = Could parse first part of email address and add as a note?

# 2024W10 - 2024-03-08

- [x] [!!!] ABLR closures, what is the logic?
- [x] [!!!] AXP templates for Azra

# 2024W10 - 2024-03-07

- [x] [!!] AXP: complete TSM questionnaire (waiting on IT response)
- [x] Load Harish legal email templates into Collexus
- [-] metabase: dermot add liquidation placement_level via updated ads report

# 2024W10 - 2024-03-06

# 2024W10 - 2024-03-05

- [x] review templates for harish (respond to email in action folder)
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

</details>
