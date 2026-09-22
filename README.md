![AutoLane Garage Marketplace](assets/cover.svg)

# AutoLane Garage Marketplace

> A location-aware marketplace for discovering, listing, managing, and promoting garage or parking space.

[![Case study](https://img.shields.io/badge/case%20study-private%20delivery-2B6CB0)](SECURITY.md)
[![React](https://img.shields.io/badge/React-18-149ECA?logo=react&logoColor=white)](https://react.dev/)
[![Firebase](https://img.shields.io/badge/Firebase-Auth%20%26%20services-FFCA28?logo=firebase&logoColor=111827)](https://firebase.google.com/)
[![Stripe](https://img.shields.io/badge/Stripe-payments-635BFF?logo=stripe&logoColor=white)](https://stripe.com/)

## Overview

AutoLane connects people searching for affordable garage or parking space with owners who can publish, price, and manage listings. The product combines geospatial search, listing creation, document/media uploads, owner management, advertising by postal area, payment flows, and an administrative console.

## My contribution

- Multi-route React application with public search and authenticated owner journeys
- Garage listing creation/editing with validation, image/document upload, pricing, deposits, and policies
- Mapbox-powered location and directions experience
- Firebase authentication and Redux state management
- Stripe-powered advertising/payment flow with success handling
- Admin management for garages, users, advertisements, fees, discounts, and postal areas
- Responsive UI composed from Bootstrap, Material UI, and reusable form patterns

## Skills demonstrated

| Area | Applied |
| --- | --- |
| React | Route-based product areas, protected views, reusable forms, listing details, and owner/admin workflows |
| State management | Redux actions/reducers for auth, garage data, metrics, and application state |
| Mapping | Mapbox geocoding, coordinates, directions, and location-aware discovery |
| Payments | Stripe Elements and payment success/failure handling for paid promotion workflows |
| Authentication | Firebase Auth integration and role-aware admin access |
| Data & files | API integration, image previews, insurance/contracts, and listing media workflows |
| UX | Search, filters, pricing summaries, confirmation states, responsive forms, and feedback dialogs |

## Core flow

```mermaid
flowchart LR
    Search[Search by location] --> Details[Review garage details]
    Owner[Owner account] --> Create[Create listing]
    Create --> Upload[Add images and documents]
    Upload --> Review[Admin review]
    Review --> Publish[Publish listing]
    Publish --> Promote[Optional paid advertising]
```

## Technical stack

React 18 · React Router · Redux · Firebase Auth · Mapbox SDK · Stripe · Material UI · Bootstrap · Axios · React Hook Form · PDF rendering.

See [architecture](docs/ARCHITECTURE.md), [user flows](docs/USER-FLOWS.md), [security policy](SECURITY.md), [screenshot guide](docs/SCREENSHOT-GUIDE.md), and [GitHub setup](docs/GITHUB-SETUP.md).
"# autolane-garage-marketplace" 
