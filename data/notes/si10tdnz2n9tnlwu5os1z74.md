
```abap
CLASS … DEFINITION … .
  PUBLIC SECTION.
    METHODS get_amount_in_coins 
      IMPORTING
        i_amount TYPE i
        i_cash_provider TYPE REF TO if_cash_provider OPTIONAL
      RETURNING VALUE(r_value) TYPE i.
  PRIVATE SECTION.
  DATA m_cash_provider TYPE REF TO if_cash_provider.
…
ENDCLASS.

CLASS … IMPLEMENTATION.
  METHOD get_amount_in_coins.
    DATA(cash_provider) = CAST if_cash_provider(
                  COND #( WHEN i_cash_provider IS BOUND
                      THEN i_cash_provider
                      ELSE NEW cl_cash_provider( ) ) ).
  …
  ENDMETHOD.
…
ENDCLASS
```
