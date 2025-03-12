Key Points Summary
1. RUM Enablement Process
Abhijeet is guiding the process for new RUM enablement.
Separate code has been created for Non-Prod and Prod environments by Abhijeet.
The previous global code, which can implement changes for all environments in one go, is still being used for management purposes.
Jeff and Stephen requested Abhijeet to modify the code for MZ to align with the approach used for RUM. This task is currently pending on Abhijeet's side.


2. MZ Change Request Process
For MZ changes:
A standard change (managed on our side) needs to be created.
Since the standard change approval isn't in place yet, a normal production change will be used temporarily.


3. RUM Change Request Process
For RUM changes:
It is categorized as a requestor change.


4. Batch Execution Plan
Jeff and Stephen suggested executing changes in batches:
A single change request will be created for MZ.
Sub-CTASKs will be assigned to individual ticket owners for validation of their changes.
Batch changes will be executed every Friday.


5. RUM Validation Process
Validation for RUM changes is the responsibility of the application team.
Post-implementation in Non-Prod:
The application team must confirm that their applications are healthy.
Only after receiving confirmation from the application team will RUM changes be implemented in Production.
