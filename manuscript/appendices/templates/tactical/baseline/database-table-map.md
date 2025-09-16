# 🗄 Database Table Map

## Table: [Table Name]

**Description:** [What this table represents in the business]

**Queries Found:**
| # | Query Snippet / Location | Type (Read/Write) | Notes |
|---|--------------------------|-------------------|-------|
| 1 | `SELECT * FROM invoices WHERE status = 'overdue'` (InvoiceRepository.php:45) | Read | Used for reminders |
| 2 | `UPDATE invoices SET status = 'paid'` (PaymentService.php:102) | Write | Should trigger event but doesn’t |

**Joins:**
- Joins with `customers` on `customer_id`
- Joins with `payments` on `invoice_id`

---
