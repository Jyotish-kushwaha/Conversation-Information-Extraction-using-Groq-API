# Conversation Information Extraction using Groq API
## 📓 Colab Notebook

You can view and run the full implementation in Google Colab:

[Open Colab Notebook](https://colab.research.google.com/drive/1_XdRWSFqEl5LoOJS-8krR2cJh4Z9N_PV?usp=sharing)


## Project Overview
This project focuses on **extracting structured information** from user conversations using the **Groq API**, which is compatible with OpenAI’s SDK. The goal is to parse free-form chat messages and extract key user details in a **JSON format**, ensuring data consistency and validation.

**Key Extracted Details:**
- Name
- Email
- Phone
- Location
- Age

---

## Objective
The task aims to:
1. Convert unstructured user chat into **structured JSON output**.
2. Validate the extracted information against a **predefined schema**.
3. Demonstrate the workflow on multiple sample chats with different formats.

---

## Technologies Used
- **Python**: Standard libraries for JSON handling and validation.
- **Groq API**: For chat completion and function calling.
- **OpenAI Function Calling**: Ensures structured output.
- **JSON Schema**: Validates the correctness of the extracted data.
- **Google Colab**: Development and demonstration platform.

---

## Workflow

### Step 1: API Setup
Configure API key and endpoint for authentication with Groq API.

---

### Step 2: Define JSON Schema
Create a **JSON schema** specifying the structure and required fields:
- Type of each field (string/integer)
- Mandatory fields (e.g., name, email, phone)
- Optional fields (e.g., location, age)

---

### Step 3: Define Function
Define a function with the schema to instruct the model:
- Function name: `extract_user_info`
- Function description: "Extracts personal details from conversation"
- Parameters: JSON schema

---

### Step 4: Feed Chat Input
Provide **sample user messages**:
- Different formats and phrasings
- Some may have missing optional fields

---

### Step 5: Model Function Call
Use Groq API to call the model:
- Model receives messages and function definition
- Returns **structured JSON** matching the schema

---

### Step 6: Parse JSON Output
Extract the function call arguments as a **JSON dictionary**.

---

### Step 7: Validate JSON
- Use `jsonschema` to validate the output.
- Ensures all required fields are present.
- Detects errors if schema is not followed.

---

### Step 8: Demonstration
- Test on multiple sample chats:
  1. Full details provided
  2. Some missing optional fields
  3. Natural conversational variations

---


---

## Challenges & Solutions
| Challenge | Solution |
|-----------|---------|
| User input in different formats | Function calling ensures flexible parsing |
| Missing optional fields | Schema allows optional fields; required fields enforced |
| Free-text output inconsistencies | JSON schema enforces structured output |
| Multiple chat variations | Batch validation using `jsonschema` |

---

## Key Takeaways
- Function calling + JSON schema is powerful for **structured extraction**.
- Groq API is fully compatible with OpenAI SDK, easy to implement.
- Validation ensures **accuracy and reliability**.
- Lightweight solution with **no external frameworks**.

---

## Future Enhancements
- Add automatic **email/phone format validation**.
- Extend schema for additional fields like **profession, company, preferences**.
- Implement **batch processing** for multiple conversations.
- Direct integration with **databases** for automatic storage.

---




