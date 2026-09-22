# Architecture

The React client separates public discovery, owner listing flows, payment surfaces, and admin operations into route-level screens. Firebase provides authentication, Mapbox handles geospatial interaction, and Stripe handles paid promotion. Redux coordinates cross-screen state while API services isolate remote requests from UI components.

