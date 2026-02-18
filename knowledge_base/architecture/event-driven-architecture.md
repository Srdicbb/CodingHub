# Event-Driven Architecture

> Phase 2.1 | Status: Partial | Priority: MEDIUM

## Current Knowledge

- Used RabbitMQ in crypto exchange project
- Used SignalR for real-time events in FIS and ESG projects
- Need to understand event sourcing, CQRS formally

## Examples / Notes

### Event Sourcing
- TODO: Storing events instead of state
- TODO: When it makes sense (audit trails, financial systems)
- TODO: Event replay and rebuilding state

### CQRS
- TODO: Separating read and write models
- TODO: When CQRS helps vs adds complexity
- TODO: CQRS + Event Sourcing combination

### Message Brokers
- TODO: RabbitMQ - exchanges, queues, bindings (deepen from crypto project)
- TODO: Kafka basics - when to use over RabbitMQ
- TODO: Dead letter queues, retry policies

## Questions / Confusions

- When is event sourcing worth the complexity?
- CQRS without event sourcing - is it useful?
- RabbitMQ vs Kafka - practical decision guide?
