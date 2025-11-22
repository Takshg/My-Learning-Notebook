# Secure data

---

# Security features in spreadsheets

### **Key Points**

- **Data security:** Protecting data from unauthorized access or corruption.
- **Spreadsheet security features:**
    - **Sheet protection:** Locking specific cells or entire worksheets to prevent accidental edits.
    - **Access control:** Setting permissions for who can view and edit the spreadsheet.
    - **Password protection:** Encrypting files and worksheets for added security.
    - **User permissions:** Controlling who can access and edit the spreadsheet in Google Sheets.
    - **Hidden tabs:** Hiding specific tabs from view, but still accessible to those with permission.

### **Benefits of using these features**

- Prevents accidental edits to important data.
- Protects sensitive information from unauthorized access.
- Allows for collaboration with others while maintaining control over data.

### **Definitions**

- **Data security:** Protecting data from unauthorized access or corruption.
- **Sheet protection:** Locking specific cells or entire worksheets to prevent accidental edits.
- **Access control:** Setting permissions for who can view and edit the spreadsheet.
- **Password protection:** Encrypting files and worksheets for added security.
- **User permissions:** Controlling who can access and edit the spreadsheet in Google Sheets.
- **Hidden tabs:** Hiding specific tabs from view, but still accessible to those with permission.

---

# Balance security and and analytics

**Data security** means protecting data from unauthorized access or corruption by putting safety measures in place. Usually the purpose of data security is to keep unauthorized users from accessing or viewing sensitive data. Data analysts have to find a way to balance data security with their actual analysis needs. This can be tricky-- we want to keep our data safe and secure, but we also want to use it as soon as possible so that we can make meaningful and timely observations.

In order to do this, companies need to find ways to balance their data security measures with their data access needs.

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/kZCs4TZmRNmQrOE2ZkTZrg_aedb925fce3b47feb2918020a55a7d41_Screen-Shot-2020-12-18-at-1.08.57-PM.png?expiry=1716854400000&hmac=VvXlLGXDAKhLIApC4-MYv5Hoay6hgGqb1X6YawylaLA)

Luckily, there are a few security measures that can help companies do just that. The two we will talk about here are encryption and tokenization.

**Encryption** uses a unique algorithm to alter data and make it unusable by users and applications that don’t know the algorithm. This algorithm is saved as a “key” which can be used to reverse the encryption; so if you have the key, you can still use the data in its original form.

**Tokenization** replaces the data elements you want to protect with randomly generated data referred to as a “token.” The original data is stored in a separate location and mapped to the tokens. To access the complete original data, the user or application needs to have permission to use the tokenized data and the token mapping. This means that even if the tokenized data is hacked, the original data is still safe and secure in a separate location.

Encryption and tokenization are just some of the data security options out there. There are a lot of others, like using authentication devices for AI technology.

As a junior data analyst, you probably won’t be responsible for building out these systems. A lot of companies have entire teams dedicated to data security or hire third party companies that specialize in data security to create these systems. But it is important to know that all companies have a responsibility to keep their data secure, and to understand some of the potential systems your future employer might use.

However, one thing you absolutely can do to help strike the right balance is to use **version control** best practices. Version control enables all collaborators within a file to track changes over time. You can understand who made what changes to a file, when they were made, and why.

Here's a simple example: Perhaps you're working on a project with a team of other people. You are all collaborating within the same set of files, but each person is responsible for a different part of the project. Without version control, it would be very difficult to keep track of who made what changes to the files and when. This would lead to confusion and, even worse, people accidentally overwriting each other's work! Version control is essential for data analytics professionals because it allows users to effectively collaborate with others and experiment with new ideas without fear of losing their work.

---

# Protect your resources

## Maintain data privacy

On Kaggle, you can upload your own datasets and keep them private. This means that they are visible and accessible by only you. You also have the option to add collaborators to your dataset, whom you can add as viewers or editors. Viewers are able to see your private dataset and editors are able to make changes to your private dataset.

You can share the link to your private dataset so anyone with the link is able to view it. If you don’t want this feature, [you can disable it in the Settings tab of your dataset](https://www.kaggle.com/product-feedback/120243).

Note: If you have a private dataset on Kaggle and you choose to make it public, **you will not be able to make the dataset private again**. The only option you would have is to delete the dataset from Kaggle completely.

## Maintain version control

As for version control, Kaggle has its own style of letting you keep records of your progress. You can read all of the details [in this post](https://www.kaggle.com/product-feedback/139884), but think back to when you’ve done some work in a Kaggle notebook and clicked on the Save Version button.

When you clicked this button then clicked **Save**, you did it without changing anything. But you also have the option to add a short descriptive note about what changes you’ve made.

This can be helpful when you’ve made changes to your notebook but want to go back to an earlier version. To do this, go to **Edit** mode and click on the number next to the **Save Version** text at the top of your notebook.

[](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/tUE5VX1-StCZNjMoDVHBRw_77fdfdfa19bc44f09c7edeb88093b6f1_6IWJWIwUQlyfLJGarE7bsw_cbc98615ed784e27b1cc4bb3aa7c83e1_ZqwuKEEOXqTR9LNADM5YzlY_Y-xH4PXsfHHB9FvaV-gEah0nFKeR-EmnkwxzLNutgjquCjn_M2IGonpI7NzgVIftE2XwZqG16gtJuvpnqftWymMO664PI_moMAko4pS2PKu5GRTKFBCgbwGVbeK7CA?expiry=1716854400000&hmac=LrViGYabNgXls9BQNbEXIU9QbKVnVY_73TWOjSM0Ez4)

This will open a navigation bar on the right side of the screen and list out all of the versions of your notebook. When you click on different versions of your notebook, the left side of the screen will populate with the code and text from that version.

[](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/dQB2nYJDSBaF8Gu1Ge7LVA_a565e40e48964229b0c59219bdf873f1_262nj-ycQXKLN6Y2H1u7AQ_21c2c8e031fb4ed8a7eb94ed626011e1_7v1mMPLjC7dzNTqSEV5Io0DB2kAOtAREpToLnkcZn1PDP176_3lSDDFMPa_1bniPMGGm7BVEtdWritNUXhVIE-sAAHbYtp5sH2PY-4Z4VucQcSWKfEvkNZ9mVYaNbpJ9slyvCC62MGQK4lPU5mt6mA?expiry=1716854400000&hmac=iPogaYdBpIYkRBy2iOGrq8mhJFtxaASJbSMbjfhklXg)

Then, once the version has run, your screen will appear like this:

[](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/vtxIehKvSXytGeqqeFhQCg_b0d23d77bb0345559b1a3dda0c0e16f1_iSTykzEKQwaM6J_Z0PnYcg_8ea577eeb6504b3282fc5fe6c3d723e1_as5JEulRBNP52f6CqZVU7TODX7m-dcpF_X2E1ripYzCTcmQCfzSQaCsvOZ_-SJSjQXFa6qB7zuUuCwhqV3fVtwi7K4t71X_qmYAR9d51-KSzyzUxDI1QZd-MwxibTNaCWu_vVv5O-9YldnRtS323QQ?expiry=1716854400000&hmac=mNp1ehe8yv2EijlQKb51vKqp7ilXKrxUVx_R8nMu2C4)

From this screen you can also open the version in **Viewer** mode, pin a version as the default, or even change the version name. Pinning a version as the default can be helpful when you have a working version of your notebook available to the Kaggle community, but want to make changes and updates that might not work the first time you implement them. This allows you to safely make changes behind the scenes while sharing with the Kaggle community the most recent working version of your notebook.

---