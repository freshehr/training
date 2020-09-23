# openEHR modelling practical

## Getting started

1. Open a web browser – Chrome or Firefox are best

2. Go to [https://tools.openehr.org/designer](https://tools.openehr.org/designer/) 
(Best if you open this link in a new tab).


3. Login: 		`freshehr_training`	
   Password: 	`ad4freshtraining`

4. Choose the repository allocated to you – Aberdeen, Dundee or Inverness

5. Find ‘Nursing Admission Assessment STARTER.v0' in the list of templates. This will open the template.

6. Open the original ['Nursing Admission Assessment paper form'](Nursing%20Admission%20Assessment.pdf) (Best if you open this link in a new tab). 


## A. Tidy the basic template

### Problem/Diagnosis	

 - Rename the Problem/Diagnosis archetype to 'Main Diagnosis'

- Constrain out everything apart from 'Problem/Diagnosis name'

### Adverse Reaction Risk

- Pull in the 'Adverse Reaction Risk' archetype

- Set it's occurrences to 0..* to allow multiple allergies to be recorded.
  
- Constrain out everything apart from 'Substance' and 'Manifestation'

- Rename ‘Manifestation’ to ‘Reaction Details’ and make it mandatory

### Medication Order

- Clone 'Specific direction description'

- Rename one to 'Dose' and the other to 'Frequency'

### Vital Signs section

 - Pull in Pulse Oximetry into Vital Signs section

- Constrain out everything apart from 'SpO2' ratio

- Make 'systolic' and 'diastolic' Blood pressure mandatory


### Add a Clinical Frailty scale

Go to the International CKM 

[https://ckm.openehr.org/ckm/archetypes/1013.1.4691/export](https://ckm.openehr.org/ckm/archetypes/1013.1.4691/export)

 (Best if you open this link in a new tab).

- Press the ‘Export ADL’ button and save the archetype somewhere on your system

- Go back into Archetype Designer and go to top-menu->‘Import’ then either Browse to your file or drag and drop then Upload.

- Go back to your template, click on ‘content’, then pull in the Clinical Frailty scale from the list of archetypes on the right.

## B. Create a new local archetype - Additional information on admission

The nurses have used the templates you created but have asked for some changes.

You can view the original document here  

['Additional Information on Admission'](Additional%20information%20on%20admission.pdf) (Best if you open this link in a new tab).


- Create a new ADMIN_ENTRY archetype called ‘Inpatient admission details’ then add these ‘element’ datapoints ...

**Mode of access**	

			Ambulatory  	

			Wheelchair	

			Stretcher	

			Other		_________________________________

**Transported with	Oxygen**	

			Monitor	

			IV		

			Other		_________________________________

**Admission method	Waiting list**		

			Booked		

			Planned		

			A&E department	

			General Practitioner	

			Bed Bureau	

				Consultant Clinic	

			Other			____________________________		

**Additional Help needed**	

		Yes  	     No  

Once you have created your new archetype, go back to your template. Highlight ‘content’ and add your new archetype then Save it.

