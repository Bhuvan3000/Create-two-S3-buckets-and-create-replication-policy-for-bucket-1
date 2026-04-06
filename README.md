# Create-two-S3-buckets-and-create-replication-policy-for-bucket-1

Youtube link: https://youtu.be/lg6SJxU0tBE


## 📌 Aim
To create two Amazon S3 buckets and configure replication from the source bucket to the destination bucket.

---

## 🛠️ Services Used
- Amazon S3
- AWS IAM

---

## 📂 Steps Performed

### 1. Create Source Bucket (Bucket-1)
- Logged into AWS Management Console
- Opened Amazon S3 service
- Created a new bucket named `bucket-1`
- Selected region and kept default settings

---

### 2. Create Destination Bucket (Bucket-2)
- Created another bucket named `bucket-2`
- Used the same region as bucket-1

---

### 3. Enable Versioning
- Enabled versioning on both buckets:
  - Bucket-1 (source)
  - Bucket-2 (destination)

---

### 4. Configure Replication Rule
- Opened **bucket-1**
- Navigated to **Management → Replication**
- Created a replication rule:
  - Rule name: `replication-rule`
  - Applied to all objects
  - Selected destination bucket: `bucket-2`
  - Created a new IAM role for replication
- Saved the rule

---

### 5. Replication Settings
- Selected: **Do not replicate existing objects**
- Applied replication to new objects only

---

### 6. Testing Replication
- Uploaded a file (`test.txt`) to bucket-1
- Verified that the file was automatically replicated to bucket-2



---

## ✅ Result
Successfully created two S3 buckets and configured replication. Objects uploaded to the source bucket were automatically replicated to the destination bucket.

---

## 📖 Conclusion
Amazon S3 replication ensures data redundancy and availability by automatically copying objects between buckets. This is useful for backup, disaster recovery, and maintaining data across regions.

---
