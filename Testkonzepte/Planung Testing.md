# Planing for Test refactoring in Provisionary

The following tests need to be implemented (or checked & improved) in PR #80:

## Model Tests

- a model cannot be created without all required data
- a model can be created with the minimal required data
- a model can be created with all data
- relationships work
  - (not) valid with (0), 1, many other models
  - when this model is deleted, the associations are deleted too but the other model (almost always) "survives"
- Jobs are queued correctly

## Controller Tests

- index & show works without login
- create etc. does **not** work without login (=> redirect to login)
- should create/update/delete with valid data & login (=> redirect to correct page)
- should **not** create/update with invalid data & login (=> 422)
- Flash messages work
- Each page shows required information correctly
- Button only show if logged in
- Filtering & sorting works

## Integration Tests

- provision config flow
- server and service provisioning flow

## System Tests

- Inline edit works
