---
creation date: <% tp.file.creation_date() %>
---
## Perspective Models:

- **Customer**
- **Admin**
- **M.M.G. Transactions**
- **Proof of Address (POA)**
- **Post Offices**
- **QuickBooks (QB) Invoices**

## Business Logic:

A user submits information for Proof of Address (POA) to the system, which then sends an M.M.G. payment link to the customer. POAs are created in the system. The customer interacts with the M.M.G. payment link and completes the payment. M.M.G. sends information back to the system in JSON format, which is used to update the created POAs' states in the system. This information is also sent to QuickBooks (QBs), which uses it to create invoices on the QBs side.

QBs notifies the customer of the successful payment. QBs then returns information to the system, where invoices for that payment are made. Admins create physical copies of POAs when they are paid for. The POAs are sent to the post office, where a stamp is added to the envelopes. Admins photograph the envelopes and upload the images to the system. The system then sends an email to the customer regarding their POA, with photographic evidence attached (POA states are updated during this process; a potential state name is 'verified'). The stamped POAs are then delivered to the post office, where they are sent to each individual customer physically.

## Relationships:

### One-to-One Relationships:

- Proof of address to M.M.G. transaction
- Proof of address to QuickBooks invoice
- Admins to account
- Customers to account

### One-to-Many Relationships:

- Customer to proof of addresses
- Customer to M.M.G. transactions
- Customer to QuickBooks invoices
- Post office to proof of addresses

### Many-to-Many Relationships:

- M.M.G. transactions to proof of addresses (if applicable)

## Additional Notes:

1. POAs are separated from payments. A user creates a POA in the system regardless of the payment's success. POAs have the following states:
    - Unpaid
    - Paid (when the customer successfully pays for the POA through an M.M.G. payment link)
    - Verified (after the admin photographs the envelope at the post office, linked to a POA; the image attachments trigger this state)

Link to original: [[2025-04-25]]