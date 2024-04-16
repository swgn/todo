:alert: Urgent Attention Required - Data & System Issues :alert:
Hi team, the following issues flagged require immediate attention and resources allocated to resolving. These can impact revenue, compliance and client relationships. After these are resolved I will post a list of secondary, less pressing issues needing to be resolved.
Requests:
@Chris B
/
@Jacques
/
@Rustam
/
@Lex

- let's divide and conquer here :teamwork: - please respond asap with which items you can take on and have resolved before COB Monday.
  @CJ Dalby
  please be available to buddy up on these on the below issues with
  @Chris B
  /
  @Rustam
  /
  @Jacques
  /
  @Lex
  for the purpose of assisting with which data points and business logic needs to be used per process, per client agreement, etc.
  @Jacques
- we need Collexus access for
  @Mara E
  asap so she can jump in to assist with validation for each of the below.

# ISSUE #1 - URGENT: WISR Balances & Payments

Description:

- Wisr payments doubling up - claiming double comms in some circumstances
- Some payments reported by client were just missing completely therefore incorrect balances.
- We've received a trust payment, then a direct to client (DC) payment or client direct debit (DD) issue has also been applied.
  All client reported fees getting added to arrears files, are remaining outstanding, no understanding if this is with us or client to fix. All of these accounts are now under a HOLD status.

## What is required:

- A review of all trust payments made directly to InDebted. Reversals of the direct to client payments needs to be completed.
- Resource required to step in an rectify the issue. (Lex?)
- Gain an understanding from the client if we are to pursue these fees or not. If so take these accounts off HOLD and get them back to the collectors.
- Have been advised the wrong logic which caused payments missing being allocated was fixed however no confirmation to the Customer team if this has been validated / is working?
- Customer team have been advised that each day the data is run through Metabase that a recon is done at the same time balance matching everything to the client daily. Not sure if this has been validated? Need confirmation.
- A resource needs to validate the loader/processor for Wisr. @Mara E
  Once complete - needs 2nd person validation from client data > what we have done on collexus

# ISSUE #2 - URGENT: Regulatory notices are not being sent on Wisr accounts

## Description:

This effects balances being accelerated as agreed, accounts aren't being escalated and largest risk is the secured space is hugely impacted by this. This will continue to impact revenue for the next quarter minimum.

Due to above regulatory notices not going, balances aren't accelerating, we can't do any repossessions that would now be overdue. This will effect our revenue and the progression of these files. (Secured files made up, on average, to nearly 50% of previous months performance)

This has been meaning to get done since 21/03/2024 when we went live with the new Wisr changes.

All old files are currently in a full collections CEASE because of this. Unsure if client has been made aware of both cease and no reg notices on old or new or balance accelerations.

Regulatory notice meta report is in draft mode - previous known logics ignored & yet to be completed - sitting with Lex today to try and fix - pulling wrong accounts- report here: https://metabase.corp.cfmg.com.au/collection/174-wisr-notices
Examples:
Under Send S88 the meta report it has picked up accounts that are;
Accounts with LPL
Under quarantine
Under hardship
Already default listed
Awaiting client instructions
Awaiting recall from client
ITR already been sent
What is required:
@Deb
to inform the client, and attempt to buy us at least 1.5 weeks to rectify.
A resource to understand ALL logics and create the reporting taking all previously agreed upon logics into account. CJ to be involved in this process.
@Mara E
: Once complete - needs 2nd person validation from our data > intended logic > what we have done on collexus.

# ISSUE #3 - URGENT: Dialer Stamping

## Description:

- Hundreds of attempted no answered calls that didn't connect to agents are missing from AMEX & CXLIVE files. More evident in Vestone with roughly ~30% at least of their calls missing. Amex/CXlive maybe 5%-10% are missing. This has been traced back to go live of ipscape.
- Tickets have been raised previously with ipscape in regards to api, webhooks - due to no response from us tickets with iPscape were closed - issues still outstanding.
- There was also previous concerns raised that we may not be able to retrieve this data to fix retrospectively
  Due to above Vestone Capital have made complaints :
- Haven't been able to charge VC for the missing stamped calls above because they aren't on the files. Due to this, VC is then think we aren't fulfilling our duties and are raising questions to Debbie + Lex.
- Side Note : Demo which handles stamping dialers is a constant issue, some days it works others it doesn't. Customer team use deno-stamp which was created, however breaks quite easily.

## What is required:

- Lex is going back to Vestone about their concerns.
- Book meeting with IPSCAPE for Lex , Chris CJ & Amor on missing outcomes from IPSCAPE exports
- Deno : A resource needs to build us a stamping processes that we can trust and has been tested. @Mara E
- Once complete - needs 2nd person validation from our ipscape call data > what we have done on collexus

# ISSUE #4 - Urgent: Resolve Page enquiries not allocating to all files

## Description:

- Resolve forms including direct debit requests and call backs, arrs etc since rebrand is not getting allocated correctly. Some are some are not.
- Certain references aren't picking up the new 'C' being in front of the 6 digit reference and certain old files are coming through into emails with C but the file has no C therefore not allocating.
- Therefore in some cases Client isn't getting notified about the DD & CB & ARR requests coming through from the customer in the overnight reporting therefore client is also missing out on revenue.
- Side note: Separate issue that may need devs - if customer has an old account that got emails with links , and they service via that - its going onto the old file - and therefore may not be getting reported back to client / actioned.

## What is required:

A resource needs to look into this to see why this is happening and a solution in the interim needs to be put into place to ensure the portal that are coming through now are somehow getting sent to the client to let them know about the request.
@Mara E
: Once complete - needs 2nd person validation from incoming resolve forms > what we have done on collexus
@Mara E

# ISSUE #5 - Urgent: Monday Place data

## Description:

The same day payments are being applied and decreasing the balance, there is an immediate adjustment increasing the balance back up.
Back on 04/04/2024 an email was sent to the client advising them that we think there is something wrong with the data.
Client came back said it was fine. Hour or so late client said data was wrong. Raised with
@Chris B
.
Unsure if this bad data that was loaded into our system was fixed? Need to confirm?

## What is required:

A resource needs to see if our data has ben reconciled & need to investigate the payments being adjusted back up rather than reversed? Then full re-con to be confirmed
@Mara E
: Once complete - needs 2nd person validation from incoming client data > what we have done on collexus
