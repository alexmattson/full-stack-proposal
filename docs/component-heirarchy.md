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

**ProfileContainer**
  - Profile
    + Header
    + Calendar

**Search**

**ApplicationSearch**
 + AutoSearch
 * AutoSearchResults

## Routes

|Path   | Component   |
|-------|-------------|
| "/sign-up" | "AuthFormContainer" |
| "/sign-in" | "AuthFormContainer" |
| "/home" | "HomeContainer" |
| "/application/:applicationId" | "ApplicationContainer" |
| "/profile" | "ProfileContainer" |
| "/search" | "Search" |
