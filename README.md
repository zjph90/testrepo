# testrepo


## Legend
```mermaid
graph TD
    classDef sql_macro fill:#f34
    classDef mview fill:#338055
    classDef table fill:#4d47b3
    classDef ords fill:#803377
    ORDS:::ords
    sqlm["SQL Macro"]:::sql_macro
    mview["Mat View"]:::mview
    table["Table"]:::table
```

## AUM Table
```mermaid
graph TD
    classDef sql_macro fill:#f34
    classDef mview fill:#338055
    classDef table fill:#4d47b3
    classDef ords fill:#803377
    ords["aum_table/:account_id/:start_date/:end_date"]:::ords --> AUM_TABLE_ORDS_SQM:::sql_macro
    AUM_TABLE_ORDS_SQM --> AUM_MV_SQM:::sql_macro
    AUM_MV_SQM --> AUM_MV1:::mview
    AUM_MV_SQM --> RM_ACCOUNTS_SQM:::sql_macro
    RM_ACCOUNTS_SQM --> tabs["ODS:TRADING_ACCOUNTS+TA_CUST_LINK_TA_FEED+CUSTOMERS"]:::table
    click AUM_TABLE_ORDS_SQM "https://github.com/cmctechnology/alpha-data/blob/master/sql_macros/aum_table_ords_sqm.sql"
    click AUM_MV_SQM "https://github.com/cmctechnology/alpha-data/blob/master/sql_macros/aum_mv_sqm.sql"
    click AUM_MV1 "https://github.com/cmctechnology/alpha-data/tree/master/mviews/AUM_MV1"
    click RM_ACCOUNTS_SQM "https://github.com/cmctechnology/alpha-data/blob/master/sql_macros/rm_accounts_sqm.sql"    
```
