# Campus-Connect

Campus-Connect is an online ticketing system for campus events. Features:
- Guest and registered user purchases (max 10 tickets per user per event)
- Admin-controlled prices, capacity, and organizer authorization (time-limited)
- Organizer dashboards for trends and feedback during authorized period
- Poster downloads, ticket PDF/QR generation, Stripe payment integration

Quick start (recommended stack: Node.js (Nest/Express), PostgreSQL, S3, Stripe):
1. Clone repo
2. Create a .env file from .env.example
3. Run database migrations (see schema.sql)
4. Start backend and frontend
5. Configure Stripe & S3 credentials

Next steps:
- Implement signup/login and email verification
- Implement event CRUD and poster uploads
- Implement purchase flow (Stripe integration) and ticket generation
- Implement admin & organizer dashboards

See schema.sql and api.md for DB design and endpoint sketches.