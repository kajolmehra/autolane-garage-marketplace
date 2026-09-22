# User flows

```mermaid
flowchart LR
    Visitor[Search location] --> Listings[Compare listings]
    Listings --> Detail[Review garage detail]
    Owner[Owner] --> Listing[Create listing]
    Listing --> Documents[Upload documents]
    Documents --> Approval[Admin approval]
    Approval --> Live[Publish listing]
    Live --> Payment[Promote by postal area]
```

