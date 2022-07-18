# Support & Service Flowchart

## Support ticket

```mermaid
graph TD;
    REQUEST([Cusotmer request])-->CHECK_REQUEST{Support: Check request}
    CHECK_REQUEST--Customization, Training, ...?-->DEFINE_SERVICE[Service: Define service with customer]
    DEFINE_SERVICE-->OFFER[Sales: Offer]
    OFFER-->ORDER[Customer: Order]
    ORDER-->ORDER_COFIRMATION[Sales: Order confirmation]
    ORDER_COFIRMATION-->PROVIDE_SERVICE[Service: Provide service]
    PROVIDE_SERVICE-->INVOICE[Sales: Create invoice]
    CHECK_REQUEST--Support?-->TICKET_ASSIGN[Support: Assign ticket]
    TICKET_ASSIGN-->PROVIDE_SUPPORT[Support: Provide support]
```

2022-01-01 - Version 1.0
