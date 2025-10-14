
### Fakes instead of mocks for unit tests
A fake is a lightweight, in-memory implementation of an interface that behaves like the real system but is fast and predictable.
Avoid mock objects that just record calls or verify interactions, because they often couple tests to implementation details rather than behavior.

