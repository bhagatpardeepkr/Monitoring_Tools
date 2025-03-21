Friday: Group all MZ requests, raise Non-Prod Clone CR, and create a release branch (release/CRNum).
Monday: Gain CR approvals, raise a single PR from release branch to main, and SMEs review the PR.
If changes are needed: Team modifies accordingly; SMEs approve on Tuesday.
If no changes: SMEs approve changes on Monday itself.
Tuesday: Merge branch, run Non-Prod pipeline, and inform teams. Create Prod CR for MZs approved in Non-Prod.
Thursday: Run Prod pipeline (code is pre-approved, no SME required). Implement changes in Prod as planned.
Each week: One CR for Non-Prod, one CR for Prod, one branch, and one PR; pipeline runs twice.
