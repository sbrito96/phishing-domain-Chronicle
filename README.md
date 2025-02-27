# Investigating a Phishing Domain with Chronicle

## 📌 Project Overview
At a financial services company, I investigated a phishing email received by an employee. The email contained a suspicious domain: **signin.office365x24.com**. Using **Chronicle**, I determined whether other employees had received similar emails and if they had interacted with the domain.

![image](https://github.com/user-attachments/assets/5e3c6ce5-d982-4870-a8a9-68247f333ecb)

---

## **1️⃣ Performing the Domain Search**
To begin the investigation, I performed a domain search in **Chronicle**:

```plaintext
Domain: signin.office365x24.com
```

![image](https://github.com/user-attachments/assets/b020142e-2fd1-49a9-b402-c583eed6675f)


- Chronicle confirmed that the domain existed in the ingested data.
- The investigation expanded by searching related indicators such as **hostnames, IP addresses, URLs, email addresses, and file hashes**.

---

## **2️⃣ Evaluating Search Results**
After searching for the domain, Chronicle provided various insights:

![image](https://github.com/user-attachments/assets/df0c4952-c8fb-43c1-9709-0fc6e82966c0)


- **VT CONTEXT:** Several security vendors flagged this domain on Virus Total.

![image](https://github.com/user-attachments/assets/80e512ba-0af9-47ad-89bd-1f26b6bfd56c)


- **WHOIS Data:** Provided registration details of the domain owner.
- **Resolved IPs:** The domain resolved to `104.215.148.63 and 40.100.174.34`.

---

## **3️⃣ Investigating the HTTP Requests and Affected Assets**

By analyzing Chronicle’s **Timeline** and **Assets** tabs:

![image](https://github.com/user-attachments/assets/d8afa77f-75b1-4a10-9173-78d103a30ec9)


- **Timeline:** Displayed HTTP requests made to the domain.
  - **GET Requests:** Indicated that employees visited the phishing site.
  - **POST Requests:** Suggested that login credentials were submitted, indicating a potential successful phishing attack.

- **Assets:** Listed the hostnames and devices that accessed the domain.

![image](https://github.com/user-attachments/assets/44a2d134-a6a1-48c6-8745-6b1a7a3c978a)


---

## **5️⃣ Key Takeaways and Mitigation Strategies**
Through this investigation, I successfully:

✅ **Identified a phishing domain**.  
✅ **Confirmed multiple assets interacted with the domain** via GET and POST requests.   
✅ **Provided intelligence for incident response** to mitigate further compromise.

### **🚀 Recommended Security Measures:**

- **Block the identified domains and IPs** at the network level.
- **Notify affected employees** and reset compromised credentials.
- **Enhance phishing detection** through security awareness training.
- **Enable multi-factor authentication (MFA)** to mitigate credential theft.

---

### **Conclusion**
Using **Chronicle**, I effectively investigated a phishing attempt and analyzed asset interactions. 
