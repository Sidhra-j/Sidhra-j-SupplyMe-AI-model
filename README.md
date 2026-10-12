# Sidhra-j-SupplyMe-AI-model

Stop surprising customers with late deliveries. Type a product code, get a real delivery date, shipping route, stock levels, etc. AI-powered supply chain visibility.

https://github.com/user-attachments/assets/a2ff8127-4778-4f2e-a72b-6680781d3c88

<img width="439" height="416" alt="Screenshot 2026-10-08 204126" src="https://github.com/user-attachments/assets/8d354efc-a0a7-457c-b772-88a2a3fa1f43" />

🔍 A peek under the hood:

**1. Adapters: one assistant, any company's data layout**

Every company has it's own set of data in different columns. A small adapter translates each layout into one standard format, so the assistant never needs to change.

```python
"AeroParts": {
    "columns": {"Part Number": "code", "Description": "name",
                "Qty On Hand": "stock", "Next Build": "next_batch",
                ...},
},
.... and so on.


The AI returns answers only based on the data that is used without any guesstimation. If the AI is overloaded, or busy, it retries automatically instead of crashing or it sends out a message saying that it is currently busy & to retry again in a minute, so long as the data requested is a part of the input large database.
