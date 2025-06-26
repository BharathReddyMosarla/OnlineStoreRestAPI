# 🛒 Online Store REST API Automation Project

## 🔍 Overview

This project is an automated test suite for validating REST APIs of an **Online Store Application**.
It includes functional coverage of the following core modules:

* **Products**
* **Cart**
* **Users**
* **Login**

The automation suite uses a combination of **REST Assured**, **TestNG**, **Selenium**, and reporting tools to ensure comprehensive validation.

---

## 🛠️ Technology Stack

* **Language**: Java
* **Automation Tools**: REST Assured, Selenium WebDriver
* **Testing Framework**: TestNG
* **Build Tool**: Maven
* **Reports**: Allure Reports, Extent Reports
* **Data Management**: Java Faker, JSON, CSV
* **Other Libraries**: JSON Schema Validator, Gson, Jackson, ScribeJava APIs
* **Framework Type**: Data-Driven + Hybrid
* **Schema Validation**: JSON Schema
* **GraphQL Support**: Enabled (where applicable)

---

## 📁 Project Structure

```
online-store-rest-api/
│
├── src/
│   └── test/
│       └── java/
│           ├── payloads/
│           │   └── Payload.java
│           │     (Dynamic data creation using Java Faker based on POJOs)
│           │
│           ├── pojo/
│           │   ├── Address.java
│           │   ├── Cart.java
│           │   ├── CartProduct.java
│           │   ├── Geolocation.java
│           │   ├── Login.java
│           │   ├── Name.java
│           │   ├── Product.java
│           │   └── User.java
│           │
│           ├── routes/
│           │   └── Routes.java
│           │     (Centralized endpoint definitions)
│           │
│           ├── testcases/
│           │   ├── BaseClass.java
│           │   ├── ProductTests.java
│           │   ├── CartTests.java
│           │   ├── UserTests.java
│           │   └── LoginTests.java
│           │
│           └── utils/
│               ├── ConfigReader.java
│               ├── DataProviders.java
│               └── ExtentReporter.java
│
├── resources/
│   ├── cartSchema.json
│   ├── config.properties
│   ├── productSchema.json
│   └── userSchema.json
│
├── testdata/
│   └── productsTestData.json
│
├── logs/
│   └── test-execution.log
│
├── reports/
│   └── ExtentReport.html
│
├── allure-results/
│
├── pom.xml
├── testng.xml
└── README.md
```

---

## ✅ API Test Coverage

### HTTP Methods Covered:

* `GET` – Fetch products, users, carts, etc.
* `POST` – Create new users, products, cart items
* `PUT` – Update user/cart/product details
* `DELETE` – Remove specific entries

### Validations:

* Status Codes (`200`, `201`, `400`, `401`, `404`, etc.)
* Response Headers (e.g., Content-Type)
* Body Attributes (ID, name, quantity, etc.)
* Schema Validation using JSON Schema
* Authentication Mechanism

### Assertions:

* Using `assertThat()` for verifying response attributes
* Positive and Negative test scenarios with valid/invalid data

---

## ⚙️ Configuration & Execution

### 🔧 Configuration:

* Use `config.properties` to manage environment variables like base URI, timeouts, etc.
* Data-driven tests use external data from JSON and CSV files

### ▶️ Run Tests:

* **Group-wise / Parallel**: Modify `testng.xml` accordingly
* **Allure Reports**: `allure serve allure-results`
* **Extent Reports**: Auto-generated after execution

### 🧪 Run via Maven:

```bash
mvn clean test
```

---

## 📦 Dependencies

Key libraries included in `pom.xml`:

* `rest-assured`
* `testng`
* `json-path`, `xml-path`
* `json-schema-validator`
* `gson`, `jackson-databind`
* `javafaker`
* `scribejava-apis`
* `allure-testng`
* `extentreports`
* Maven Surefire and Compiler plugins

---

## 📌 Notes

* **Authentication**: Tested login functionality using secure authentication methods
* **GraphQL**: If available in any module, GraphQL request/response tested via custom queries
* **Reusable**: Routes and payloads are modular and reusable across test cases
* **Logs**: Execution logs captured under `/logs`

---

## 🙌 Contribution

Feel free to fork the repo, enhance the test suite, or raise issues for bugs or feature suggestions.
