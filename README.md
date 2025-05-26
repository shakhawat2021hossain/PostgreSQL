### 1. What is PostgreSQL?

PostgreSQL হলো একটি Relational Database Management System(RDBMS)। এটি ডেটা সংরক্ষণ, ব্যবস্থাপনা এবং অনুসন্ধান করার জন্য ব্যবহৃত হয়। এটা একটা software, যেটা আমাদের tools & interface দেয়, CRUD Operation, security, control এর জন্য। SQL ব্যবহার করে আমরা এর সাথে interact করি।

---


### 3. Explain the Primary Key and Foreign Key concepts in PostgreSQL.

- **Primary Key:**
- এটি এমন একটি কলাম বা কলামের সমন্বয় যা প্রতিটি সারিকে (row) ইউনিকভাবে চিহ্নিত করে। এক টেবিলে একটি মাত্র প্রাইমারি কী থাকে এবং এটি কখনো NULL হতে পারে না।
- Primary Key ২ টি কলামের সমন্বয় হলে সেটাকে Composite primary key বলে।

- **Foreign Key:**
- এটি এমন একটি কলাম যা অন্য টেবিলের primary key এর সাথে সংযুক্ত থাকে। এটি দুইটি টেবিলের মধ্যে সম্পর্ক তৈরি করে।

---

### 4. What is the difference between the VARCHAR and CHAR data types?

- **CHAR(n):** এটি ফিক্সড-length ডেটা টাইপ। যত অক্ষরই রাখুন না কেন, এটি সবসময় নির্ধারিত `n` সংখ্যক অক্ষর সংরক্ষণ করে। অতিরিক্ত স্থানে স্পেস দিয়ে পূরণ করে।

- **VARCHAR(n):** এটি ভ্যারিয়েবল-length ডেটা টাইপ। এটি শুধুমাত্র যতটুকু অক্ষর লাগে ততটুকুই সংরক্ষণ করে। অতিরিক্ত স্পেস নষ্ট হয় না।

---

### 5. Explain the purpose of the WHERE clause in a SELECT statement.
এটা data filtering এ ব্যবহিত হয়। `WHERE` ক্লজ ব্যবহার করে নির্দিষ্ট শর্ত অনুযায়ী রেকর্ড ফিল্টার করা হয়। এটি `SELECT`, `UPDATE`, `DELETE` ইত্যাদি স্টেটমেন্টের সাথে ব্যবহার করা যায়, যাতে শুধুমাত্র প্রয়োজনীয় রেকর্ডগুলোর উপর কাজ করা যায়।

Example:
```sql
SELECT * FROM species WHERE conservation_status = 'Endangered';
```
---

### 7. How can you modify data using UPDATE statements?

PostgreSQL-এ UPDATE স্টেটমেন্ট ব্যবহার করে টেবিলের ডেটা পরিবর্তন করা যায় ।

Example:
```sql
UPDATE table_name
SET column1 = value1,
    column2 = value2,
    ...
WHERE condition;

