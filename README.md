# ☁️ Automated AWS Receipt Processing System

This project automates the extraction and storage of data from receipt images using AWS cloud services. It eliminates manual data entry by leveraging AI-driven OCR, serverless workflows, and real-time notifications.

---

## 📌 Project Overview

Manual receipt processing is time-consuming, error-prone, and hard to scale. This solution uses **Amazon Textract** to intelligently extract data from receipts and store it in **DynamoDB**. The entire process is automated using **AWS Lambda**, with files stored in **S3** and notifications sent via **Amazon SES**.

---

## 🛠️ Architecture & Services Used

| Layer             | AWS Service          | Description                                     |
| ----------------- | -------------------- | ----------------------------------------------- |
| **Storage**       | Amazon S3            | Stores uploaded receipt images (JPG, PNG, PDF)  |
| **Processing**    | Amazon Textract      | Extracts text and structured data from receipts |
| **Database**      | Amazon DynamoDB      | Stores structured receipt data                  |
| **Compute**       | AWS Lambda           | Automates the processing workflow               |
| **Notifications** | Amazon SES           | Sends email notifications with receipt details  |
| **Security**      | IAM Roles & Policies | Secure access between AWS services              |

---

## 🔧 Setup & Workflow

1. **Upload receipt** to S3 bucket.
2. **Trigger Lambda** function on new file upload.
3. **Textract processes** image and extracts text.
4. **Lambda stores** extracted data in DynamoDB.
5. **SES sends** email notification with parsed details.

---
## 🧪 Testing

* Test by uploading various receipt formats (images or PDFs).
* Confirm data is stored in DynamoDB.
* Check for successful email notification via SES.

---


## 🧼 Cleanup Instructions

To avoid charges:

* Delete the **S3 bucket** and uploaded files
* Stop **Textract** API calls
* Delete **DynamoDB** table
* Disable **SES** and remove verified emails
* Remove **IAM Roles and Policies**

---

## 💡 Future Improvements

* Add support for batch processing
* Build a frontend dashboard (React or Vue)
* Implement custom data validation and formatting

---

## 📂 Tech Stack

`AWS Lambda` · `Amazon Textract` · `Amazon S3` · `Amazon DynamoDB` · `Amazon SES` · `IAM` · `Python`

