# Terms and definitions

## Data

Any participant records held by the MCEC ranging from email responses to survey responses.

### De-identified data

The U.S. Department of Education defines [de-identified data](https://studentprivacy.ed.gov/glossary#de-identified-data) as:

```
[...] records that have a re-identification code and have enough personally identifiable information removed or obscured so that the remaining information does not identify an individual and there is no reasonable basis to believe that the information can be used to identify an individual. The re-identification code may allow the recipient to match information received from the same source.

For more information, see the [SLDS Technical Brief: Basic Concepts and Definitions for Privacy and Confidentiality in Student Education Records](https://nces.ed.gov/pubs2011/2011601.pdf).
```

#### Re-identification code

"A re-identification code enables an authorized researcher to return to the source of de-identified data and match the de-identified data to the source records.

For more information, see the SLDS Technical Brief: Basic Concepts and Definitions for Privacy and Confidentiality in Student Education Records." [Glossary, Protecting Student Privacy, 2021/02/07](https://studentprivacy.ed.gov/glossary#glossary-node-239)

To learn more about the codes (keys) used by re-data, please refer to the [MCEC Keys (codes) document](MCEC-keys-codes.md).

### Anonymized data

"Anonymization takes the data one step beyond de-identification. That is, anonymized data are data that have been de-identified, and they do not include a re-identification code. In an anonymized data file, the student case numbers in the data records cannot be linked back to the original student record system. Returning to the examples discussed above, anonymized data would not be useful to staff using data to monitor the progress and performance of individual students. However, if a professor at a university reads the research report from the analysis of academic gains of students in the afterschool enrichment program and decides that he or she would like to have a class of graduate students apply different analytic procedures to see if the results can be replicated, an anonymized file could be produced from the de-identified file used by the researchers to serve this purpose. To do this, the re-identification code must be removed and the file should be reviewed to ensure that additional statistical disclosure techniques do not need to be applied. The documentation for the anonymized data file should identify any disclosure limitation techniques that were applied and their implications for the analysis." ([Seastrom, 2010, p. 6](https://nces.ed.gov/pubsearch/pubsinfo.asp?pubid=2011601))

### Methods of data de-identification

The MCEC Project uses two methods of de-identification: redaction and suppression. In our project, protected information is redacted by taking any direct or indirect identifier defined in [HIPAA](docs/HIPAA-tags.md) or [FERPA](docs/MCEC-specific-tags.md) and replacing them with a tag. On the other hand, suppression is the entire removal of a section, phrase or paragraph in which only a single tag [[suppressed-info]] is used to replace that content. For more formal definitions of these two methods, we refer the reader to the official FERPA documentation: [Data De-identification: An Overview of Basic Terms](https://studentprivacy.ed.gov/sites/default/files/resource_document/file/data_deidentification_terms_0.pdf).

#### Redaction of data

"Redaction is a general term describing the process of expunging sensitive data from the records prior to disclosure in a way that meets established disclosure equirements applicable to the specific data disclosure occurrence (e.g., removing or obscuring PII from published reports to meet federal, state, and local privacy laws as well as organizational data disclosure policies). (See disclosure limitation method for more information about specific techniques that can be used for data redaction.)" ([Data De-identification: An Overview of Basic Terms, p. 5](https://studentprivacy.ed.gov/sites/default/files/resource_document/file/data_deidentification_terms_0.pdf))

#### Suppression of data

"Suppression is a disclosure limitation method which involves removing data (e.g., from a cell or a row in a table) to prevent the identification of individuals in small groups or those with unique characteristics. This method may often result in very little data being produced for small populations, and it usually requires additional suppression of non-sensitive data to ensure adequate protection of PII (e.g., complementary suppression of one or more non-sensitive cells in a table so that the values of the suppressed cells may not be calculated by subtracting the reported values from the row and column totals). Correct application of this technique generally ensures low risk of disclosure; however, it can be difficult to perform properly because of the necessary calculations (especially for large multi-dimensional tables). Further, if additional data are available elsewhere (e.g., total student counts are reported), the suppressed data may be re-calculated." ([Data De-identification: An Overview of Basic Terms, pp. 5-6](https://studentprivacy.ed.gov/sites/default/files/resource_document/file/data_deidentification_terms_0.pdf))

#### Safe Harbor Method

"According to the Privacy Rule of the Health Insurance Portability and Accountability Act (HIPAA), the de-identification process can be accomplished using two separate pathways: Safe Harbor method and Expert Determination approach [...] The Safe Harbor method requires all 18 personal identifiers to be eliminated." [Modes of De-identification](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC5977668/)

The Safe Harbor method outlines a set of identifiers to be stripped from any publicly available information. These identifiers are linked with "the individual or of relatives, employers, or household members of the individual" ([U.S. Department of Health & Human Services](https://www.hhs.gov/hipaa/for-professionals/privacy/special-topics/de-identification/index.html#safeharborguidance), 2021/01/31). We have expanded these identifiers to include data specific to our needs. For instance, the Safe Harbor "A" identifier category (Names) has been expanded [here](docs/HIPAA-tags.md) to include hypocorisms, which are relatively frequent in academic emails.

### Modes of data de-identification

According to [(Kayaalp, 2017)](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC5977668/), there are eight different modes of medical data de-identification:

```
A.	Repository-wide batch de-identification
B.	On-demand cohort-specific de-identification
C.	On-demand de-identification of query results
D.	De-identification with patient and provider identifiers
E.	Scientist involved de-identification
F.	Patient involved de-identification
G.	Physician involved de-identification
H.	Online de-identification by honest brokers
```

Although the MCEC Project does not collect medical records, we use this categorization to our own research. Thus, the mode of de-identification used by the MCEC is the Repository-wide batch de-identification mode, which is defined as follows:

"When institutions obtain a de-identification system, some may immediately create a de-identified version of their entire repository, so that researchers with proper credentials can quickly access what they need in a de-identified format." [(Kayaalp, 2017)](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC5977668/)

## Human Subjects Protection Program (HSPP) and Institutional Review Boards (IRBs)

"The Human Subjects Protection Program (HSPP), as the administrative and regulatory support program to the Institutional Review Boards (IRBs), works in collaboration with the research community to maintain an ethical and compliant research program. The IRBs are the independent review committee charged with the protection of human research subjects. An IRB must review all research and related activities involving human subjects conducted at the University of Arizona or by in which the University is a responsible participant. The University of Arizona HSPP has been accredited by the Association for Accreditation of Human Research Protection Programs (AAHRPP) since 2005, strong evidence of our commitment to the protection of human research subjects."[Human Subjects Protection Program, HSPP, 2021/02/07](https://rgw.arizona.edu/compliance/human-subjects-protection-program)

### Data collection

The MCEC Team collects data under the following IRB protocol information:

```
Date: April 28, 2020
Principal Investigator: Damian Yukio Romero Diaz
Protocol Number: 2004533142
Protocol Title: Collection and Analysis of Authentic College Emails
```

Because academic [emails are considered as educational records](https://www.registrar.arizona.edu/personal-information/family-educational-rights-and-privacy-act-1974-ferpa?topic=ferpa):

"Written permission from the student is required to access non-directory information. In limited circumstances, the IRB may waive the requirement to obtain written permission from the student found here. To obtain a waiver to access FERPA information, the investigator must include protocol-specific justification for why access to the FERPA information is needed without written approval from the student. This request must be submitted to the IRB for review and approval."[Access to Records, HSPP, 2021/01/07](https://rgw.arizona.edu/sites/default/files/access_to_records_v2020-03.pdf)

The MCEC requests participants for their [informed consent](https://rgw.arizona.edu/compliance/human-subjects-protection-program/HSPP-forms/consent-templates) before collecting any student or instructors data.

### Undue influence or coercion

Some of our PIs currently attend, or have worked as Graduate Teaching Assistants in some of the departments where data is being collected. This means that there are some ethical concerns regarding the influence that a MCEC Team member may have during the recruitment process. This is true for courses where the recruiting research members are a part of (such has a graduate class where recruitment may happen) or when the recruiting researcher is the instructor of a class (TA, grader, or main instructor).

For these cases, the MCEC assigns the recruitment task to a PI that is not part of the class in question. The Human Subjects Protection Guidelines guidance on this matter is reproduced below:

"Student artifacts and other educational records cannot be accessed until after final grades are posted if any project personnel also has access to student grades. In addition, these project personnel cannot be involved in recruitment, consenting, or identifiable data collection or analysis of his/her students as to avoid the potential for undue influence or coercion. In this instance, a third party not affiliated with the study would need to be responsible for recruiting and consenting students as well as collecting identifiable data, including educational records, and hold those items until final grades are posted. This person will need to be the point of contact for the student to request withdraw from the study, if they wish to do so prior to posting of final grades. However, if the project personnel/instructor wishes to analyze data in real time, the third party can de-identify the data and share it with the project personnel/instructor."[Access to Records, HSPP, 2021/01/07](https://rgw.arizona.edu/sites/default/files/access_to_records_v2020-03.pdf)

## Identifiers

### Direct identifiers

"Direct identifiers include information that relates specifically to an individual such as the individual’s residence, including for example, name, address, Social Security Number or other identifying number or code, telephone number, e-mail address, or biometric record. See also Indirect Identifier.

For more information, see the [SLDS Technical Brief: Basic Concepts and Definitions for Privacy and Confidentiality in Student Education Records](http://nces.ed.gov/pubsearch/pubsinfo.asp?pubid=2011601)."[Glossary, Protecting Student Privacy, 2021/02/07](https://studentprivacy.ed.gov/glossary#header-for-D)

### Indirect identifier

"Indirect identifiers include information that can be combined with other information to identify specific individuals, including, for example, a combination of gender, birth date, geographic indicator and other descriptors. Other examples of indirect identifiers include place of birth, race, religion, weight, activities, employment information, medical information, education information, and financial information. See also Direct Identifier.

For more information, see the [SLDS Technical Brief: Basic Concepts and Definitions for Privacy and Confidentiality in Student Education Records](http://nces.ed.gov/pubsearch/pubsinfo.asp?pubid=2011601)."[Glossary, Protecting Student Privacy, 2021/02/07](https://studentprivacy.ed.gov/glossary#header-for-I)

### Personally identifiable information (PII)

"Personally identifiable information (PII) includes information that can be used to distinguish or trace an individual’s identity either directly or indirectly through linkages with other information.

Additional information on PII is available in the [Family Educational Rights and Privacy Act Regulations, 34 CFR §99.3](http://www2.ed.gov/policy/gen/guid/fpco/pdf/ferparegs.pdf), and in the PTAC publication [Checklist: Data Governance](https://studentprivacy.ed.gov/node/167/)" [Glossary, Protecting Student Privacy, 2021/02/07](https://studentprivacy.ed.gov/glossary#header-for-I)

### Personally identifiable information for education records

"Personally identifiable information for education records is a FERPA term referring to identifiable information that is maintained in education records and includes direct identifiers, such as a student’s name or identification number, indirect identifiers, such as a student’s date of birth, or other information which can be used to distinguish or trace an individual’s identity either directly or indirectly through linkages with other information.

See [Family Educational Rights and Privacy Act Regulations, 34 CFR §99.3](http://www2.ed.gov/policy/gen/guid/fpco/pdf/ferparegs.pdf), for a complete definition of PII specific to education records and for examples of other data elements that are defined to constitute PII. Additional information is available in the PTAC publication [Protecting Student Privacy While Using Online Educational Services](https://studentprivacy.ed.gov/node/161/)." [Glossary, Protecting Student Privacy, 2021/02/07](https://studentprivacy.ed.gov/glossary#header-for-I)

## Information Privacy Acts (HIPAA vs FERPA)

The MCEC Project collects two types of data (also known as MCEC participant data):

- Email conversations in simple text format (.txt UTF8-encoded files) between instructors and students, and
- Survey data containing sociolinguistic, language background, and sociodemographic information.

While the MCEC Project does not deal with health information directly, the University of Arizona considers academic emails as educational records, which means that these are protected by [FERPA](Terms-and-definitions.md#family-educational-rights-and-privacy-act-ferpa):

"Examples of an Education Record include:
[...]
Course work including papers and exams, class schedules, as well as written, email or recorded communications that are part of the academic process
"[Family Educational Rights and Privacy Act of 1974 (FERPA), Office of the Registrar, 2021/02/07](https://www.registrar.arizona.edu/personal-information/family-educational-rights-and-privacy-act-1974-ferpa?topic=ferpa)

Additionally, email data, even if it is work/school related (i.e. not personal in nature), may contain direct or indirect personal identifiers (name, email, student/employee ID, etc.), medical data (emails messages such as "Dear Professor, I have a disability and I will need accommodation"), and student records (emails messages such as "...I am not sure why I got a C in the midterm exam.") both in structured or unstructured format. In order to protect our participant's privacy and confidentiality, we follow the guidance provided in both the Family Educational Rights and Privacy Act (FERPA) as well as the Health Insurance Portability and Accountability Act (HIPAA). We do so by:

A) Incorporating HIPAA's [Safe Harbor method](Terms-and-definitions.md#safe-harbor-method) for data de-identification. See our [HIPAA Tags](HIPAA-tags.md) document for more information.

B) Expanding the identifiers used in the Safe Harbor method to include FERPA and MCEC-specific categories.

[](https://www.hhs.gov/hipaa/for-professionals/privacy/special-topics/de-identification/index.html#standard)

### Family Educational Rights and Privacy Act (FERPA)

"The Family Educational Rights and Privacy Act (FERPA) is a federal law that affords parents the right to have access to their children’s education records, the right to seek to have the records amended, and the right to have some control over the disclosure of personally identifiable information from the education records. When a student turns 18 years old, or enters a postsecondary institution at any age, the rights under FERPA transfer from the parents to the student (“eligible student”). The FERPA statute is found at 20 U.S.C. § 1232g and the FERPA regulations are found at 34 CFR Part 99."([What is FERPA?](https://studentprivacy.ed.gov/faq/what-ferpa))

### FERPA protected information

Like HIPAA, FERPA protects two types of information: education records, and personally identifiable information.

"Education records are those records that are directly related to a student and are maintained by an educational agency or institution or by a party acting for the agency or institution. For more information, see the Family Educational Rights and Privacy Act regulations, 34 CFR §99.3." ([U.S. Department of Education. (2021, February 2). *Glossary*. Student Privacy.](https://studentprivacy.ed.gov/glossary#educational-records))

"Personally identifiable information (PII) includes information that can be used to distinguish or trace an individual’s identity either directly or indirectly through linkages with other information" [U.S. Department of Education. (2021, February 2). *Glossary*. Personally Identifiable Information (PII)](https://studentprivacy.ed.gov/glossary#header-for-P)

###  FERPA vs. HIPAA Infographic

"Health information is regulated by different federal and state laws, depending on the source of the information and the entity entrusted with the information. The Family Educational Rights and Privacy Act (FERPA) and the Health Insurance Portability and Accountability Act of 1996 (HIPAA) are two examples of federal laws that regulate privacy and the exchange of specific types of information. The work of healthcare providers, school personnel, and others interacts with FERPA and HIPAA frequently, which is why it is important to understand these laws and know when they apply."[FERPA vs. HIPAA infographic](https://www.cdc.gov/phlp/publications/topic/healthinformationprivacy.html)

### Health Insurance Portability and Accountability Act (HIPAA)

"The Health Insurance Portability and Accountability Act of 1996 (HIPAA) is a federal law that required the creation of national standards to protect sensitive patient health information from being disclosed without the patient’s consent or knowledge. The US Department of Health and Human Services (HHS) issued the HIPAA Privacy Rule to implement the requirements of HIPAA. The HIPAA Security Rule protects a subset of information covered by the Privacy Rule.

Compare HIPAA with FERPA

HIPAA Privacy Rule
The Privacy Rule standards address the use and disclosure of individuals’ health information (known as “protected health information”) by entities subject to the Privacy Rule. These individuals and organizations are called “covered entities.” The Privacy Rule also contains standards for individuals’ rights to understand and control how their health information is used. A major goal of the Privacy Rule is to ensure that individuals’ health information is properly protected while allowing the flow of health information needed to provide and promote high quality health care and to protect the public’s health and well-being. The Privacy Rule strikes a balance that permits important uses of information while protecting the privacy of people who seek care and healing."[About the Health Insurance Portability and Accountability Act](https://www.cdc.gov/phlp/publications/topic/hipaa.html)

## Multilingual College Email Corpus (MCEC)

The Multilingual College Email Corpus Project (MCEC) is an ongoing collection of student and instructor emails across several departments from the University of Arizona. It is a first-of-its-kind project given its wide scope (several disciplines and academic levels) and the sociolinguistic and language backgound information collected (L1, L2, linguistic experiences, heritage languages, and more).

### MCEC Project

This term is used to distinguish the activities surrounding the MCEC from the corpus itself (MCEC). The MCEC Project was founded in 2019 by Damian Romero as part of his Ph.D. dissertation project. After devising the MCEC Project, Damian joined efforts with Hanyu Jia and Mohammed AlShakhori to form the [Board of Directors](MCEC-team-roles.md#dirctors) of the MCEC Project. Since then, the project has grown to host numerous graduate students from different departments.

### MCEC Team

Also called the MCEC Research Team, includes all people who have shown interest in the MCEC Project and have been approved by the directors. Members of the MCEC team include the Principal Investigators (PI, co-PIs) and non-Principal Investigators (non-PIs.). For a full list, please consult our [MCEC Team Roles document](MCEC-team-roles.md).

### Principal investigators

Principal Investigators (PI and co-PIs) are researchers who have passed the relevant [Collaborative Institutional Training Initiative (CITI) training](https://rgw.arizona.edu/compliance/human-subjects-protection-program/getting-started) for ethical research and who have been approved by the [IRB](#human-subjects-protection-program-hspp-and-institutional-review-boards-irbs) to recruit participants. Not all MCEC Team members are principal investigators.

Only Principal investigators can recruit participants for the project. 

For an updated list of PIs, please refer to our [MCEC Team Roles document](MCEC-team-roles.md#current-pis).

For more information about PIs and co-PIs eligibility and responsibilities, consult the following UArizona HSPP documentation:

- [Principal Investigator Eligibility](https://rgw.arizona.edu/sites/default/files/pi_eligibility_v2020-06.pdf)
- [Principal Investigator (PI) Responsibilities](https://rgw.arizona.edu/sites/default/files/investigators_responsibility_after_irb_approval_v2020-06.pdf)

## Participants

### Instructors

Instructors is an umbrella term for anyone in charge or partly in charge of the academic process in a class. This includes professors, adjuncts, teaching assistants, graders, etc.)

### Students

The MCEC project collects data from a variety of students including undergraduate, graduate, on-campus, off-campus (online), and professional students, among others.

### MCEC participant data

Any data related to MCEC participants such as email exchanges and survey responses.

## Privacy and confidentiality

"The terms privacy and confidentiality are often invoked in discussions about rights and responsibilities when it comes to student records; in fact, they are often used interchangeably even though they have distinct meanings. So exactly what does each of these terms mean?" [Basic Concepts and Definitions for Privacy and Confidentiality in Student Education Records, p. 3](https://nces.ed.gov/pubs2011/2011601.pdf)

### Confidentiality

"Confidentiality relates to the management of another individual’s personally identifiable information. In a 2009 National Academy of Sciences, Institute of Medicine report, confidentiality is defined as referring to the obligations of those who receive personal information about an individual to respect the individual’s privacy by safeguarding the information (Committee on Health Research and the Privacy of Health Information: The HIPAA Privacy Rule, 2009, Beyond the HIPAA Privacy Rule: Enhancing Privacy, Improving Health Through Research, pp. 17–18). " [Basic Concepts and Definitions for Privacy and Confidentiality in Student Education Records, p. 4](https://nces.ed.gov/pubs2011/2011601.pdf)

### Privacy

"The concept of privacy relates to individual autonomy and each person’s control over their own information (Report of the National Academy of Science 1993 Panel Report Private Lives and Public Policies, p. 3). This includes each person’s right to decide when and whether to share personal information, how much information to share, and the circumstances under which that information can be shared (Report of the National Academy of Science 1993 Panel Report Private Lives and Public Policies, p. 22)." [Basic Concepts and Definitions for Privacy and Confidentiality in Student Education Records, p. 3](https://nces.ed.gov/pubs2011/2011601.pdf)

## Records

### Education records

The University of Arizona considers [academic emails as educational records](https://www.registrar.arizona.edu/personal-information/family-educational-rights-and-privacy-act-1974-ferpa?topic=ferpa). This means that all student email data is protected by FERPA. FERPA's definition of educational records is the following:

"Education records are those records that are directly related to a student and are maintained by an educational agency or institution or by a party acting for the agency or institution.

For more information, see 20 U.S.C. §1232g(a)(4)(A) and the [Family Educational Rights and Privacy Act regulations, 34 CFR §99.3](Family Educational Rights and Privacy Act regulations, 34 CFR §99.3).

Additional information is available in the PTAC publication [Checklist: Data Sharing Agreement](https://studentprivacy.ed.gov/node/418/)." [Glossary, Protecting Student Privacy, 2021/02/07](https://studentprivacy.ed.gov/glossary#header-for-E)

### IRB records

"IRB records are retained for six (6) years following completion of the research, which is longer than required by the human subject rules but is consistent with requirements for HIPAA retention.

This applies to all research studies, whether or not participants were enrolled. Sponsored grants and contracts may require additional periods for record retention." 
[Data Security and Records Retention, HSPP, 2021/02/07](https://rgw.arizona.edu/sites/default/files/data_security_and_records_retention_v2020-04.pdf)

### Record retention

"Research records should be maintained for whichever of the following time periods is the longest:
a) Six (6) years after the completion of the research; or
b) If the research involves children, 6 years after the youngest child in the research reaches the agesof majority (In Arizona the age of majority is 18 years old);
c) The length of time required by law (see below for FDA regulated research); or
d) As long as the sponsor requires (for sponsored research).
If desired, the investigator may archive these records with U"
[Data Security and Records Retention, HSPP, 2021/02/07](https://rgw.arizona.edu/sites/default/files/data_security_and_records_retention_v2020-04.pdf)

### Who grants access to records?

"Access to department specific records may be granted by the individual department. Permission for use of large-scale University of Arizona student records (undergraduate, graduate, and professional) is granted by the Registrar’s Office. The request for release of information and a copy of the protocol must be submitted to the Registrar for a determination of whether the release of information is appropriate under FERPA."[Access to Records, HSPP, 2021/01/07](https://rgw.arizona.edu/sites/default/files/access_to_records_v2020-03.pdf)

## Research Data Repository (ReDATA)

"The University of Arizona Research Data Repository (ReDATA) serves as the institutional repository for non-traditional scholarly outputs resulting from research activities by University of Arizona researchers. Depositing research materials (datasets, code, images, videos, etc.) associated with published articles and/or completed grants and research projects into ReDATA helps UA researchers ensure compliance with funder and journal data sharing policies as well as University data retention policies. ReDATA is designed for materials intended for public availability. All published materials will receive a Digital Object Identifier (DOI) for citation purposes" (ReDATA About Page, Data Cooperative, 2021/02/07)[https://data.library.arizona.edu/data-management/services/research-data-repository-redata]