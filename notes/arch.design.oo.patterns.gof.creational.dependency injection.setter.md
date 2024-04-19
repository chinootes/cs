---
id: fl33cgyb0rl5jff4v4zsa3g
title: Setter Injection
desc: ''
updated: 1708452306858
created: 1708452293552
---

```abap
CLASS … DEFINITION … .
  PUBLIC SECTION.
    METHODS set_cash_provider IMPORTING i_cash_provider TYPE REF TO if_cash_provider.
  PRIVATE SECTION.
    DATA m_cash_provider TYPE REF TO if_cash_provider.
…
ENDCLASS.

CLASS … IMPLEMENTATION.
  METHOD set_cash_provider.
    m_cash_provider = i_cash_provider.
  ENDMETHOD.
…
ENDCLASS.
```
