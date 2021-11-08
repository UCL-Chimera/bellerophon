# CHIMERA data management mini meeting  -- Mon 8 Nov 2021 at 15:00 - 16:00

Attendees

* Sam Ray
* Claire Black
* Eliza Brown
* Anika Cawthorn
* Mohsin Shah
* Daniel Key

Apologies

* Thomas Frost
* Stef Piatek




### Summary

The proposed project will gather data from UCLH for a project using blood gas data. There are two examples (1) Oxygen dissociation curve (ODC) evaluation over time, age, and disease status (Eliza) and (2) Undefined work on arterial blood gases (Thomas). Each project should run end to end from the source data at the hospital to an analysis in the UCL DSH. 

This project will emphasise the UCLH data pipeline as the other projects will work using GOSH T3 data. However, this exemplar provides the best opportunity to understand what merging data from the two sites will be like. We propose therefore a very simple abbreviated extract of similar data from GOSH that we will move to the DSH, but won't plan to use in the actual analysis.




### Data ask

Rough categories of data that are likely to be needed

Data items

* Spine of patient identifiers (e.g. define a person)
* Arterial bloods gases data (needs further specifying; which fields are critical)
* SpO2
* FiO2
* Ventilator data such that we can define when a patient is on/off a ventilator
* COVID status

Cohort

* Not discussed in detail but ?12months of the smallest subset of fields above




### Data pipeline

* Local query 
	* UCLH: decide on source ?DeCOVID ?EMAP ?OMOP
		* need to review the pros and cons but for now should just do whatever is 'easiest'
* Local anonymisation as per CHIMERA requirements
* Local procedure to confirm data ready to move
	* code to anonymise
	* pull request to review that code
	* four eyes to check data before actual transfer
* Upload to DSH
* Run model 




### Process

Work toward a 2 stage timeline

* Next 3 weeks: Re-group and orient data flows with other groups
	* Alex and Hugh: data heavy
	* Vanessa and Sina: super small
* End of Feb '22: 
	* First pass complete for _all_ data groups (even if incomplete in different ways) so we can discuss what's realistic going forward




### Actions

We will convert these to github issues after meeting with the other groups.



- [ ] prepare a data dictionary @eliza-brown @thomas-frost
- [ ] discuss phenotyping for ventilators from DeCOVID/OMOP (@ed-palmer) and CCHIC @finn-catling : @eliza-brown @thomas-frost  
- [ ] prepare local data
	- [ ] UCLH @anika-cawthorn
	- [ ] GOSH @daniel-key @mohsin-shaw  (parallel extract of token of number of rows and fields from DRIVE not to be merged and used but for visibility and understanding of the process)
- [ ] restart conversation with DSH
	- [ ] find IAA (information asset administrator) @steve-harris to ask @julie-taylor and then @claire-black to explain what this means
- [ ] work through a pathway of moving data from UCLH
- [ ] success criteria: prepare an example analysis from both users @eliza-brown @thomas-frost perhaps using CCHIC data that we can use to confirm this works in the DSH
- [ ] CCHIC as a parallel and how much this helps
	- [ ] need to decide on how/where to align
	- [ ] use local DeCOVID build instead of EMAP?











