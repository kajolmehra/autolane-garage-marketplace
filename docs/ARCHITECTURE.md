# Architecture

The React client separates public discovery, owner listing flows, payment surfaces, and admin operations into route-level screens. Firebase provides authentication, Mapbox handles geospatial interaction, and Stripe handles payment-method collection and recurring rental subscriptions. Redux coordinates cross-screen state while API services isolate remote requests from UI components.

## Payment and settlement model

1. A renter confirms the rental/lease terms, rental rate, and security deposit.
2. Stripe Elements collects the payment method and the API creates the recurring booking subscription.
3. The platform applies an administrator-configured per-payment service fee (the marketplace commission).
4. The contract/payment record retains the charge, deposit, fee, subscription result, and owner settlement state for operational reconciliation.

For each booking, the settlement view separates the money into three understandable buckets: renter charge, platform commission, and owner payable. The owner payable is the amount prepared for owner payment after the service fee is applied; the security deposit remains a separately labelled amount. Payment states can be presented as pending, succeeded, failed, or ready for settlement so support teams can reconcile exceptions without exposing card data.

The public case study intentionally describes the settlement state and workflow rather than exposing provider account IDs, webhook URLs, customer data, or production financial records.
