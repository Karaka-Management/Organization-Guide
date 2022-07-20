# Support & Service Flowchart

```mermaid
graph TD;
    REQUEST([Customer request])-->IS_AUTHORIZED{Support: Is authorized?}
    IS_AUTHORIZED--Yes-->CHECK_REQUEST{Support: Categorize};
    IS_AUTHORIZED--No-->DECLINE[Support: Decline request]
    CHECK_REQUEST--Is customization, training, data migration, ...?-->DEFINE_SERVICE[Service: Define service with customer];
    DEFINE_SERVICE-->OFFER[Sales: Offer];
    OFFER-->ORDER[Customer: Order];
    ORDER-->ORDER_COFIRMATION[Sales: Order confirmation];
    ORDER_COFIRMATION-->PROVIDE_SERVICE[Service: Provide service];
    PROVIDE_SERVICE-->INVOICE[Sales: Create invoice];
    INVOICE-->ACCOUNTING[[Accounting]];
    CHECK_REQUEST--Support?-->TICKET_ASSIGN[Support: Assign ticket];
    TICKET_ASSIGN-->PROVIDE_SUPPORT[Support: Provide support];
    PROVIDE_SUPPORT-->CHECK_INVOICING{Has free support minutes?};
    CHECK_INVOICING--Yes-->NO_INVOICING([No Invoicing]);
    CHECK_INVOICING--No-->INVOICE;
```

2022-01-01 - Version 1.0
