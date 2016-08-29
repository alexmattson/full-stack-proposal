## Component Hierarchy

**AuthFormContainer**
  - AuthForm

**HomeContainer**
  - Home
    + ApplicationVolume
    + Buttons
      * NewApplication
      * UpdateApplication
      * RejectApplication
      * OfferApplication
    + Applications
  - Sidebar

**ApplicationContainer**
  - Application
   + Header
   + Progress
   + Contact
   + Events
    * NewEvent
    * UpdateEvent

**ProfileContainer**
  - Profile
    + Header
    + Calendar

**Search**
 + AutoSearch
 * AutoSearchResults

## Routes

|Path   | Component   |
|-------|-------------|
| "/sign-up" | "AuthFormContainer" |
| "/sign-in" | "AuthFormContainer" |
| "/home" | "HomeContainer" |
| "/home/new-application" | "NewApplication" |
| "/home/update-application" | "UpdateApplication" |
| "/home/reject-application" | "RejectApplication" |
| "/home/offer-application" | "OfferApplication" |
| "/application/:applicationId" | "ApplicationContainer" |
| "/application/:applicationId/update-application" | "UpdateApplication" |
| "/application/:applicationId/reject-application" | "RejectApplication" |
| "/application/:applicationId/offer-application" | "OfferApplication" |
| "/application/:applicationId/offer-application" | "OfferApplication" |
| "/application/:applicationId/events" | "NewEvent" |
| "/application/:applicationId/events/:event_id" | "UpdateEvent" |
| "/profile" | "ProfileContainer" |
