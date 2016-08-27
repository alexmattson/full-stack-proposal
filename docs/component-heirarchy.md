## Component Heirarchy

**AuthFormContainer**
 - AuthForm

**HomeContainer**
 - Home
  + ApplicationVolume
  + Buttons
  + Applications
 - Sidebar

**ApplicationContainer**
 - NotesHeader
  * NoteIndex

**Search**

**NotebookSearch**
 + AutoSearch
 * AutoSearchResults

## Routes

|Path   | Component   |
|-------|-------------|
| "/sign-up" | "AuthFormContainer" |
| "/sign-in" | "AuthFormContainer" |
| "/home" | "HomeContainer" |
| "/home/new-application" | "NewApplicationContainer" |
| "/home/update-application" | "UpdateContainer" |
| "/home/rejected" | "RejectedContainer" |
| "/home/offer" | "OfferContainer" |
| "/home/application/:applicationId" | "ApplicationContainer" |
| "/home/application/update-application" | "UpdateContainer" |
| "/home/application/rejected" | "RejectedContainer" |
| "/home/application/offer" | "OfferContainer" |
| "/profile" | "ProfileContainer" |
| "/search" | "Search" |
