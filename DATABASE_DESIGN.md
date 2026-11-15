# Database Design

## users

| Field | Type |
|---------|---------|
| id | BIGINT |
| username | VARCHAR |
| email | VARCHAR |
| password | VARCHAR |
| role | VARCHAR |

---

## customers

| Field | Type |
|---------|---------|
| id | BIGINT |
| name | VARCHAR |
| email | VARCHAR |
| phone | VARCHAR |

---

## orders

| Field | Type |
|---------|---------|
| id | BIGINT |
| customer_id | BIGINT |
| product_name | VARCHAR |
| status | VARCHAR |
| order_date | DATETIME |
| expected_delivery | DATETIME |

---

## refunds

| Field | Type |
|---------|---------|
| id | BIGINT |
| order_id | BIGINT |
| refund_status | VARCHAR |
| refund_amount | DECIMAL |

---

## tickets

| Field | Type |
|---------|---------|
| id | BIGINT |
| customer_id | BIGINT |
| title | VARCHAR |
| description | TEXT |
| status | VARCHAR |

---

## chat_sessions

| Field | Type |
|---------|---------|
| id | BIGINT |
| user_id | BIGINT |
| created_at | TIMESTAMP |

---

## Relationships

Customer
    |
    | One-To-Many
    |
Orders

Customer
    |
    | One-To-Many
    |
Tickets

Order
    |
    | One-To-One
    |
Refund

User
    |
    | One-To-Many
    |
Chat Sessions
