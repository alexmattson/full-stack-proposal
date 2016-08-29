# Redux Structure

## Auth Cycles

### Session API Request Actions

* `signUp`
  0. invoked from `SignupForm` `onSubmit`
  0. `POST /api/users` is called.
  0. `receiveCurrentUser` is set as the success callback.
* `logIn`
  0. invoked from `Navbar` `onSubmit`
  0. `POST /api/session` is called.
  0. `receiveCurrentUser` is set as the callback.
* `logOut`
  0. invoked from `Sidebar` `onClick`
  0. `DELETE /api/session` is called.
  0. `removeCurrentUser` is set as the success callback.

### Session API Response Actions

* `receiveCurrentUser`
  0. invoked from an API callback
  0. the `SessionReducer` stores `currentUser` in the application's state.
* `removeCurrentUser`
  0. invoked from an API callback
  0. the `SessionReducer` removes `currentUser` from the application's state.

## Error Cycles

### Error API Response Actions
* `setErrors`
  0. invoked from API callbacks on error for actions that generate POST requests
  0. the `ErrorReducer` stores the `form` in the application's state; `errors` are mapped to their respective forms
* `removeErrors`
  0. invoked from API callbacks on success for actions that generate POST requests
  0. the `ErrorReducer` removes `errors` for a given `form` in the application's state.

## Application Cycles

### Applications API Request Actions

* `fetchAllApplications`
  0. invoked from `ApplicationsIndex` `didMount`/`willReceiveProps`
  0. `GET /api/notes` is called.
  0. `receiveAllApplications` is set as the success callback.

* `createApplication`
  0. invoked from new application button `onClick`
  0. `POST /api/applications` is called.
  0. `receiveSingleApplication` is set as the success callback.

* `fetchSingleApplication`
  0. invoked from `ApplicationDetail` `didMount`/`willReceiveProps`
  0. `GET /api/applications/:id` is called.
  0. `receiveSingleApplication` is set as the success callback.

* `updateApplication`
  0. invoked from `ApplicationForm` `onSubmit`
  0. `POST /api/applications` is called.
  0. `receiveSingleApplication` is set as the success callback.

* `destroyApplication`
  0. invoked from delete application button `onClick`
  0. `DELETE /api/applications/:id` is called.
  0. `removeApplication` is set as the success callback.

### Applications API Response Actions

* `receiveAllApplications`
  0. invoked from an API callback
  0. the `ApplicationReducer` updates `applications` in the application's state.

* `receiveSingleApplication`
  0. invoked from an API callback
  0. the `ApplicationReducer` updates `applications[id]` in the application's state.

* `removeApplication`
  0. invoked from an API callback
  0. the `ApplicationReducer` removes `applications[id]` from the application's state.

## Event Cycles

### Events API Request Actions

* `fetchAllEvents`
  0. invoked from `EventsIndex` `didMount`/`willReceiveProps`
  0. `GET /api/events` is called with query params.
  0. `receiveAllEvents` is set as the success callback.

* `createEvent`
  0. invoked from new event button `onClick`
  0. `POST /api/applications/:application_id/events` is called.
  0. `receiveApplicationEvents` is set as the callback.

* `fetchApplicationEvent`
  0. invoked from `EventDetail` `didMount`/`willReceiveProps`
  0. `GET /api/applications/:application_id/events` is called.
  0. `receiveApplicationEvents` is set as the success callback.

* `updateEvent`
  0. invoked from `EventForm` `onSubmit`
  0. `POST /api/applications/:application_id/events/:event_id` is called.
  0. `receiveApplicationEvents` is set as the success callback.

* `destroyEvent`
  0. invoked from delete event button `onClick`
  0. `DELETE /api/applications/:application_id/events/:event_id` is called.
  0. `removeEvent` is set as the success callback.

### Events API Response Actions

* `receiveAllEvents`
  0. invoked from an API callback.
  0. The `Event` reducer updates `events` in the application's state.

* `receiveApplicationEvents`
  0. invoked from an API callback.
  0. The `Event` reducer updates `events` in the application's state.

* `removeEvent`
  0. invoked from an API callback.
  0. The `Event` reducer removes event from `events` in the application's state.

## Contact Cycles

### Contacts API Request Actions

* `createContact`
  0. invoked from new event button `onClick`
  0. `POST /api/applications/:application_id/contacts` is called.
  0. `receiveApplicationContacts` is set as the callback.

* `fetchApplicationContact`
  0. invoked from `ContactDetail` `didMount`/`willReceiveProps`
  0. `GET /api/applications/:application_id/contacts` is called.
  0. `receiveApplicationContacts` is set as the success callback.

* `updateContact`
  0. invoked from `ContactForm` `onSubmit`
  0. `POST /api/applications/:application_id/contacts/:contact_id` is called.
  0. `receiveApplicationContacts` is set as the success callback.


### Contacts API Response Actions

* `receiveApplicationContacts`
  0. invoked from an API callback.
  0. The `Contact` reducer updates contact from `application` in the application's state.

* `updateContact`
  0. invoked from an API callback.
  0. The `Contact` reducer updates contact from `application` in the application's state.

## SearchSuggestion Cycles

* `fetchSearchSuggestions`
  0. invoked from `ApplicationSearchBar` `onChange` when there is text
  0. `GET /api/applications` is called with params.
  0. `receiveSearchSuggestions` is set as the success callback.

* `receiveSearchSuggestions`
  0. invoked from an API callback.
  0. The `SearchSuggestion` reducer updates `suggestions` in the application's state.

* `removeSearchSuggestions`
  0. invoked from `NoteSearchBar` `onChange` when empty
  0. The `SearchSuggestion` reducer resets `suggestions` in the application's state.
