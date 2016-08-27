# Job Logged

[Heroku link][heroku]

[heroku]: http://www.herokuapp.com

## Minimum Viable Product

Managing all the intricacies of the job search process can be difficult; this site aims to make it a little bit easier for the user. No more messing around with nasty spreadsheets, we will provide a repository for all your details of the job search process. By the end of Week 9, this app will, at a minimum, satisfy the following criteria with smooth, bug-free navigation, adequate seed data and sufficient CSS styling:

- [ ] Hosting on Heroku
- [ ] New account creation, login, and guest/demo login
- [ ] Application CRUD cycle
- [ ] Event scheduling and managing on application page
- [ ] Events will automatically be pushed to calander on Profile page
- [ ] Statistics tracking the number of applications sent, responses received, and offers received
- [ ] Autocomplete search feature
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

### Phase 2: Notes Model, API, and components (2 days)

**Objective:** Notes can be created, read, edited and destroyed through
the API.

- [ ] `Note` model
- [ ] Seed database with a small amount of test data
- [ ] CRUD API for notes (`NotesController`)
- [ ] JBuilder views for notes
- Note components and respective Redux loops
  - [ ] `NotesIndex`
  - [ ] `NoteIndexItem`
  - [ ] `NoteForm`
- [ ] Autosave notes feature
- [ ] Style notes components
- [ ] Seed notes

### Phase 3: Notebooks (2 day)

**Objective:** Notes belong to Notebooks that can be created, read, edited and destroyed through the API.

- [ ] `Notebook` model
- [ ] Seed database with a small amount of test data
- [ ] CRUD API for notes (`NotebooksController`)
- [ ] JBuilder views for notebooks
- [ ] Adding notes requires a notebook
- [ ] Moving notes between notebooks
- [ ] Viewing notes by notebook
- [ ] Style notebook components
- [ ] Seed notebooks

### Phase 4: Tags (1 days)

**Objective:** Notes can be tagged with multiple tags, and tags are searchable.

- [ ] `Tag` model and `Taggings` join table
- [ ] Fetching tags for notes
- [ ] Adding tags to notes
- [ ] Searching notes by tag
- [ ] Style search & tag components
- [ ] Seed tags with seed data

### Phase 5: Allow Complex Styling in Notes (1 days, W2 Th 6pm)

**objective:** Allow rich text editing of notes.

- [ ] Integrate `react-quill` (based on Quill.js).
- [ ] Rails helpers to sanitize HTML before rendering.
- [ ] Style Quill components.
- [ ] Add Quill styling to seeded notes

### Phase 6: - Pagination / infinite scroll for Notes Index (1 day, W2 F 6pm)

**objective:** Add infinite scroll to Notes Index

- [ ] Paginate Notes Index API to send 20 results at a time
- [ ] Append next set of results when user scrolls and is near bottom
- [ ] Style scroll components and transitions
- [ ] Ensure seed data demonstrates infinite scroll

### Bonus Features (TBD)
- [ ] Emphasis on simple yet engaging animated transition elements throughout the site similar to [ChartJS][ChartJS]
- [ ] Make charts comparative to other applicants
- [ ] Notifications for upcoming events
- [ ] “Offers page” to track and manage open offers
- [ ] Gmail integration to allow a user to see all emails from the email listed as the contact for the application
- [ ] Market salary calculation through payscale api
- [ ] Resume uploading and management system

[ChartJS]: CharJShttp://www.chartjs.org/
