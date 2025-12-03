# 📄 Contract Generation Automation – n8n Workflow

This n8n workflow automates contract creation, validation, and notification to sales agents and administrators.

---

## **Setup Instructions**

1. **Import the Workflow**

   * Open your n8n instance.
   * Go to `Workflows → Import`.
   * Select the workflow JSON file provided and import it.

2. **Add Necessary API Keys**

   * Add credentials for **Google Drive**, **Google Doc**, and **Gmail** nodes.
   * Make sure the credentials have access to create and send documents.

3. **Prepare the Contract Template**

   * Copy your contract template to Google Drive.
   * [https://docs.google.com/document/d/1VR0-SA0Z33dWaHbHATsvLAiNugHVm09BITYzFseC5M8/edit?usp=sharing](https://docs.google.com/document/d/1VR0-SA0Z33dWaHbHATsvLAiNugHVm09BITYzFseC5M8/edit?usp=sharing)
   * Rename it to:

     ```
     Contract - Starter Plan Template
     ```
   * Inside the **same folder** where the template is located, create a subfolder named:

     ```
     Sent Contracts
     ```
   * The workflow will copy the template, fill in customer data, and move completed contracts to this folder.

4. **Update Administrator Email**

   * Locate the node: `Send error message to administrator`.
   * Replace the **"to" email** with your administrator's email address.
   * This ensures the admin receives notifications if any errors occur.

---

## **Usage**

1. Trigger the workflow by submitting the form or adding data to the input node.
2. The workflow will:

   * Validate all fields (all are required).
   * Generate a new contract in Google Docs.
   * Notify the **sales agent** when the contract is ready.
   * Send an **error notification** to the admin and agent if validation or generation fails.
   * Move completed contracts to the `Sent Contracts` folder.

---

## **Notes**

* All numeric fields and dates are validated.
* Agents receive **human-readable error emails** if any field is missing or invalid.
* The workflow calculates **total contract value** and formats all currency fields.
* Make sure the Google Drive folder structure is correct for smooth operation.

---

## **Contact**

For issues with the workflow setup or execution, contact your system administrator.
