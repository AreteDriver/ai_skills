---
name: Test Strategy
category: testing
priority: 4
description: How to write effective tests and choose the right level of testing.
---

# Test Strategy Skill

## Test Pyramid
1. **Unit tests** (many) — Single function/class, fast, no I/O.
2. **Integration tests** (some) — Components working together, may use test DB.
3. **E2E tests** (few) — Full user flow through the real system.

## What to Test
- Happy path for every public function.
- Edge cases: empty input, null, boundary values, max length.
- Error paths: invalid input, network failure, permission denied.
- Regressions: every bug fix gets a test.

## What NOT to Test
- Private implementation details (test behavior, not structure).
- Third-party library internals.
- Trivial getters/setters with no logic.

## Test Quality
- **Arrange, Act, Assert** — One clear action per test.
- **Descriptive names** — `test_returns_404_when_user_not_found`, not `test1`.
- **No test interdependence** — Each test sets up its own state.
- **Fast** — Unit test suite should complete in seconds.
- **Deterministic** — No flaky tests. Mock external services and clocks.

## Coverage
- Aim for high coverage on business logic, not 100% everywhere.
- Coverage is a floor, not a ceiling — passing tests still need to assert the right things.
