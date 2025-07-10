# ⚙️ **Pro Commands**

This section covers powerful text-processing tools in Linux: **AWK**, **SED**, and **GREP** useful for parsing logs, filtering data, and scripting.

---

## 📊 AWK – Column-based Text Processing

| Command | Description |
|--------|-------------|
| `head -n 2 filename` | Prints the first 2 lines of a file. |
| `awk '{print $1,$2}' filename` | Prints the 1st and 2nd columns of each line. |
| `awk '/EVENT/ {print $1,$2,$3,$5}' filename` | Filters lines containing "EVENT" and prints selected columns. |
| `awk '/EVENT/ {print count++}' filename` <br> `awk '/EVENT/ {count++} END {print count}' filename` | Counts how many times "EVENT" appears. |
| `awk '$2 >= "08:53:53" && $2 <= "08:54:35" { print $2 }' filename` | Prints column 2 for lines within a time range. *(Change `$2` as needed)* |
| `awk 'NR >= 2 && NR <= 10 {print}' filename` | Prints lines from line number 2 to 10. |

> 🧠 **Note:** AWK is best for working with **structured data (columns)**.

---

## 🧹 SED – Stream Editing (Line by Line)

| Command | Description |
|--------|-------------|
| `sed 's/INFO/LOG/g' filename` | Replaces all "INFO" with "LOG" in the file. |
| `sed -n '/INFO/=' filename` | Prints line numbers where "INFO" is found. |
| `sed -n -e '/INFO/=' -e '/INFO/p' filename` | Prints both "INFO" lines and their line numbers. |
| `sed '1,15 s/INFO/LOG/g; 1,10p; 11q' filename` | Replaces "INFO" with "LOG" from lines 1–15, prints 1–10, and quits at line 11. |

> 🧠 **Note:** SED is used for **structured, semi-structured, or unstructured data** – it works **line by line**.

---

## 🔍 GREP – Pattern Searching

| Command | Description |
|--------|-------------|
| `grep -i INFO filename` | Case-insensitive search for "INFO". |
| `grep -i -c info filename` | Counts how many times "info" appears (case-insensitive). |
| `ps aux` | Lists all running processes. |
| `ps aux \| grep ubuntu` | Filters processes containing "ubuntu". |
| `ps aux \| grep ubuntu \| awk '{print $2}'` | Prints the process ID (2nd column) of "ubuntu" processes. |

---

> 🧾 **Summary:**
> - **AWK** → For **structured, column-wise data** (powerful for logs, CSVs, etc.)
> - **SED** → For **line-wise editing**, replacements, and range-based operations
> - **GREP** → For **searching specific patterns or keywords**

---

