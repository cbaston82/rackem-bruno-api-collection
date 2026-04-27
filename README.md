# Rackemm Bruno API Collection

Bruno API collection for the [rackemm-api-node](https://github.com/cbaston82/rackemm-api-node) backend. Rackemm is a pool tournament finder — find a tournament anywhere, anytime.

## Related Projects

| Project | Repo |
|---|---|
| Frontend (React, Redux, TailwindCSS) | [rackemm-ui](https://github.com/cbaston82/rackemm-ui) |
| Backend (Node, Express, MongoDB) | [rackemm-api-node](https://github.com/cbaston82/rackemm-api-node) |
| API Collection (Bruno) | [rackemm-bruno-api-collection](https://github.com/cbaston82/rackemm-bruno-api-collection) |

## Getting Started

**1. Clone the repo**

```bash
git clone https://github.com/cbaston82/rackemm-bruno-api-collection
```

**2. Open in Bruno**

Open Bruno and load the cloned folder as a collection. See [Bruno docs](https://docs.usebruno.com/introduction/what-is-bruno) if you haven't used Bruno before.

**3. Set up the environment**

Select the `rackemm` environment. Update the `token` variable after logging in via the `auth/login` request.

The API runs at `http://localhost:4000/api/v1` by default. Make sure [rackemm-api-node](https://github.com/cbaston82/rackemm-api-node) is running locally.

## Collection Structure

```
auth/
  login               POST  /api/v1/auth/login
  register            POST  /api/v1/auth/register

events auth/          (requires token)
  events              GET   /api/v1/events
  event               GET   /api/v1/events/:id
  create event weekly POST  /api/v1/events
  create event special POST /api/v1/events
  patch event special PATCH /api/v1/events/:id
  create event delete DEL   /api/v1/events/:id

events public/
  events              GET   /api/v1/events/public
  event               GET   /api/v1/events/public/:id
  event brackets      GET   /api/v1/events/public/:id/brackets
  event reviews       GET   /api/v1/events/public/:id/reviews
  events stats        GET   /api/v1/events/public/stats

filters auth/         (requires token)
  get all filters     GET   /api/v1/filters
  get a filter        GET   /api/v1/filters/:id
  create filter       POST  /api/v1/filters
  patch a filter      PATCH /api/v1/filters/:id
  delete filter       DEL   /api/v1/filters/:id

reviews auth/         (requires token)
  create review       POST  /api/v1/reviews
  patch review        PATCH /api/v1/reviews/:id
  delete review       DEL   /api/v1/reviews/:id

reviews public/
  get all reviews     GET   /api/v1/reviews
```

## Screenshot

![Bruno Collection Screenshot](https://res.cloudinary.com/hoo/image/upload/v1739751587/rackemm_images/bruno-screenshot.png)

![Rackemm Logo](https://res.cloudinary.com/hoo/image/upload/v1695232082/rackemm_images/app_images/rackemm-logo-transparent.png)

## Author

[@cbaston82](https://github.com/cbaston82)

## License

[MIT](https://choosealicense.com/licenses/mit/)
