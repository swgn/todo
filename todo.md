## Company KPIs

1. Achieve Revenue of $4,894,534 (Oct '23 - Jun '24).
1. Achieve a Net Profit of $1,050,000 (Oct '23 - Jun '24).
1. Achieve a Revenue Run Rate for FY25 of $7m by Jun '24.
1. Co-Lead the name change of reminda to InDebted by EOM Mar '24 (April 8)
1. Support the design and integration of key support teams to InDebted by EOM Jun '24

## OKR

1. Publish a graph to track revenue day-on-day towards target
1. Publish a graph to track net profit day-on-day towards target
1. Publish a graph to track revenue run rate day-on-day towards target

# Notes

# 2024W14 - 2024-04-02

- Revenue Run Rate: Run Rate = Revenue in Period / # of Days in Period x 365

- [ ] !!! respond to Ann @ MP re: Reg notices

- [ ] Add all email templates to mercury

- [ ] $ book dental appointment
- [ ] $ book other appointment

- [ ] WISR regulatory notices process, work with CM
- [ ] WISR reg notice process, understand better!

- [ ] XML generator for Harish/LPL for garnishees (2024W13)

- [ ] ipSCAPE issue with ph1 vs ph2 fields, investigate and remedy [wait for next release 2024-03-06] !!!

- [ ] list of AXP comms templates 1 Oct to 31 Mar (due 2024-03-22)

- [ ] Set own OKRs: review company kpis and set own krs to break down. start scoring progress

- janus - better handling of duplicate files, log and prevent re/review each load
- janus - create load files in a specific directory (source settings? or output?), bypass metabase

- [ ] #rebrand - review non-HTML email templates in Collexus for rebrand
- [ ] #rebrand - website: finish v1.0 site
- [ ] #rebrand - rebrand website for indebted
- [ ] #rebrand - email template to send to customers (to be sent ?)
- [ ] #rebrand - sms template to send to customers (to be sent ?)
- [ ] #rebrand - AXP letters of authority, updated with indebted trading name [Let Ravi know!]
- [ ] #rebrand - overlap of policies on indebted.co website

- [ ] Add `cxactivitylog` table to janus
- [ ] Update LH permissions in GRC, allow access to press Reassess button

- [ ] [!!] Consolidate file adjustment profiles in CX. Use the ADJUST payment load profile as used for VC.

  - [x] AB adjustment profile updated
  - [ ] MP adjustments in janus
    - [ ] Move from ETL to janus
  - [x] updated for MADJUST for WISR
  - [ ] update for DEBTADJUST_RS

- [ ] ipSCAPE - refactor so abandoned calls are not stamped! see filcode 62595, campaign id 65jrf7727noc / leadId 91207 2024-03-11

- [ ] WISR - overnight reporting, post-change only need DD reschedule report. Cancel others.

- [ ] Get LH access to github to manage email templates?
- [ ] LH access to publish docs in Confluence

- [ ] janus: update AXP ads report, adding liquidation portfolios (email from AI)
- [ ] janus: kept promise rate information for Rustam to build report
- [ ] janus: spin report for ynna, document process

- [ ] cx: build new report for WISR for reg notices, using cxactivitylog table based on reg notice activity codes (see 99.VC.009)

- [ ] Dupe stamping - follow up CJ on 2024-03-08

- [ ] ISO 27001 programme - merge with InDebted?
- [ ] ISO 9001 programme - merge with InDebted?

- [ ] implement automatic sweep of overnight files to client sftp directories

  - [ ] Vestone
  - [ ] AB
  - [ ] Wisr

- [ ] Check placement load profiles - we should be setting `FILODEBTDUE` at initial load, updating only `FILDOD` on subsequent metadata updates

  - [x] VCEA
  - [ ] WISR:WREA
  - [ ] WISR
  - [ ] MP
  - [ ] RS

- [ ] Retention of recordings, AXP want 2y8m years per CHC, we hold for only 2y (Maria, Lex)

  - Chaser email sent to Lex 2024-02-23

- [ ] Add ttl to for dynamodb resolve table
- [ ] Start enforcing ttl for dynamodb campaign table

- [ ] Add arr_con_au template to mercury (see ref 10041057 as example of send 2024-03-13)

- Daily load process for CXLIVE is flawed because it us batch based, should really compare against last client file rather than against CX info.

  - Issue: if a single file in a batch does not load, the logic to close files flags open CX files that do not exist in latest client file. If latest client file only contains updated error files, all other open files will incorrectly be flagged to closed.
  - Could we compare record against record in latest client batch, treat each entry as an atomic element? If record is received and existed in last file received prior, then update/reconcile. If no record in previous file,
  - Would it simply make more sense to receive a closure report? Client tells us that the file is closed and provide a reason for closing?
  - Possible solution: forget metabase, parse client file and make imports directly. Can use API to check data from Collexus (live data). Can still load full client file into a metabase table, however generation of imports happens in deno, not metabase
  - Streaming all the things
  - Check out use of JSON LINES

- [ ] ~ test new metabase server's slack integration (it security issues potentially)
- [ ] ~ investigate better way to DO payments in Collexus, pending or unconfirmed would be great. Get confirmed when payment is reconciled or verified (by Finance or client file)
- [ ] ~ relax ID verification for deceased processing (Ravi) Very hard to ID efficiently

- [ ] ~ test out metabase rest API for running reports or accessing data

- [ ] ~ client reporting via SFTP automated via either CX run OR metabase API calls?

- [ ] ~ merge AWS accounts instances with InDebted

- [ ] ~ settlement tracker spreadsheet by admin should be moved to metabase

<details>
<summary>Completed items</summary>

# 2024W14 - 2024-04-02

# 2024W13 - 2024-03-28

- [x] Load daily WISR files...
- [x] [!!!] generic web links for indebted.co redirect
- [x] [!!!] regex for indebted.co website redirect

# 2024W13 - 2024-03-27

- [x] add cname for AWS CF static.indebted.au
- [x] WISR - reconcile balances after FINTXN entries

# 2024W13 - 2024-03-26

- [x] WISR - load new FINTXN entries?

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
