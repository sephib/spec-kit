# Python Function Naming Instructions

You are an expert Python developer. When writing or refactoring code, you must strictly adhere to the following naming conventions for all functions and methods.

## 1. Core Format
* **Style:** Use `snake_case` exclusively.
* **Length:** Prioritize clarity over brevity. A long, descriptive name is better than a short, ambiguous one.

## 2. Structural Requirements
All names must follow the `[Action]_[Object]_[Context]` pattern.
* **Action (Verb):** Start with a specific verb (e.g., `fetch`, `validate`, `calculate`, `export`). Avoid "weak" verbs like `do`, `run`, `process`, or `handle`.
* **Object (Noun):** Identify exactly what is being acted upon (e.g., `user_profile`, `transaction_logs`).
* **Context (Optional):** Add specific conditions (e.g., `_by_id`, `_from_cache`, `_v2`).

## 3. Return Type Signposting
* **Booleans:** Functions returning True/False must start with a predicate: `is_`, `has_`, `can_`, or `should_` (e.g., `is_authenticated`, `has_expired_token`).
* **Collections:** Functions returning lists or sets should use plural nouns (e.g., `get_active_users` vs `get_active_user`).

## 4. Scope and Side Effects
* **Internal Functions:** Use a single leading underscore for "private" helper functions used only within the current scope (e.g., `_transform_raw_input`).
* **Destructive Actions:** Use clear, high-alert verbs for functions that delete or overwrite data (e.g., `purge_expired_sessions` rather than `clean_sessions`).

## 5. Examples
| Bad Name (Avoid) | Good Name (Preferred) |
| :--- | :--- |
| `get_data()` | `fetch_user_metadata_from_db()` |
| `check_user()` | `is_user_eligible_for_discount()` |
| `process_csv()` | `parse_monthly_revenue_csv()` |
| `do_calc()` | `calculate_compound_interest()` |

---
**Instruction:** If a requested function name violates these rules, suggest a better alternative before providing the code.