This repository contains statistics aggregated from public online data (`data.csv`) on the NSERC PGS/CGS-D program, the flagship doctoral scholarship program in Canada. Each row represents the statistics for a given year, ranging from 2003-2022. Note that 2022 represents the 2021-2022 application cycle, with awards starting in 2022. The CGS-D is valued at $35,000 each year, and awarded to the most highly ranked applicants, while the PGS-D is valued at $21,000 and is awarded to the subsequently ranked applicants The award values, as of April 2023, have not changed in 20 years.

### Brief Background

The NSERC PGS/CGS-D is a PhD level scholarship awarded by the Natural Sciences and Engineering Research Council of Canada (NSERC), in conjunction with their social science (SSHRC) and health science (CIHR) counterparts. Most applications are made through the institution at which the award will be held (<https://www.nserc-crsng.gc.ca/_doc/Students-Etudiants/CGSDFlowchart_e.pdf>). Each institution reviews the application and forwards a certain number of applications to the national level, according to the quota (<https://www.nserc-crsng.gc.ca/Students-Etudiants/PG-CS/quota-quota_eng.asp>). Applications are then adjuciated at the national level, where each applicant is given a ranking. In 2022, the success rate for a CGS-D for forwarded applications was 330/1721 (~top 19.2%) and the success rate for a PGS-D was 387/1721 (~the next 22.5%). The CGS-D must be held at a Canadian institution, while the PGS-D can be held at a foreign institution. Applicants who would have received a CGS-D but wish to attend a foreign institution may choose to receive a PGS-D instead. 


A full description of the NSERC CGS-D award can be found at the following link: <https://www.nserc-crsng.gc.ca/students-etudiants/pg-cs/cgsd-bescd_eng.asp>. Below is an excerpt from the link above:

The objective of the Canada Graduate Scholarships – Doctoral (CGS D) program is to promote continued excellence in Canadian research by rewarding and retaining high-calibre doctoral students at Canadian institutions. By providing support for a high-quality research training experience to awardees, the CGS D program strives to foster impacts within and beyond the research environment.


### Selected descriptions of variables

- `ApplicationsFwd`: # of applications forwarded to NSERC. Alternative wordings include "eligible applications", "applications received". At least more recently, this number in large part represents the number of applications that are deemed meritorious at the university level, before being forwarded to NSERC. This number should not be interpreted as representative of the # of applications made to the university, as university has a specific quota number of applications which they are permitted to forward. A smaller portion of `ApplicationsFwd` are those made directly to NSERC, of which I believe there is no quota. It is possible that direct applications made up a larger proportion in the past.

- `UBCPhDDomestic`, `UBCPhDIntl`: Number of enrolled domestic and international PhD students at UBC. The number of domestic students can be seen as a (biased) proxy of how many potential applicants there are to the PGS/CGS programs.

- `AwardValuepApplicant`, `AwardValuepEnrolled`: Award value normalized per number of applications forwarded, and per enrolled domestic students, respectively. 

- `CPIFactor2022`: Inflation factor computed using the raw CPI in April of each year, using 2022 as a reference. For example, the CPI in April 2003 was 102.4, and the CPI in April 2022 was 149.8, and the inflation factor is calculated as 149.8/102.4 $\approx$ 1.46. Interpret as $100 in 2003 is equivalent in purchasing power to $146 today. 

### Sources:

- Number of applications and awards are retrieved from the following links (replacing Year = `Year`): <https://www.nserc-crsng.gc.ca/NSERC-CRSNG/FundingDecisions-DecisionsFinancement/ScholarshipsAndFellowships-ConcoursDeBourses/index_eng.asp?Year=2021> for the years 2008-2022.

- For the years 2003-2007, the data are retrieved from tables in <https://circum.com/index.cgi?en:doc:T081>, exhibit 2.4 and 2.5.

- CPI factors are obtained from the Bank of Canada, series V41690973, <https://www.bankofcanada.ca/rates/price-indexes/cpi/>. 

- UBC enrolment info are obtained from <https://www.grad.ubc.ca/about-us/graduate-education-analysis-research/enrolment-demographics>. 