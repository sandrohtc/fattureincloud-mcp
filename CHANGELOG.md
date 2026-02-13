# Changelog

## [1.3.0] - 2026-02-13

### Fixed
- `create_invoice` ora include `ei_code` (codice univoco SDI) dall'anagrafica cliente
- `duplicate_invoice` ora verifica e aggiorna `ei_code` dal cliente in anagrafica
- Import `traceback` spostato a livello di modulo

### Added
- `check_numeration` - nuovo tool per verificare continuità numerica fatture per anno
- `build_entity_from_client()` - funzione centralizzata per costruzione entity con ei_code + PEC
- `get_ei_code_for_client()` - recupero codice SDI con fallback intelligente (ei_code → PEC → 0000000)
- Response di create/duplicate ora include campo `ei_code` per conferma

### Tool totali: 13

---

## [1.2.0] - 2025-12-15

### Added
- `delete_invoice` - elimina fatture bozza (non inviate)
- Verifica stato SDI prima dell'eliminazione

### Tool totali: 12

---

## [1.1.0] - 2025-12-10

### Added
- `send_to_sdi` - invio fattura elettronica allo SDI
- `get_invoice_status` - stato fattura con traduzioni italiane
- `send_email` - invio copia cortesia via email
- `list_received_documents` - fatture passive (fornitori)
- `get_situation` - dashboard finanziaria annuale
- `create_invoice` - creazione fatture come bozza
- `duplicate_invoice` - duplicazione con sostituzione testo

### Tool totali: 11

---

## [1.0.0] - 2025-12-09

### Initial release
- `list_invoices` - lista fatture emesse
- `get_invoice` - dettaglio fattura
- `list_clients` - lista clienti
- `get_company_info` - info azienda

### Tool totali: 4
