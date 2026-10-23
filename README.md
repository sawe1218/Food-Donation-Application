# FoodShare – Food Donation PWA

A progressive web app that connects food donors (restaurants, caterers, households) with NGOs and volunteers, so surplus food reaches people instead of landfill. Built as my MSc Computer Science dissertation project at Middlesex University London.

## Features

- **Donor, receiver, volunteer and admin roles** with protected routes
- **Donation listings and claims** – post surplus food, browse nearby donations, track claims
- **Location-based matching** with interactive maps (Leaflet + OpenCage geocoding)
- **Volunteer delivery tracking** with ride credits and a donation timeline
- **NGO partnership hub** for organisations to coordinate collections
- **In-app chat** between donors, receivers and volunteers
- **Impact tracking and badges** to reward regular donors
- **Push and email notifications** (Firebase Cloud Messaging, EmailJS)
- **Admin dashboard** for managing users and donations
- **Social sharing** of donations and impact

## Tech Stack

| Area | Tools |
|------|-------|
| Frontend | React 18, React Router 6, Material UI 7 |
| Backend | Firebase Authentication, Cloud Firestore, Firebase Cloud Messaging |
| Maps | Leaflet, React Leaflet, OpenCage |
| Notifications | FCM, EmailJS, React Toastify |
| Testing | Jest, React Testing Library |

## Getting Started

```bash
git clone https://github.com/sawe1218/Food-Donation-Application.git
cd Food-Donation-Application
npm install
cp .env.example .env   # add your Firebase and EmailJS keys
npm start
```

The app runs at `http://localhost:3000`.

## Testing

```bash
npm test                 # watch mode
npm run test:ci-unix     # single run with coverage
```

Tests cover authentication (login, registration, auth context), an end-to-end auth flow and the dashboard.

## Project Structure

```
src/
├── components/   # auth, chat, delivery, maps, ngo, impact, sharing, timeline
├── contexts/     # auth context
├── pages/        # dashboards, donations, claims, profile, achievements
├── services/     # Firebase configuration
├── hooks/ utils/ styles/
functions/        # Firebase Cloud Functions scaffold
docs/             # implementation notes, Firestore rules, admin guide
wireframes/       # original UI wireframes
```

## Licence

MIT
