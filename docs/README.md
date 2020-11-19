# openEHR modelling practical

## Agenda

## UHB: openEHR Training Session Two 18-Nov-2020

| Topic                                    | Dtn. | Start | End   |
| ---------------------------------------- | ---- | ----- | ----- |
| Introduction to openEHR Reference model  | 45   | 09:00 | 09:45 |
| Break                                    | 10   | 09:45 | 09:55 |
| Modelling example - Somerset dataset     | 45   | 09:55 | 10:40 |
| Break                                    | 10   | 10:40 | 10:50 |
| Working with the API		               | 45   | 10:50 | 11:35 |
| Break                                    | 10   | 11:35 | 11:45 |
| API continued	+ AQL	                   | 45   | 11:45 | 12:30 |
| Break                                    | 5    | 12:30 | 12:35 |
| Questions/ issues				           | 15   | 12:35 | 12:50 |

## Practical session - Getting started

1. Open a web browser – Chrome or Firefox are best

2. Go to [https://tools.openehr.org/designer](https://tools.openehr.org/designer/) 
(Best if you open this link in a new tab).


3. Login: 		`freshehr_training`	
   Password: 	`ad4freshtraining`

4. Choose the repository allocated to you – Aberdeen or Dundee

5. Open the [Somerset dataset mindmap](other/WMCN%20MDT.pdf) (best done in a new window) 

Have a look at each part of the dataset and think whether these might be INSTRUCTIONS, ACTIONS, OBSERVATIONS etc. - refer to your repository or CKM (openehr.ckm.org for possible examples).

6. Once you have an idea of roughly what kind of information is in there, have a go at creating new templates one for the Referral and for the Case/Pathway.


### Technical Intro

You may find this document helpful as a follow-up to the brief Technical Intro.
We will cover the Technical aspects in more depth in the next training event.

https://freshehr.github.io/dhi-proms/


## Download Postman artefacts

[![Run in Postman](https://run.pstmn.io/button.svg)](https://app.getpostman.com/run-collection/7643fba2c3a2034777e4#?env%5Bdhi-scotland%5D=W3sia2V5IjoiZWhyc2NhcGVCYXNlVXJsIiwidmFsdWUiOiIiLCJlbmFibGVkIjp0cnVlfSx7ImtleSI6Im9wZW5laHJCYXNlVXJsIiwidmFsdWUiOiIiLCJlbmFibGVkIjp0cnVlfSx7ImtleSI6Im9wZW5FaHJFeHBsb3JlciIsInZhbHVlIjoiaHR0cHM6Ly9leHBsb3Jlci5jb2RlNGhlYWx0aC5vcmcvZXhwbG9yZXIiLCJlbmFibGVkIjp0cnVlfSx7ImtleSI6IkNEUk5hbWUiLCJ2YWx1ZSI6ImVocnNjYXBlLmNvbSIsImVuYWJsZWQiOnRydWV9LHsia2V5IjoiZG9tYWluU3VmZml4IiwidmFsdWUiOiJjb2RlNGhlYWx0aC5vcmciLCJlbmFibGVkIjp0cnVlfSx7ImtleSI6IlNlc3Npb25IZWFkZXIiLCJ2YWx1ZSI6IkVoci1TZXNzaW9uLWRpc2FibGVkIiwiZW5hYmxlZCI6dHJ1ZX0seyJrZXkiOiJVc2VybmFtZSIsInZhbHVlIjoiYTgxZjQ3YzYtYTc1Ny00ZTM0LWI2NDQtM2NjYzYyYjRhMDFjIiwiZW5hYmxlZCI6dHJ1ZX0seyJrZXkiOiJQYXNzd29yZCIsInZhbHVlIjoiJDJhJDEwJDYxOWtpIiwiZW5hYmxlZCI6dHJ1ZX0seyJrZXkiOiJBdXRob3JpemF0aW9uIiwidmFsdWUiOiJCYXNpYyBZVGd4WmpRM1l6WXRZVGMxTnkwMFpUTTBMV0kyTkRRdE0yTmpZell5WWpSaE1ERmpPaVF5WVNReE1DUTJNVGxyYVE9PSIsImVuYWJsZWQiOnRydWV9LHsia2V5IjoiYWNjb3VudE5hbWUiLCJ2YWx1ZSI6ImRoaS1zY290bGFuZCIsImVuYWJsZWQiOnRydWV9LHsia2V5IjoiY29tbWl0dGVyTmFtZSIsInZhbHVlIjoiRHIgQ2hhbCIsImVuYWJsZWQiOnRydWV9LHsia2V5IjoicGF0aWVudE5hbWUiLCJ2YWx1ZSI6Ikl2b3IgQ294IiwiZW5hYmxlZCI6dHJ1ZX0seyJrZXkiOiJzdWJqZWN0SWQiLCJ2YWx1ZSI6Ijk5OTk5OTkwMDAiLCJlbmFibGVkIjp0cnVlfSx7ImtleSI6Im5oc051bWJlciIsInZhbHVlIjoiOTk5OTk5OTAwMCIsImVuYWJsZWQiOnRydWV9LHsia2V5Ijoic3ViamVjdE5hbWVzcGFjZSIsInZhbHVlIjoidWsubmhzLm5oc19udW1iZXIiLCJlbmFibGVkIjp0cnVlfSx7ImtleSI6ImVocklkIiwidmFsdWUiOiIzZTY3NDczOS05NTBjLTRiOGEtOTc2Yi01YWVmMjFjNjE4YzUiLCJlbmFibGVkIjp0cnVlfSx7ImtleSI6InBhcnR5SWQiLCJ2YWx1ZSI6IjQwOTUwMyIsImVuYWJsZWQiOnRydWV9LHsia2V5IjoidGVtcGxhdGVJZCIsInZhbHVlIjoiREhJIC0gVlRFIEFzc2Vzc21lbnQtdjAiLCJlbmFibGVkIjp0cnVlfSx7ImtleSI6ImNvbXBvc2l0aW9uSWQiLCJ2YWx1ZSI6IjA5NWFkYzg3LTcxY2MtNDFlMS1hYTQ2LWFmOWQ3MmY4ZGRmNjo6YTgxZjQ3YzYtYTc1Ny00ZTM0LWI2NDQtM2NjYzYyYjRhMDFjOjoxIiwiZW5hYmxlZCI6dHJ1ZX1d)

## A. List templates and upload a new template

https://freshehr.github.io/dhi-proms/cdr/ehrscape/ECDR2-openehr-templates/

## B. Create new EHR - register a patient with the CDR

https://freshehr.github.io/jmohw-cdr/opencdr/OCDR5-creating-an-ehr/

## C. Retrieve the patient's ehrId from their subjectID (NHS Number)

https://freshehr.github.io/dhi-proms/cdr/ehrscape/ECDR5-retrieving-an-ehrId/

## D. Get an example template

```bash
curl --location --request GET 'https://cdr.code4health.org/rest/v1/template/JMOHW - Passport observations.v0/example?format=FLAT&exampleFilter=OUTPUT' \
--header 'Content-Type: application/json' \
--header 'Authorization: {{Authorization}}'
```
## E. Commit a composition

https://freshehr.github.io/dhi-proms/dhis/DHIS6-committing-proms-data/

## F. Update a composition

https://freshehr.github.io/dhi-proms/dhis/DHIS8-updating-proms-data/

## G. Run a query

https://freshehr.github.io/dhi-proms/dhis/DHIS5-querying-proms-data/

### Further reading

#### General Information:

openEHR website: https://www.openehr.org/

openEHR videos and presentations: https://www.youtube.com/c/openehr/featured

openEHR Discourse (discussion forum): https://discourse.openehr.org/

What is openEHR? - Introduction: https://www.openehr.org/about/what_is_openehr

openEHR Zotero library: https://www.zotero.org/libraries


Clinical Knowledge Managers (CKMs) - archetype repositories and governance tools:

International CKM: https://ckm.openehr.org/ckm/

Apperta CKM (UK): https://ckm.apperta.org/ckm/


#### Social Care Examples:

Social Care Project on Apperta CKM: https://ckm.apperta.org/ckm/projects/1051.61.50
A repository for the social care related archetypes and templates that we have been working on for various use cases
Care Home Dataset template: https://ckm.apperta.org/ckm/templates/1051.57.273

Based on the care home data inventory described in a recent paper by Lucy Johnston et al from Edinburgh Napier University, which is available here: https://www.medrxiv.org/content/10.1101/2020.08.17.20176503v2 

The original data inventory is shown below, along with another care home dataset that we have used as an example in our data models.
![](images/care-home-data-stds.png)
