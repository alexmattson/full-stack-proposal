# API Endpoints

## HTML API

### Root

- `GET /` - loads React web app

## JSON API

### Users

- `POST /api/users`
- `PATCH /api/users`

### Session

- `POST /api/session`
- `DELETE /api/session`
- `GET /api/session`

### Applications

- `GET /api/applications`
  - Applications index/search
- `POST /api/applications`
- `GET /api/applications/:id`
- `PATCH /api/applications/:id`
- `DELETE /api/applications/:id`

### Events

- `GET /api/events`
  - Used in profile page
  - includes query param for only selecting events on currently viewed month
- `GET /api/applications/:application_id/events`
  - Retrieves events for a single application
- `POST /api/applications/:application_id/events`
  - if event doesn't already exist, it will be created
- `PATCH /api/applications/:application_id/events/:event_id`
  - if event exists, it will update it
- `DELETE /api/applications/:application_id/events/:event_id`
  - if event exists, it will delete it
