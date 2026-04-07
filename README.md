🌾 **Agmarknet Price API – Usage Guide**

A simple **REST API interface** to fetch real-time agricultural commodity prices (mandi rates) using query parameters.

---

### 🔗 **API Endpoint**

```text
http://127.0.0.1:5000/request?commodity=Item&state=State&market=City
```

---

### 🧾 **How to Use**

Replace the placeholders with actual values:

* `Item` → Commodity name (e.g., Potato, Tomato)
* `State` → State name (e.g., Karnataka)
* `City` → Market/City name (e.g., Bangalore)

---

### ✅ **Example Request**

```text
http://127.0.0.1:5000/request?commodity=Potato&state=Karnataka&market=Bangalore
```

---

### 📥 **Sample JSON Output**

```json
[
  {
    "S.No": "1",
    "City": "Bangalore",
    "Commodity": "Potato",
    "Min Prize": "1500",
    "Max Prize": "1800",
    "Model Prize": "1600",
    "Date": "04 Nov 2023"
  },
  {
    "S.No": "2",
    "City": "Bangalore",
    "Commodity": "Potato",
    "Min Prize": "1400",
    "Max Prize": "1700",
    "Model Prize": "1500",
    "Date": "04 Nov 2023"
  },
  {
    "S.No": "3",
    "City": "Bangalore",
    "Commodity": "Potato",
    "Min Prize": "1500",
    "Max Prize": "1800",
    "Model Prize": "1600",
    "Date": "03 Nov 2023"
  }
]
```

---

### 📊 **Response Fields Explained**

* **S.No** → Record index
* **City** → Market location
* **Commodity** → Selected item
* **Min Prize** → Minimum price (₹/quintal)
* **Max Prize** → Maximum price
* **Model Prize** → Average/modal price
* **Date** → Recorded date

---

### ⚠️ **Important Notes**

* Values must **exactly match dropdown options** from the source site
* API is **case-sensitive** in some cases
* Requires backend server (`app.py`) running locally
* Data reflects prices from the **last few days (typically 7 days)**

---

### 💡 **Tips for Better Usage**

* Validate inputs before calling API
* Cache responses to avoid repeated scraping
* Use in dashboards or mobile apps for real-time insights

---

### 🚀 **Why This API is Useful**

> Converts a **manual government website workflow** into a **programmable, reusable data service** for agriculture analytics and applications.

---

If you’re building agri-tech solutions, this API can be your data backbone 🌱
