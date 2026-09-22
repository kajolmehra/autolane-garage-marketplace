# User flows

```mermaid
flowchart TB
    Visitor[Search location and dates] --> Listings[Compare approved listings]
    Listings --> Detail[Review garage detail, rate, deposit, and policies]
    Detail --> Terms[Confirm rental terms]
    Terms --> Checkout[Pay rental charge + security deposit]
    Checkout --> Authorised{Payment authorised?}
    Authorised -->|No| Retry[Correct payment details]
    Retry --> Checkout
    Authorised -->|Yes| Booking[Create booking / contract]
    Booking --> Recurring[Create recurring booking payment]
    Recurring --> Commission[Apply platform service fee]
    Commission --> OwnerPayment[Track owner balance and settlement state]
    OwnerPayment --> Reconcile[Reconcile charge, deposit, fee, and payout]

    Owner[Owner workspace] --> Listing[Create listing]
    Listing --> Documents[Upload images and insurance documents]
    Documents --> Approval{Admin review}
    Approval -->|Approved| Live[Publish listing]
    Approval -->|Changes needed| Listing
    Live --> Listings
    Live --> Payment[Promote by postal area]
```

## Booking payment and commission flow

- The renter reviews the garage, rental rate, deposit, and payment schedule before checkout.
- Stripe Elements tokenizes the card details; the application sends only the payment method reference to the payment API.
- The payment API creates the recurring subscription for the booking and returns a success or failure state to the contract screen.
- A configurable per-payment service fee represents the platform commission. Administrators can update the fee rule without exposing financial secrets in the client.
- The resulting payment, deposit, subscription, fee, and owner settlement state can be reconciled against the booking/contract record.
