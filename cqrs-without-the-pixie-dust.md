# CQRS Without the Pixie Dust

- Blue book and Red book of Domain-Driven-Design
- Axon Framework Open Source library
- Events will be the glue between commands and queries
- Event Driven Architecture without MicroServices?

### Event sourcing vs Event Streaming

- Event sourcing is a service consuming its own events to determine what it should do in the future.
- Value is in the actual events that happened, not what was stored (for example if a use added an item to a cart then deleted it from the cart. The database doesn't know anything happened, but the events know a lot happened).

### Eventual Consistency

- Whiel we fear it and attempt to avoid it, we end up getting the one thing that is worse: Eventual inconsistency.

## Be Event Driven!

- Being truly event-driven takes more than just using a specific tech stack.
- Event storming, Event Modelling, Domain-Drive Design (by Eric Evens)

## Awkward coupling

- Events invert and/or obfuscate dependencies
- Communication can't always be in past tense
