You are an expert HPC architect and HPC user-experience designer.

Your task:
Analyze the following **HPC user type** and generate a **very complete, structured taxonomy** of all queries and needs that this user may ask in an HPC agentic chat system.

# User Type:
Input_User_Type: → REPLACE_THIS_WITH_USER_TYPE  (e.g., HPC Researchers, System Administrators, etc.)

# Output Format Requirements:

## 1️⃣ Category List (High-Level Overview)
Provide a list of all query / need / requirement categories for this user type.
Categories must cover EVERYTHING they may ask the system.

✅ Ensure categories include:
- HPC operations
- Monitoring (if applicable)
- Performance analysis
- Data management
- Troubleshooting and support
- Documentation and learning help
- Any domain-specific needs

## 2️⃣ Detailed Table Version
Create a table:

| Category | Description | Example Queries (3–5 each) | Agent(s) to Fulfill Request (RAG? Monitoring? Control?) |

Where:
- “Agent(s)” refers to which capability is needed:
    - RAG Agent (docs/wiki info)
    - ExaSage Monitoring Agent (real-time + historical telemetry)
    - HPC Job Executer Agent (actions on cluster)
    - Data Analytics Agent (performance insights)
    - Facility Agent (if relevant)
    - Admin capabilities if privileged

Include **at least 12 categories** — more if needed.

## 3️⃣ Permissions & Access Control Notes
Specify:
- Which categories require elevated privileges
- Which categories are public/user-level
- Security concerns / safe routing recommendation

## 4️⃣ Extended Example Questions Corpus
Provide at least **25 real natural-language user questions** that belong to the categories above.
Questions must be diverse in style and granularity.

## 5️⃣ Priority Tags (Optional)
Label each category with:
- (H) High Frequency
- (M) Medium Frequency
- (L) Low Frequency but high value

---
Rules:
- The taxonomy must be comprehensive enough for use in **agent routing + intent classification**
- Avoid generic wording — be HPC-specific (SLURM, MPI, GPU nodes, IPMI, Ganglia, etc.)
- Include **storage + data pipeline + Jupyter** if this user may use them
- Include **performance optimization + reproducibility** categories where relevant

---

Now generate the output for the given **User Type** above.
