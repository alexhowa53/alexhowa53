# Campus-Connect API - Overview

This document sketches the primary API endpoints and request/response shapes.

Authentication:
- POST /api/auth/signup
- POST /api/auth/login
- POST /api/auth/refresh
- GET /api/users/me

Events:
- GET /api/events
- GET /api/events/:id
- GET /api/events/:id/poster

Admin:
- POST /api/admin/events
- PUT /api/admin/events/:id
- POST /api/admin/events/:id/authorize-organizer
- PUT /api/admin/events/:id/price
- PUT /api/admin/events/:id/tickets-available
- GET /api/admin/events/:id/purchases

Purchase:
- POST /api/events/:id/purchase
  - Body (example): { email, userId?, quantity, payment_method_token }
  - Validations:
    - quantity <= 10
    - user's total tickets for event + quantity <= 10
    - tickets_available >= quantity

Feedback:
- POST /api/events/:id/feedback
- GET /api/events/:id/feedback

Organizer:
- GET /api/organizer/events/:id/trends
- GET /api/organizer/events/:id/attendees

Utilities:
- GET /api/events/:id/capacity
- GET /api/orders/:id/tickets