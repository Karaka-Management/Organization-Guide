# Sales Flowchart

```mermaid
graph TD;
    REQUEST([Cusotmer request])-->OFFER[Sales: Offer to customer]
    OFFER-->ORDER[Customer: Order];
    ORDER-->VALID_ORDER{Is valid?};
    VALID_ORDER--YES?-->ORDER_CONFIRMATION[Sales: Order confirmation];
    ORDER_CONFIRMATION-->DELIVERY[Warehouse/Service: Delivery to customer];
    DELIVERY-->INVOICE[Sales: Generate invoice];
    INVOICE-->BOOKING[Accounting: Booking invoice];
    BOOKING-->PAYMENT{Customer pays?};
    PAYMENT--YES?-->BOOKING_PAYMENT[Accounting: Book payment];
    PAYMENT--NO?-->REMINDER[Accounting: Create reminder];
    REMINDER--3-->PAYMENT;
    REMINDER-->LAWYER[Accouting: Collection with lawyer];
    REMINDER-->SELL_RECEIVABLE[Accounting: Sell receivables];
    REMINDER-->BAD_DEBT[CFO: Loss on bad debt];
    LAWYER-->LAWYER_PAID{Customer pays?};
    LAWYER_PAID--YES?-->BOOKING_PAYMENT;
    LAWYER_PAID--NO?-->BAD_DEBT;
```

2022-01-01 - Version 1.0
