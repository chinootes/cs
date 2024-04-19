---
id: p1ty1b2ir8g56shkio6srld
title: Constructor Injection
desc: ''
updated: 1708452314793
created: 1708452263500
---

```abap
CLASS … DEFINITION … .
  PUBLIC SECTION.
   METHODS constructor 
     IMPORTING i_cash_provider TYPE REF TO if_cash_provider OPTIONAL.
 PRIVATE SECTION.
   DATA m_cash_provider TYPE REF TO if_cash_provider.
 …
ENDCLASS.

CLASS … IMPLEMENTATION.
  METHOD constructor.
    m_cash_provider = COND #( WHEN i_cash_provider IS BOUND
               THEN i_cash_provider
               ELSE NEW cl_cash_provider( ) ).
  ENDMETHOD.
 …
ENDCLASS.
```
