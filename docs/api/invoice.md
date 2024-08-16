---
sidebar_position: 3
---

# Facility Booking

## Endpoint

<kbd>POST</kbd> `/invoices/facility`

## Request Parameters

### Header Parameters

| Header Parameter   |  Status  |  Type  | Description        |
| ------------------ | :------: | :----: | ------------------ |
| **X-Auth-Account** | required | string | authorized account |

### Body Parameters

| Body Parameter           |  Status  |  Type  | Description                                |
| ------------------------ | :------: | :----: | ------------------------------------------ |
| **external_id**          | required | string | unique transaction code                    |
| **customer_name**        | required | string | customer name                              |
| **customer_email**       | required | string | customer email                             |
| **customer_phone**       | required | string | customer phone                             |
| **payment_channel_code** | required | string | payment channel code                       |
| **product_code**         | required | string | product code                               |
| **subtotal**             | required | number | subtotal amount                            |
| **discount**             | optional | number | discount amount                            |
| **discount_code**        | optional | number | discount voucher code                      |
| **tax**                  | optional | number | tax amount                                 |
| **total**                | required | number | total amount [(subtotal - discount) + tax] |
| **booking_date**         | required |  date  | booking date                               |
| **booking_begin**        | required |  time  | booking begin time                         |
| **booking_end**          | required |  time  | booking end time                           |
| **note**                 | optional | string | additional note                            |

## Responses

### 200 - Success

### 401 - Unauthorized Account

```json
{
  "status": false,
  "msg": "Unauthorized account"
}
```