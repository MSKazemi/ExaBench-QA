---

## 🧠 **Tip for Scaling to 500 Queries**

When you grow your dataset:

* Keep **`query_text` + `intent`** as the semantic anchors.
* Treat **`category`, `user_type`, and `data_sources`** as your *taxonomy dimensions*.
* Use **`expected_answer` + `evaluation_signal`** for your *evaluation schema*.
* Automate population of **`created_at`, `dedupe_of`, `notes`** later with scripts.

---

If you like, I can give you a **benchmark design matrix** template (role × category × difficulty) showing how each key fits into evaluation stages (retrieval, reasoning, formatting, scoring). Would you like that next?