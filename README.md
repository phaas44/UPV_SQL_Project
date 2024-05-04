# UPV SQL Project
This repo contains the results of a group project conducted at UPV during my exchange year. We designed an Oracle Database using Oracle SQL Developer for a given task description.

## Key Learnings
During this project work I mainly learned about:
- SQL
- UML Class Modelling
- Oracle Databases

## Task Description
We are going to design the database of a police investigation department. We must store information about the department’s employees, whose SSN is unique and it is always known; the passport number, which is also unique; the employee number, which identifies the employee, the name, telephone number, and category. Some workers are investigators, and others are forensic experts.

The following data on the crimes to be investigated are also kept: identification code, type, date of registration of the crime, description, and place. The place is stored as a longitude and latitude, as a crime potentially
could take place in a secluded area without a specific address. The longitude and latitude has to be provided. There is also information on other persons, for whom a code is stored to identify them, year of birth,
and address; a general description of further known details of the person are also stored. It is necessary to record whether there is a relationship between persons, indicating what type of relationship (parent, sibling, cousin, friend, co-worker, etc.). The database does not store information about all
existing people.For each crime, it is possible to know which persons have been victims, indicating,in that case, the effect of the crime on them. A victim always has an effect.

The persistence of who is the victim, witness, and suspect in a
crime are in this case considered fixed roles after a trial and judgment have been made. Therefore, one person can only take one of these roles in one crime, and the role cannot be changed. The suspect in this case should therefore be considered more as a convict. The choice of using fixed roles was made to keep a more simplistic approach to the assignment. However, this does not perfectly reflect the reality in which a person might change role in a crime or might take more than one role as an investigation progresses or if a case gets reopened. When there is a fatality, and the corpse has been found, the corpse data (Data about the dead person itself) are recorded, and a forensic scientist is later assigned to perform the autopsy. When the
autopsy is finished, the forensic scientist fills out a report on the result. For each crime, it is also stored, when known, which person or persons are suspects. It is also stored which persons have witnessed the crime, and the witness always has an interrogation. Also the the investigator who has conducted the interrogation, the date of the interrogation, and the statement
of the witness has to be stored. It was chosen that only witnesses gets an interrogation.

For each crime, the evidences that are found are stored. Each piece of evidence is numbered with a unique number for each crime. A piece of evidence can be of different types: a photo from which the investigator who took it is saved; a
fingerprint, which is associated, when possible, with a person; a recording or other types of evidence. For each piece of evidence, different types of analysis can be performed. Each type of analysis has a code that identifies it, a name,
and a description. For every analysis of an evidence, a report is made after analyzing a piece of evidence which consists of the resultant data and the conclusion. The forensic expert, who has conducted the analysis, also writes the report.

## Proposed Database Architecture
A detailed UML Classdiagramm can be found [here](https://github.com/phaas44/upv_sql_project/blob/master/docs/Database_Architecture.pdf)
