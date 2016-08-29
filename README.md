![logo.png](https://s13.postimg.org/lnbhemlav/logo.png)

[Heroku link][heroku]

[heroku]: http://www.herokuapp.com

## Minimum Viable Product

Managing all the intricacies of the job search process can be difficult; this site aims to make it a little bit easier for the user. No more messing around with nasty spreadsheets, we will provide a repository for all your details of the job search process. By the end of Week 9, this app will, at a minimum, satisfy the following criteria with smooth, bug-free navigation, adequate seed data and sufficient CSS styling:

- [ ] Hosting on Heroku
- [ ] New account creation, login, and guest/demo login
- [ ] Application CRUD cycle
- [ ] Event scheduling and managing on application page
- [ ] Events will automatically be pushed to calendar on Profile page
- [ ] Statistics tracking the number of applications sent, responses received, and offers received
- [ ] Production README

## Design Docs
* [View Wireframes][wireframes]
* [React Components][components]
* [API endpoints][api-endpoints]
* [DB schema][schema]
* [Redux Structure][redux-structure]
* [Sample State][sample-state]

[wireframes]: http://imgur.com/a/9ZVln
[components]: docs/component-heirarchy.md
[redux-structure]: docs/redux-structure.md
[sample-state]: docs/sample-state.md
[api-endpoints]: docs/api-endpoints.md
[schema]: docs/schema.md

## Implementation Timeline

### Phase 1: Backend setup and Front End User Authentication (2 days)

**Objective:** Functioning rails project with front-end Authentication

- [ ] New Rails project
- [ ] `User` model/migration
- [ ] Back end authentication (session/password)
- [ ] `StaticPages` controller and root view
- [ ] Webpack & react/redux modules
- [ ] `APIUtil` to interact with the API
- [ ] Redux cycle for frontend authentication
- [ ] User signup/signin components
- [ ] Blank landing component after signup/signin
- [ ] Style signup/signin components
- [ ] Seed users
- [ ] Review phase 1

### Phase 2: Applications Model, API, and components (2 days)

**Objective:** Applications can be created, read, edited and destroyed through
the API.

- [ ] `Application` model
- [ ] Seed database with a small amount of test data
- [ ] CRUD API for applications (`ApplicationsController`)
- [ ] JBuilder views for applications
- Application components and respective Redux loops
  - [ ] `ApplicationsIndex`
  - [ ] `ApplicationIndexItem`
  - [ ] `ApplicationNewForm`
  - [ ] `ApplicationUpdateForm`
  - [ ] `ApplicationRejectForm`
  - [ ] `ApplicationOfferForm`
- [ ] Style applications components
- [ ] Seed sample application

### Phase 3: Events Model, API, and components (2 days)

**Objective:** Events belong to an Application and can be created, read, edited and destroyed through the API.

- [ ] `Event` model
- [ ] Seed database with a small amount of test data
- [ ] CRUD API for events (`EventsController`)
- [ ] JBuilder views for events
- [ ] Adding events requires an application
- [ ] Calendar on profile page
- [ ] Adding an event on an application adds event to calendar
- [ ] Style event components
- [ ] Seed sample events

### Phase 4: Contacts (1 day)

**Objective:** Application has a contact and can be created, read and edited.

- [ ] `Contact` model
- [ ] Adding contact to applications
- [ ] Style contact components
- [ ] Seed sample contact

### Phase 5: Charts (1 day)

**objective:** Charts for Application statistics.

- [ ] Integrate [ChartJS][ChartJS]
- [ ] Home page chart tracking applications sent over time.
- [ ] Profile page Charts
  + [ ] Applications Sent
  + [ ] Responses Received
  + [ ] Offers Received
- [ ] Add styling to charts

[ChartJS]:http://www.chartjs.org/

### Phase 6: Search (0.5 days)

**objective:** Auto complete search feature for application.

- [ ] Integrate [EasyAutocomplete][EasyAutocomplete]
- [ ] Style Search components.

[EasyAutocomplete]:http://easyautocomplete.com/


### Phase 6: - Final Styling integration (0.5 days)

**objective:** Ensure every component is integrated well with each other on the site.

- [ ] Review styling.

### Bonus Features (TBD)
- [ ] Emphasis on simple yet engaging animated transition elements throughout the site similar to [ChartJS][ChartJS]
- [ ] Make charts comparative to other applicants
- [ ] Notifications for upcoming events
- [ ] Gmail integration to allow a user to see all emails from the email listed as the contact for the application
- [ ] “Offers page” to track and manage open offers
- [ ] Market salary calculation through payscale api
- [ ] Resume uploading and management system

[ChartJS]: CharJShttp://www.chartjs.org/
