![AutoLane Garage Marketplace](assets/cover.svg)

# AutoLane Garage Marketplace

> A location-aware garage marketplace with rental checkout, recurring booking payments, owner settlement tracking, and configurable platform commission.

[![Case study](https://img.shields.io/badge/case%20study-private%20delivery-2B6CB0)](SECURITY.md)
[![React](https://img.shields.io/badge/React-18-149ECA?logo=react&logoColor=white)](https://react.dev/)
[![Firebase](https://img.shields.io/badge/Firebase-Auth%20%26%20services-FFCA28?logo=firebase&logoColor=111827)](https://firebase.google.com/)
[![Stripe](https://img.shields.io/badge/Stripe-payments-635BFF?logo=stripe&logoColor=white)](https://stripe.com/)

## Overview

AutoLane connects people searching for affordable garage or parking space with owners who can publish, price, and manage listings. The product combines geospatial search, listing creation, document/media uploads, owner management, rental checkout, recurring booking payments, advertising by postal area, and an administrative console. Payment operations cover the renter charge, security deposit, configurable platform service fee/commission, and the resulting owner payment state.

## My contribution

- Multi-route React application with public search and authenticated owner journeys
- Garage listing creation/editing with validation, image/document upload, pricing, deposits, and policies
- Mapbox-powered location and directions experience
- Firebase authentication and Redux state management
- Stripe-powered rental checkout with payment-method validation, subscription creation, and success handling
- Configurable per-payment service fee/commission rules managed by administrators
- Owner/renter contract payment records, deposit visibility, and settlement/reconciliation states
- Admin management for garages, users, advertisements, fees, discounts, and postal areas
- Responsive UI composed from Bootstrap, Material UI, and reusable form patterns

## Skills demonstrated

| Area | Applied |
| --- | --- |
| React | Route-based product areas, protected views, reusable forms, listing details, and owner/admin workflows |
| State management | Redux actions/reducers for auth, garage data, metrics, and application state |
| Mapping | Mapbox geocoding, coordinates, directions, and location-aware discovery |
| Marketplace payments | Stripe Elements checkout for rental charges and security deposits, with clear success/failure states |
| Recurring billing | Subscription-based booking payments tied to the active rental/contract record |
| Commission & settlement | Configurable per-payment platform fee, owner payment state, and reconciliation-ready records |
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
    Publish --> Booking[Confirm rental terms]
    Booking --> Charge[Collect rental charge + security deposit]
    Charge --> Subscription[Create recurring booking subscription]
    Subscription --> Fee[Apply platform service fee / commission]
    Fee --> Settlement[Track owner settlement and payment state]
    Publish --> Promote[Optional paid advertising]
```

## Technical stack

React 18 · React Router · Redux · Firebase Auth · Mapbox SDK · Stripe · Material UI · Bootstrap · Axios · React Hook Form · PDF rendering.

See [architecture](docs/ARCHITECTURE.md), [user flows](docs/USER-FLOWS.md), [security policy](SECURITY.md), [screenshot guide](docs/SCREENSHOT-GUIDE.md), and [GitHub setup](docs/GITHUB-SETUP.md).
"# autolane-garage-marketplace" 
