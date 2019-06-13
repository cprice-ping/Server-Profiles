This set of calls is used to demonstrate DataGov's ability to perform fine-granined access to **any** REST API.

APIs that are being called in this set are:
* PingDirectory REST API \ Consent API
* Epic FHIR Sandbox
* Cerner FHIR Sandbox

Things that are showed in this:

* PingDirectory REST API
  * Scope --> Attribute mapping
  * Scope --> Method mapping
  * User --> Record Ownership enforcement
  * Preferences --> Filtered Results

* FHIR APIs
  * Consent --> Definition
  * Consent --> Capture
  * Consent --> Versioning
  * Consent --> Revocation
  * Consent --> Delegation
  * Account Linking --> PD User to FHIR Systems

The demo is designed to be an example of a Patient Portal - with access to manipulate the User Profile, and access controls to various EMR Patient Records

The Server Profile for this demo consists of:
* PingFederate - Used to Authenticate User and provide Bearer tokens (Note: the default DG ATV is a MockATV - no PF required)
* PingDirectory - Used to store the Portal User information, along with Users and Consent Definitions for this demo
* [Coming soon] PingDataGovernance - The API proxy that's enforcing the Consent request
* [Coming soon] DG Policy Admin Point - Used to show the policies that are defined
