# IAM Basics

The account created from previous lesson have an associate root user, and the account trust this user fully. This is why the account root user has full unrestricted access to the account.

In most real world situations, you want to be able to grant other people in your organization access to your AWS account. This might be users, groups or even applications which they create or manage, and you generally want restrict the access that these people, groups or applications have. It always best practice to only give the permissions required to do a job, or perform a task and this is called LEAST PRIVILEGED ACCESS

If root account credentials leaked then the damage is account wide, cannot restricted

Every AWS account comes with its own running copy of IAM, its own database.

**IAM is a globally resilient service**, so any data is always secure across all AWS regions

The IAM that you see in each of your accounts is your own dedicated instance of IAM separate from other accounts and from anyone else's accounts. Your AWS account is fully trust your instance of IAM.

Inside IAM you can create other identities, in 3 different types: user, group and role
  - User: Identities which represent humans or applications that need access to your account
  - Group: Collection of related users (development team, finance, HR team etc..)
  - Role: Can be used by AWS services, or for granting external access to your account

IAM allow create Policy which are essentially objects or documents, which can be use to allow or deny access to AWS services WHEN AND ONLY WHEN they're attached to IAM users, groups or roles. So policy on their own do nothing, they simply define, allow or deny right to certain services only when you attach the policies to other identities, so users, groups or roles do they have any effect

On high level, IAM have 3 main jobs
  - Manages identities - an ID Provider (IDP)
  - Authenticate (Prove you are who you claim to be)
  - Authorize (Allow or Deny access to resource, define by policy attach to the resource)

IAM only controls local identities in your account, and there is no cost to use IAM