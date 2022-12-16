# New Item

```mermaid
flowchart TB
    CREATE_PURCHASE[Create Purchase]-->FORWARD_SALES[Sales]
    CREATE_SALES[Create Sales]-->FORWARD_PURCHASE[Purchase]
    FORWARD_PURCHASE-->MANAGEMENT[Management]
    FORWARD_SALES-->MANAGEMENT[Management]
    MANAGEMENT-->QM[QM]
```
