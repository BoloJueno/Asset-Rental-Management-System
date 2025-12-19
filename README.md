# HOA Asset Rental Management System

### Database Application Project

Java Web Application (JSP/Servlets + MySQL)

---

## 📌 Overview

This project is a Java-based web application developed as part of the *Homeowners Association (HOA) Database Application Project*. It implements **Feature Set 2**, focusing on the full rental lifecycle for subdivision-owned assets.

The system is designed for the **HOA Officer in Charge of Assets**, enabling them to efficiently register assets, manage rental transactions, authorize returns, and maintain accurate, policy-compliant records.

This application is built to interact with the official HOA database schema based on the provided project case documentation.

---

## 🎯 Core Features (Feature Set 2)

### **1. Register an Asset**

* Add new property, equipment, furniture, and other assets.
* Provide asset classification, value, acquisition information, condition, and location.

### **2. Update Asset Information**

* Modify existing asset details.
* Prevent modification of system-controlled values unless permitted.

### **3. Delete Wrongly Encoded Assets**

* Only possible if:

  * Asset has **no activities**,
  * **No rental transactions**, and
  * **No disposal records**.
* Enforces HOA policy: assets in use cannot be deleted.

### **4. Dispose an Asset**

* Mark asset as *For Disposal* or *Disposed*.
* Records the decision for audit compliance.

### **5. Record Rental**

* Create rental transactions with:

  * Reservation date
  * Rental date
  * Resident renting the asset
  * Authorizing officer
  * Rental amount & discounts
  * Rental status (Reserved, Cancelled, On Rent, Returned)

### **6. Process Rental Return**

* Record return date & inspection details.
* Attach assessed damage fees if necessary.
* Automatically updates status to **Returned**.
* Includes linked child assets for bundled rentals.

### **7. Update Rental Information**

* Modify non-restricted rental details.
* Maintains change logs for audit traceability.

### **8. Delete Rental Information**

* Allowed only with **HOA President approval**.
* Rentals are not physically deleted;
  → Status is updated to **Deleted**, following HOA regulatory requirements.

---

## 🏛 System Architecture

* **Frontend:** JSP, HTML, CSS
* **Backend:** Java Servlets
* **Database:** MySQL

