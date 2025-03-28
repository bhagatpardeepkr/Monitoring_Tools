As discussed in today's call with Abhijeet, we have reviewed our strategy to onboard MZ and RUM in a more streamlined and efficient way, rather than working on multiple tasks simultaneously.

For MZ:
Non-Prod:

We will create a single standard production change request, and in parallel, we will create an intermediate branch where all ticket changes will be pushed with comments in the format #<ticket-no.> in front of the changes. This approach will make it easy to segregate and identify code changes.
For the change request, we will create corresponding CTASKs for every user to validate their respective changes.
Once validation is done, we will obtain the required approvals and then create a PR (Pull Request) from the intermediate branch. Abhijeet will only need to review and approve this single PR.
After that, we will run the Jenkins job for Non-Prod. Once the change request is implemented, we will ask the user to validate the changes.
Finally, after all CTASKs are closed, we will move the status of the change request to "Review."


Prod:

There is no need to create a PR for production because the changes will already be present in Non-Prod. We will simply run the Jenkins job again for production.
However, we will need to create a separate PR for production and obtain all required approvals.
As discussed, for the IAM role, we will adopt a similar approach: create an intermediate branch, push all changes into it, and then create a PR.
After approvals, we will run a single Jenkins job for both MZ and IAM changes in production.

For RUM:
Non-Prod:

As discussed, we will create a single change request for the entire Non-Prod environment.
We will then create an intermediate branch and push all changes in one go for Dev, UAT, and Pre-Prod in the Terraform code.
Once the change request is implemented, we will ask users to validate the changes.

Prod:
We will request the users to create the change request on their side.
On our side, we will create corresponding CTASKs to implement the required changes.
