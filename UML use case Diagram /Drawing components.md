**Use Case Diagram relationships** 

---

### **1. Communication Association**
- **What**: A direct interaction between an **actor** and a **use case**.
- **Who**: Any actor (e.g., Customer, Admin).
- **When**: When the actor uses the system to perform a task.

**Example**:
- A **Customer** browses products:
  ```
  Customer ---- Browse Products
  ```

---

### 2.  << include >> Relationship Relationship
- **What**: Reusable functionality shared between use cases.
- **Who**: The actor interacts with the **base use case**, which automatically includes the other use case.
- **When**: The included use case always executes as part of the base use case.

**Example**:
- **Customer** places an order, and the system **includes** payment verification:
  ```
  Customer ---- Place Order ----<<include>>---- Verify Payment
  ```

---

### 3. << extend >> Relationship
- **What**: Optional or conditional functionality added to a base use case.
- **Who**: The actor interacts with the **base use case**, and the extended use case happens only if conditions are met.
- **When**: When specific criteria (e.g., a discount is available) are satisfied.

**Example**:
- **Customer** places an order, and the system **extends** it with a discount if applicable:
  ```
  Customer ---- Place Order ----<<extend>>---- Apply Discount
  ```

---

### **4. Communication Generalization**
- **What**: Represents a **"is-a" relationship** between actors or use cases.
- **Who**: A specific actor or use case inherits behaviors from a more general one.
- **When**: Inherited behaviors are always available to the specific actor or use case.

**Example**:
- A **User** is generalized into **Customer** and **Admin**:
  ```
       User
      /    \
 Customer   Admin
  ```

---
