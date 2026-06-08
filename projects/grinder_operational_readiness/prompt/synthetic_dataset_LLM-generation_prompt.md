# Synthetic Dataset Generation Prompt — Grinder Pre-Use Checklist Prototype

Generate a realistic synthetic CSV dataset based on a workshop portable angle grinder pre-use inspection checklist used in an industrial maintenance environment.
The dataset is for analytical and educational purposes only and must not represent real employees, real operational records, or real facilities.
The generated dataset must align directly with the inspection structure of the grinder pre-use checklist.

**Dataset Size**
Generate between 50 rows.

**Output Format**
Output only:

* clean CSV format
* headers included
* no markdown
* no explanations
* no code blocks

**Required Columns**
Use the following columns exactly:
date time shift grinder_asset_id grinder_specification
power_cable_ok trigger_switch_ok guard_ok side_handle_ok flange_locknut_ok abrasive_disc_ok rpm_compatible housing_vents_ok spindle_tightness_ok ppe_confirmed
inspection_result defects_noted tagged_out

**Operational Rules**
date
Use realistic sequential dates across a 2–3 week workshop operating period.

time
Use realistic inspection times such as:

* 06:30
* 14:10
* 18:45

shift
Allowed values:

* Day
* Afternoon
* Night

grinder_asset_id
Use IDs such as:

* AG-01
* AG-02
* AG-03
* AG-04
* AG-05

grinder_specification
Allowed values:

* 4 inch
* 7 inch

**Inspection Fields**
The following fields must contain only:

* Yes
* No
Fields:

* power_cable_ok
* trigger_switch_ok
* guard_ok
* side_handle_ok
* flange_locknut_ok
* abrasive_disc_ok
* rpm_compatible
* housing_vents_ok
* spindle_tightness_ok
* ppe_confirmed
Most inspections should pass.

Occasionally include failures such as:

* damaged power cable
* cracked abrasive disc
* missing guard
* loose handle
* RPM incompatibility
* blocked cooling vents

inspection_result
Allowed values:

* Pass
* Fail
If multiple inspection fields contain "No", inspection_result should usually be "Fail".
defects_noted
Include short realistic operational defect summaries such as:

* Cable insulation damaged
* Guard missing
* Disc cracked near edge
* Cooling vents blocked with dust
* Flange worn
* PPE incomplete
* Spindle loose during rotation test
Leave some rows blank when no defects are observed.
tagged_out
Allowed values:

* Yes
* No
If:

* abrasive_disc_ok = No
* rpm_compatible = No
* guard_ok = No
* spindle_tightness_ok = No
then tagged_out should frequently be "Yes".
Operational Realism Constraints

* Avoid perfectly clean data.
]* Include occasional repeated defects on the same grinder.
* Simulate believable workshop inspection variability.
* Most inspections should pass.
* Some inspections should fail.
* Avoid unrealistic randomization.
* Do not generate impossible combinations.
Important Constraint
The dataset must reflect:

* grinder operational readiness inspection logic
* equipment-focused inspection workflows
* workshop maintenance conditions
The dataset must not include:

* employee performance scoring
* behavioral monitoring
* surveillance logic
* disciplinary metrics
