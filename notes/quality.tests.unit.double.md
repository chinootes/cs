---
id: 4xlimo3qcr6q90b3gk85tqc
title: Test Double
desc: ''
updated: 1708453800352
created: 1708453622761
---

- Like stunt double, but for testing.
- For testing purposes, test double does the job of the code on which your code under test depends.

## Types of Test doubles
  
### Stub

Provides “indirect input”

1. Test places desired return value in stub
2. Stub returns the desired value to the code under test

```abap
CLASS ltd_stub DEFINITION FOR TESTING.
  PUBLIC SECTION.
    INTERFACES if_cash_provider PARTIALLY IMPLEMENTED.
    DATA m_notes TYPE if_cash_provider=>tt_change.
ENDCLASS.
        
CLASS ltd_stub IMPLEMENTATION.
  METHOD if_cash_provider~get_notes.
    r_notes = m_notes.
  ENDMETHOD.
ENDCLASS.
```

### Spy 

Logs the “indirect output”

1. Spy logs the value passed by the code under test
2. Test verifies the recorded value

```abap
CLASS ltd_spy DEFINITION FOR TESTING.
    PUBLIC SECTION.
    INTERFACES if_cash_provider PARTIALLY IMPLEMENTED.
    DATA m_currency TYPE string.
ENDCLASS.

CLASS ltd_spy IMPLEMENTATION.
    METHOD if_cash_provider~get_notes.
    m_currency = i_currency.
    ENDMETHOD.
ENDCLASS
```

### Fake

Simple implementation of depended-on component

### Mock 

Extension of stub, spy, and fake; verifies the “indirect input” and/or “indirect output” according to given expectations

1. Test places desired value in mock
2. Spy logs the value passed by the code
under test
3. Stub returns the desired value to the code
under test
4. Test verifies the recorded value

```abap
CLASS ltd_mock DEFINITION FOR TESTING.
    PUBLIC SECTION.
    INTERFACES if_cash_provider PARTIALLY IMPLEMENTED.
    DATA m_currency TYPE string.
    DATA m_currency_exp TYPE string.
    DATA m_notes TYPE if_cash_provider=>tt_change.
ENDCLASS.

CLASS ltd_mock IMPLEMENTATION.
    METHOD if_cash_provider~get_notes.
    m_currency = i_currency.
    r_notes = m_notes.
    ENDMETHOD.
    METHOD assert_expectations.
    cl_abap_unit_assert=>assert_equals(
    act = m_currency
    exp = m_currency_exp ).
    ENDMETHOD.
ENDCLASS.
```

### Dummy

Satisfies syntax requirements; does nothing

## References

Terminology from the book _xUnit Test Patterns, Gerard Meszaros_
