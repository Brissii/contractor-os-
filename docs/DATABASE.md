# ContractorOS Database Schema

## Companies

| Field | Type |
|-------|------|
| id | UUID |
| company_name | Text |
| phone | Text |
| email | Text |
| address | Text |
| created_at | Timestamp |

---

## Users

| Field | Type |
|-------|------|
| id | UUID |
| company_id | UUID |
| first_name | Text |
| last_name | Text |
| email | Text |
| password_hash | Text |
| role | Owner / Manager / Employee |
| created_at | Timestamp |

---

## Customers

| Field | Type |
|-------|------|
| id | UUID |
| company_id | UUID |
| first_name | Text |
| last_name | Text |
| phone | Text |
| email | Text |
| address | Text |
| city | Text |
| state | Text |
| zip | Text |
| notes | Text |

---

## Jobs

| Field | Type |
|-------|------|
| id | UUID |
| customer_id | UUID |
| estimate_id | UUID |
| status | Scheduled / Active / Complete |
| start_date | Date |
| end_date | Date |
| total_price | Decimal |
| estimated_profit | Decimal |
| actual_profit | Decimal |

---

## Estimates

| Field | Type |
|-------|------|
| id | UUID |
| customer_id | UUID |
| subtotal | Decimal |
| overhead | Decimal |
| profit_margin | Decimal |
| total_price | Decimal |
| status | Draft / Sent / Approved |

---

## Employees

| Field | Type |
|-------|------|
| id | UUID |
| company_id | UUID |
| first_name | Text |
| last_name | Text |
| pay_rate | Decimal |
| position | Text |
