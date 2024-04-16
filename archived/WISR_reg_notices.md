# SECTION 88

- [NCCP Act](https://classic.austlii.edu.au/au/legis/cth/consol_act/nccpa2009377/)
- [s88 of the National Credit Code (Schedule 1 of the NCCP Act](https://www8.austlii.edu.au/cgi-bin/viewdoc/au/legis/cth/consol_act/nccpa2009377/sch1.html#_Toc155788863)

# PRIVACY NOTICES

- [Privacy Act 1988, Section 6Q](https://www5.austlii.edu.au/au/legis/cth/consol_act/pa1988108/s6q.html)
- [Privacy Act 1988, Section 21D](https://www5.austlii.edu.au/au/legis/cth/consol_act/pa1988108/s21d.html)

## 6Q Notice

- Can be combined with s88 notice
- Amount in arrears under the credit contract must exceed $150

Paragraph 9.3 expands the notice requirements:

- the CP must issue the Section 6Q notice and the Section 21D(3)(d) notice separately;
- the CP must issue the Section 6Q notice before the Section 21D(3)(d) notice;
- the CP must not issue the Section 21D(3)(d) notice less than 30 days after the issue of the Section 6Q notice;
- the CP must issue the Section 6Q notice and Section 21D(3)(d) notice by sending them to the individual's last known address at the time of despatch;
- the amount that is disclosed by the CP to the CRB as the amount that is overdue must have been overdue for at least 60 days and not be more than the amount specified in the Section 21D(3) notice, plus adjustments for interest, fees and other amounts, less any part payments prior to the date of disclosure by the CP to the CRB.
- the default information must not be disclosed by the CP to the CRB:
  - earlier than 14 days after the date on which the Section 21D(3) notice is issued by the CP to the
    individual; or
  - later than 3 months after that date; and
- the CP must meet the other requirements relating to default information that are set out in Part IIIA, the Regulations and this CR code.

Questions:

- Has a S88/6Q been issued?
- Has 30 days elapsed since S88/6Q was issued?

## Logic - New Files

- If [new debt uploaded] and [client dpd > 24]: issue S88 notice (regardless of PORCODE)

- If [debt = secured] and [balance > $10,000] and [days since S88 issuance > 34]: issue ITR notice
- If [debt = secured] and [balance between $151 and $10,000] and [days since S88 issuance > 34]: issue 6Q notice
- If [debt = secured] and ([days since ITR issuance> 34] OR [days since 6Q notice > 34]) and [client dpd > 94]: issue 21D notice AND move file to WISA porcode AND update outstanding balance = loan balance
- If [debt = unsecured] and [days since s88 issuance > 34] and [balance > $150]: issue 6Q notice
- If [debt = unsecured] and [days since 6Q issuance > 34]: issue 21D notice
- If [debt = secured] and [days since 6Q notice > 34] and [client dpd > 94]: issue 21D notice AND move file to WIUA porcode AND update outstanding balance = loan balance

## Logic - Old Files

- 
- How do we detect when a notice has been sent?
